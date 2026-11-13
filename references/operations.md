# Policies, apps, security and operations

Source review: 2026-11-13. Use these as starting points; feature specifics depend on tenant, plan, device platform, enrollment and version.

## Policies and targeting

Policies collect settings that can be assigned to devices, users and groups. A device can receive multiple policies; check conflicts and actual effective state rather than assuming all assigned settings apply. Start with a small target group, validate on-device results, then expand. UI policy support may exceed the [policy API schemas](https://www.hexnode.com/mobile-device-management/developers/policies/create-policy/). Source: [policy setup](https://www.hexnode.com/mobile-device-management/help/policy-management/set-up-policies/).

## Apps and kiosk

Choose the application source, assignment, licensing, installation/update behavior and managed configuration for the platform. Hexnode documents catalogs, app bundles, allow/block lists and mandatory apps; confirm exact behavior and silent-install prerequisites for the enrollment method. For Apple, check Apps and Books licenses/token; for Android Enterprise, check managed Google Play and work-profile scope; for desktop packages, check installer type, architecture and dependencies. [App management](https://www.hexnode.com/uem/features/app-management/) · [app troubleshooting](https://www.hexnode.com/mobile-device-management/help/deploying-and-managing-apps/troubleshoot/).

For kiosk, identify platform, single/multi-app or web use case, required apps/sites, permissions, connectivity and exit/recovery path. Test authentication, updates, reboot and offline recovery on a pilot. Supervision, Android Enterprise mode or OS edition may affect the available options; do not assume all kiosk modes exist for every OS. [Kiosk platform guides](https://www.hexnode.com/mobile-device-management/help/kiosk-lockdown-of-devices/ios-kiosk-lockdown-of-devices/).

## Compliance and access

Separate detection rules, noncompliance status, remediation and conditional access. Determine the signal source and freshness, grace period, user experience and the behavior for offline devices. Microsoft Entra conditional access requires the relevant integration and device registration; verify current licensing and supported platforms. Test compliant, noncompliant and recovery cases before broad enforcement. [Compliance rules](https://www.hexnode.com/mobile-device-management/help/endpoint-compliance/compliance-rules/) · [Entra integration](https://www.hexnode.com/mobile-device-management/help/conditional-access/integrate-entra-id/) · [registration and enforcement](https://www.hexnode.com/mobile-device-management/help/conditional-access/register-devices-enforce-compliance/).

## Updates and security controls

Plan patch rings, maintenance windows, reboot requirements, reporting and rollback. Treat OS updates, third-party app patches and OS-specific restrictions as distinct capabilities. [Patch overview](https://www.hexnode.com/mobile-device-management/help/patches-and-updates/overview-concepts/) · [Windows](https://www.hexnode.com/mobile-device-management/help/patches-and-updates/windows-patch-update-management/) · [Apple](https://www.hexnode.com/mobile-device-management/help/patches-and-updates/apple-software-update-management/) · [Linux](https://www.hexnode.com/mobile-device-management/help/patches-and-updates/linux-patch-and-update-management/).

For encryption and certificates, distinguish deployment from verified endpoint state. Check FileVault/BitLocker prerequisites, escrow, authorization to recover keys, renewal/revocation and failure recovery. Check certificate identity and SCEP or integration requirements per use case. Hexnode documents [certificate management](https://www.hexnode.com/uem/features/automated-certificate-management/) and [macOS LAPS](https://www.hexnode.com/mobile-device-management/help/managing-mac-devices/laps/); verify per-platform capabilities and access controls.

## Other capabilities worth considering

- [RBAC and technician roles](https://www.hexnode.com/mobile-device-management/help/technicians/technician-roles/): scope administrator access to operational need.
- [Integrations](https://www.hexnode.com/uem/features/mdm-integrations/): identity and service-management integrations; confirm the particular integration's events and permissions. [Webhooks](https://www.hexnode.com/mobile-device-management/help/hexnode-integrations/webhooks/) may support event-driven workflows.
- [Reports](https://www.hexnode.com/mobile-device-management/help/reports/hexnode-reports-reports/), inventory and [asset management](https://www.hexnode.com/mobile-device-management/help/asset-management/overview-asset-management/): identify freshness and coverage before using data for compliance decisions.
- [Hexnode Gateway](https://www.hexnode.com/uem/features/hexnode-gateway/), [Hexnode Access](https://www.hexnode.com/uem/features/hexnode-access/) and [Genie AI](https://www.hexnode.com/uem/features/hexnode-genie/) address different onboarding, access and AI-assisted workflows. Check actual entitlements and documentation; do not assume these are enabled in a tenant.
