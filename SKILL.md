---
name: hexnode-mdm
description: Work with Hexnode UEM/MDM including enrollment, policies, automation, scripting, API integrations, wildcards, apps, kiosk, compliance, troubleshooting and migration. Use whenever a task involves Hexnode, including Apple, Android, Windows, Linux, ChromeOS, and Zebra devices, or when comparing or migrating MDM platforms to or from Hexnode.
---

# Hexnode UEM/MDM

Help users plan, configure, integrate, troubleshoot and operate Hexnode. Answer in the user's language. Prefer concrete steps, prerequisites, verification and relevant source links over generic feature lists.

## Workflow

1. Identify the desired result, platform and OS version, ownership/BYOD, enrollment method and supervision or Android Enterprise mode. For scripts, identify the execution mechanism and desired trigger. For API questions, distinguish reading, changing a resource and initiating an action.
2. Ask only for missing details that affect the answer; otherwise state reasonable assumptions. Availability can depend on plan, tenant, role, OS, edition, agent, integration and enrollment. Never imply every feature works on every platform.
3. Read the relevant reference below. Check linked official documentation when web access is available for current capabilities, exact UI labels, API schemas, limits and OS requirements. State when something could not be verified. Prefer current official documentation and tenant evidence over historical notes.
4. Give platform-specific steps, prerequisites, expected outcome and verification. Distinguish a policy assigned/applied from an asynchronous action or script actually succeeding. Troubleshoot through targeted checks, not one assumed cause.
5. For deployments, scope targets, test on a pilot device/group, inspect per-device outcomes and plan recovery before expansion. Do not claim a script, API operation or deployment was tested unless it actually was.

## References

Read only the relevant file, relative to this skill directory:

- [API and integrations](references/api.md): authentication, pagination, policy and automation endpoints, request examples, webhooks and error handling.
- [Enrollment and platforms](references/platforms.md): Apple, Android Enterprise, Windows, Linux, ChromeOS, tvOS, visionOS, Zebra, and migration.
- [Scripts, automation and troubleshooting](references/automation.md): choosing a mechanism, Android scripting, wildcards, execution context, secrets, diagnostics and renaming.
- [Policies, apps and operations](references/operations.md): app management, kiosk, compliance, conditional access, patching, certificates, RBAC and integrations.

`references/legacy-skill.md`, `API_REFERENCE.md`, `HEXNODE_API_COMPLETE.md` and `hexnode_api_complete_docs.json` are historical material, not authoritative operational guidance. The legacy skill contains known errors and unsafe examples; verify any material recovered from these files against current official documentation.

## Principles

- List policies using the documented `GET /api/v1/policy/`. Don't infer undocumented endpoints or assume a 404 proves an entire feature is unavailable. The API can list and initiate existing automations.
- Hexnode documents Android scripting as well as Windows, macOS and Linux scripting; eligibility and privileges are device- and mechanism-specific. Do not promise unrestricted shell/root access or iOS script execution.
- Policies and automations can overlap. Policy scripts can have execution schedules, and Automate can bundle and target actions. Choose based on the actual trigger, prerequisites and tenant options; verify enrollment trigger support for the specific mechanism.
- Never embed a tenant API key in a script or package distributed to endpoints. Prefer a trusted central integration using managed secrets and appropriately scoped access. Environment variables are not automatically secret storage; verify each mechanism's handling.
- Check pagination and reject ambiguous device matches. Distinguish the Hexnode friendly name from the OS hostname, and report local and console updates separately. Avoid fixed timing, guaranteed success rates and universal runtime assumptions.
