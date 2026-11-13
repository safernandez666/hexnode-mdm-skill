# Automation, scripts and troubleshooting

Sources checked 2026-11-13: [Automate](https://www.hexnode.com/mobile-device-management/automate/), [advanced scripting](https://www.hexnode.com/uem/features/advanced-scripting/), [Android scripts](https://www.hexnode.com/mobile-device-management/help/run-script-on-android/), [sample script repository](https://www.hexnode.com/mobile-device-management/help/sample-script-repository/) and [wildcards](https://www.hexnode.com/mobile-device-management/help/how-to-pass-device-and-user-information-using-the-wildcards-supported-by-hexnode-mdm/).

## Mechanism selection

| Need | Starting point | Verify |
|---|---|---|
| Persistent device configuration | Policy | OS support, enrollment mode, targets, conflicts and actual applied settings |
| Scheduled or event-driven grouped actions | Automate | Supported trigger for this platform, schedule, filters, targets and status |
| Immediate one-off action | Device action or an existing automation | Device eligibility, connectivity, privilege and per-device result |
| Scheduled/scripted configuration | Policy script or automation | Available triggers, execution context, retries and how completion is reported |

An automation can bundle actions and can be saved and run again; do not describe all automations as non-reusable. Do not assert that every policy has an enrollment trigger: confirm the actual UI or current documentation for the execution method. A startup-triggered script runs only after the relevant startup event; it is not synonymous with immediate execution on enrollment.

## Script design and secrets

- Hexnode documents PowerShell and other Windows formats, shell/AppleScript/JavaScript on macOS, Bash on supported Linux distributions, and Android shell/custom scripts on eligible devices. Confirm the OS, agent, vendor/device eligibility, permitted operations and exact execution context in the corresponding help article. Never assume Android shell access means root or arbitrary system privileges.
- Choose the least privilege needed. Specify interpreter, paths, arguments and timeout appropriate to the environment. Capture useful non-sensitive output; provide explicit nonzero failures and idempotent behavior when retries are possible. Test with the same privilege and execution context used by Hexnode.
- Tenant API keys belong in a trusted central integration or a properly managed secret system, not in scripts, policy payloads, arguments, logs, repositories or device images. Environment variables and protected files still expose secrets to some processes or administrators; confirm the actual access model. If a workflow requires distributing a tenant key, redesign it or state the limitation rather than hardcoding it.
- Prefer built-in management controls where appropriate; make changes observable, verify final state, and support pilot/rollback. Document what should happen if an API update fails after a local change.

## Wildcards

Wildcards inject device/user attributes into supported fields. Their spelling, applicability, availability and behavior differ by field and feature; check the linked official wildcard documentation before quoting a specific token. When passing values as script arguments, validate and quote them, handle missing values and avoid treating substituted content as executable code. Do not claim wildcards only work in scripts or that every script field substitutes them.

## Diagnosing pending or failed execution

1. Capture platform/version, enrollment and agent state, mechanism, target, intended trigger, last check-in, action status, timestamps and any error/output.
2. If queued/pending, check target membership, online/connectivity, prerequisite agent, schedule or trigger and whether the relevant event has occurred. An applied policy alone is not proof that its script ran. If startup is configured, compare policy association and last startup; do not present restart as the only possible cause.
3. If failed, inspect exit code and output, interpreter/arguments, privileges, OS compatibility, command paths, execution context and network dependencies. Verify the script locally under an equivalent account when possible.
4. If status says success, still verify intended device state and any dependent API/console update. Report partial success explicitly and test safe re-execution.

## Rename workflow

First decide whether the user wants an OS name, Hexnode friendly name, or both. OS naming rules vary: validate character set and length before applying and reserve enough unique identifier characters instead of truncating the end. On Windows, allow for restart before verifying the OS name. For console updates, a central integration can list all device pages, match exactly and refuse zero/multiple matches; update the friendly name and verify it independently. Do not assume the device is on the first page or report complete success when a required step fails.
