# Enrollment and platforms

Hexnode's [enrollment overview](https://www.hexnode.com/uem/features/device-enrollment/) describes Apple ADE, Android zero-touch, Samsung Knox Mobile Enrollment, Windows Autopilot, ROM-based Android, self-enrollment and QR enrollment. Support for a specific feature is not guaranteed by the platform name alone: check hardware, OS version, enrollment state, license, integrations and platform documentation. Source review: 2026-11-13.

## Choose the management model

1. Establish whether the device is corporate-owned or personal, who uses it, whether it is shared, and which data and controls are required.
2. Check whether it is new, already configured or managed by another MDM. Determine whether changing enrollment requires a reset, user participation, reassigning an organizational portal or removing existing management; do not assume reset is always required.
3. Confirm identity and provider prerequisites, licensing, network access and the target platform's supported OS versions. Build a pilot with a reversible path and document user impact.
4. Enroll, check that the device reports correctly, assign pilot groups and policies, then verify each expected result on the endpoint and in Hexnode.

## Apple: iOS/iPadOS and macOS

- For eligible corporate devices, Automated Device Enrollment connects Apple Business Manager (ABM) or Apple School Manager (ASM), device assignment and Hexnode enrollment profiles. Check supervision and whether a setup/reset is necessary for the specific device state. Apple supervision is not equivalent to Android Device Owner.
- For BYOD, evaluate supported User Enrollment and account-driven options, their privacy boundary, account requirements and reduced management scope. Choose device enrollment when full device management is appropriate.
- Check APNs certificate and ABM/ASM tokens, assignment, renewal, network reachability and the actual profile state when diagnosing enrollment or policy delivery. Apple enrollment and push do not depend on assuming the same agent architecture as desktop scripting.
- macOS scripts, FileVault escrow, PPPC/TCC, system extensions and software updates have separate OS and enrollment requirements. Verify the relevant control and recovery-key access on a pilot.

Sources: [iOS enrollment](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/ios-enrolling-devices/), [macOS enrollment](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/macos-enrolling-devices/), [ABM integration](https://www.hexnode.com/mobile-device-management/help/hexnode-integrations/apple-business-manager/), [macOS security](https://www.hexnode.com/mobile-device-management/help/managing-mac-devices/security-macos/).

## Android and Android Enterprise

Distinguish a work profile from a fully managed corporate device, and verify the exact Android Enterprise mode and ownership before recommending restrictions, app installation, kiosk or scripts. Android zero-touch and Samsung Knox Mobile Enrollment are provisioning methods; check eligible models, reseller/portal configuration and setup state. An OEM-specific integration or OEMConfig may be needed for particular device controls; never infer device-owner privileges or root access from enrollment alone.

Sources: [Android Enterprise enrollment](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/android-enterprise-enrolling-devices/), [Android Enterprise app management](https://www.hexnode.com/mobile-device-management/help/managing-android-enterprise-devices/app-management/), [OEMConfig](https://www.hexnode.com/mobile-device-management/help/managing-android-enterprise-devices/oemconfig/), [Android scripts](https://www.hexnode.com/mobile-device-management/help/run-script-on-android/).

## Windows

Check OS edition and version, identity join and enrollment state before prescribing a policy or Autopilot workflow. Validate device assignment and enrollment integration, then inspect MDM and agent status as applicable. BitLocker, Defender, updates, kiosk and LAPS have distinct prerequisites; don't assume that all features are present on Home or all Windows Server editions. `Rename-Computer` generally needs a restart for the new OS name to take effect; distinguish that from the Hexnode friendly name.

Sources: [Windows enrollment](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/windows-enrolling-devices/), [edition comparison](https://www.hexnode.com/mobile-device-management/help/managing-windows-devices/edition-wise-feature-comparison/), [Windows server](https://www.hexnode.com/mobile-device-management/help/secure-windows-server/windows-server-management/).

## Linux, ChromeOS, tvOS, visionOS and Zebra

- **Linux:** verify distribution/version and agent requirements for the actual feature; Hexnode documents policies, Bash execution, remote view and live terminal, not just scripting. [Linux enrollment](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/linux/) · [Linux configuration](https://www.hexnode.com/mobile-device-management/help/managing-linux-devices/configurations-managing-linux-devices/)
- **ChromeOS:** check Google Workspace integration and the supported management scope. [ChromeOS enrollment](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/chromeos/) · [managed guest session](https://www.hexnode.com/mobile-device-management/help/managing-chromeos-devices/managed-guest-session/)
- **tvOS and visionOS:** consult their platform-specific enrollment and restrictions; do not reuse iPhone or Mac procedures without checking. [tvOS](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/tvos-enrolling-devices/) · [visionOS](https://www.hexnode.com/mobile-device-management/help/enrolling-devices/visionos/)
- **Zebra printers:** Link-OS printer management is distinct from Android Zebra handheld management. Check compatible printer models, enrollment, network and supported commands. [Zebra printers](https://www.hexnode.com/mobile-device-management/help/managing-zebra-printers/overview/)
- **Android TV and Fire OS:** check their particular supported capabilities rather than treating them as interchangeable with phones. [Android TV](https://www.hexnode.com/mobile-device-management/help/managing-android-devices/android-tv/) · [Fire OS](https://www.hexnode.com/uem/platform/fire-os/)

## Migration

Inventory devices, ownership, OS versions, existing enrollment, policies, apps and identities. Map controls and enrollment methods individually; confirm management removal and ABM/ASM or zero-touch ownership transfer requirements before touching devices. Pilot representative devices and document rollback, communication, recovery keys and service dependencies. Verify successful enrollment and policy results before expanding. See the [Hexnode migration framework](https://www.hexnode.com/mobile-device-management/help/migration-framework/migrate-to-hexnode/).
