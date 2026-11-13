# Hexnode API and integrations

Research checked against the linked documentation on 2026-11-13. The cloud examples below use `https://<portal>.hexnodemdm.com/api/v1/`; verify the actual base URL for regional, on-premises or other deployments. Endpoint availability and behavior can change.

## Authentication

Enable API access under Admin > API, and protect the API key as a secret. Hexnode's [authentication page](https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/authentication/) describes HTTP Basic authentication, while its endpoint examples send the key directly in the `Authorization` header. Follow the current example for the endpoint and confirm with the tenant; do not silently change the header to `Bearer` or invent a base64 format.

On a trusted administrative machine, after obtaining the key securely and placing it in the environment, this read-only request follows the [list devices example](https://www.hexnode.com/mobile-device-management/developers/devices/list-all-devices/):

```bash
curl --fail-with-body --silent --show-error \
  -H "Authorization: $HEXNODE_API_KEY" \
  "$HEXNODE_BASE_URL/api/v1/devices/?per_page=100&page=1"
```

Avoid printing headers or keys; protect logs, CI outputs and shell history. `curl` arguments and environment variables may be exposed to local processes; use a secret manager and an appropriate trusted execution environment for production. Never distribute the tenant key to managed devices.

## Documented operations

| Purpose | Method and path | Official source |
|---|---|---|
| List devices | `GET /devices/` | [List devices](https://www.hexnode.com/mobile-device-management/developers/devices/list-all-devices/) |
| List policies | `GET /policy/` | [List policies](https://www.hexnode.com/mobile-device-management/developers/policies/list-policies/) |
| Create policy | `POST /policy/` | [Create policy](https://www.hexnode.com/mobile-device-management/developers/policies/create-policy/) |
| Edit policy | `PUT /policy/{id}/` | [Edit policy](https://www.hexnode.com/mobile-device-management/developers/policies/edit-policy/) |
| Associate policy | `POST /actions/associate_policy/` | [Associate policy](https://www.hexnode.com/mobile-device-management/developers/actions/associate-policy/) |
| Set console friendly name | `POST /actions/save_friendly_name/` | [Set friendly name](https://www.hexnode.com/mobile-device-management/developers/actions/set-friendly-name/) |
| List automations | `GET /automations/list/` | [List automations](https://www.hexnode.com/mobile-device-management/developers/automations/api-to-list-automations/) |
| Initiate existing automation | `POST /automations/run-now/` | [Initiate automation](https://www.hexnode.com/mobile-device-management/developers/automations/initiate-automation-via-api/) |

Paths in this table are relative to `/api/v1`. Run-now executes an automation already created in the console; it does not establish an API for creating or editing automations. For other operations, consult the [developer index](https://www.hexnode.com/mobile-device-management/developers/), including actions, users, groups, apps, reports and content management.

## Policy association and automation bodies

The association endpoint uses top-level arrays, e.g. `{"policies":[45],"devicegroups":[12]}`. That shape is different from the automation run-now endpoint:

```json
{
  "automationList": [1],
  "applyFilter": true,
  "targets": {"devices": [123]}
}
```

The run-now documentation requires at least one target type. Validate IDs, scope and `applyFilter` behavior with the tenant. An accepted request means initiation, not necessarily successful execution on the device; inspect the action/automation status.

For policy payloads, use the authoritative platform-specific schema: [iOS](https://www.hexnode.com/mobile-device-management/developers/policies/ios-policies/), [Android](https://www.hexnode.com/mobile-device-management/developers/policies/android-policies/), [macOS](https://www.hexnode.com/mobile-device-management/developers/policies/macos-policies/), [Windows](https://www.hexnode.com/mobile-device-management/developers/policies/windows-policies/). Respect nesting, field spelling and conditionally required fields. Check whether the endpoint supports the exact setting; UI support does not automatically imply API support. Read existing state and understand PUT semantics before modifying a policy.

## Pagination, matching and retries

Device listing documents `page`, `per_page` (maximum 250), `results`, `count` and `next`. Search every page or use a documented server-side filter; do not assume a `serial_number` filter is supported. Match exact normalized serials and handle zero or multiple matches explicitly. When following `next`, ensure it remains HTTPS and on the expected trusted tenant origin before forwarding credentials; use documented page parameters if the link is malformed.

Handle network failures and HTTP 400, 401, 403, 404, 429 and 5xx distinctly. Check `Retry-After` when present and use bounded backoff with jitter for retryable reads. Avoid blindly retrying writes/actions: first determine whether the request already took effect or the operation is idempotent. HTTP success can indicate that an action was queued rather than completed.

## Integrations and event delivery

Consider [webhooks](https://www.hexnode.com/mobile-device-management/help/hexnode-integrations/webhooks/) rather than constant polling when the required event is supported. Verify event coverage, authentication and delivery behavior in current documentation; design receivers to tolerate duplicate or delayed events. For a centrally managed rename, validate the device identity and target, call the friendly-name action from the trusted service and verify the resulting console state. The friendly name is separate from an OS hostname.
