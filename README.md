# Intune: Enterprise Endpoint Management and Privileged Access

A complete Microsoft Intune environment I designed, built and secured, covering **Windows, macOS, iOS, Android and Linux**, with Entra **PIM** for least-privilege administration.

This repo documents the architecture, the security controls and how the pieces fit together. Screenshots are cropped to the settings panes; tenant names and IDs, GUIDs, keys, domains, user and device identifiers, and internal URLs have been removed or blacked out.

## Scope at a glance

| Area | What was built |
|---|---|
| Configuration profiles | **166** across Windows (104), macOS (54), iOS/iPadOS (4), Android Enterprise (4) |
| Compliance policies | Windows, macOS, iOS 15 to 18, Android (BYOD and corporate), Linux |
| Endpoint security | Defender for Endpoint, Attack Surface Reduction, Application Control, Account Protection, LAPS, Web Protection |
| Enrollment | Windows Autopilot (user-driven, Entra joined, pre-provisioning, device name template) |
| Privileged access | Entra PIM: **148** role assignments across **34** roles, **75** eligible and **73** active |

## What was built

### 1. Compliance, per platform
Compliance policies define "healthy" for each OS and mark devices noncompliant on a schedule, with end-user email notifications and retire actions on mobile.

- **Windows**: minimum OS builds (Windows 10 22H2, Windows 11 23H2 and 24H2), BitLocker, Secure Boot and code integrity, TPM, firewall, antivirus and antispyware, UAC settings, and Defender for Endpoint machine risk score
- **macOS**: minimum OS and build, system integrity protection, disk encryption, firewall
- **iOS/iPadOS**: minimum OS versions for 15 through 18, jailbreak detection, password requirements
- **Android Enterprise**: separate BYOD (work profile) and corporate-owned policies; root detection, Play Integrity, encryption, password complexity
- **Linux**: allowed distributions, device encryption, password policy

### 2. Hardened device configuration
- **Windows baseline and hardening**: UAC consent on the secure desktop with an admin-elevation workflow, BitLocker on removable drives, Application Guard, SmartScreen, Microsoft Store controls, RDP redirection restrictions (separate profiles for physical and virtual machines), Office macro blocking
- **macOS**: FileVault with key escrow and rotation, Platform SSO (Secure Enclave key) with Entra ID, privacy preferences policy control (PPPC), system extensions, managed login items, notifications, Microsoft AutoUpdate, Edge extension control
- **iOS**: SSO app extension for Microsoft Entra ID

### 3. Endpoint security
- **Microsoft Defender for Endpoint**: connector setup across platforms, onboarding, antivirus, cloud-delivered protection, network protection
- **Attack Surface Reduction** rule sets, with exclusions managed separately from rules
- **Application Control** and **Web Protection**
- **Windows LAPS** with 30-day rotation, 20-character complex passwords and post-authentication reset
- **Account Protection** profile for Windows Hello for Business and Credential Guard settings

### 4. Patching
Windows Autopatch rings for Windows and Office with separate Broad, Fast, First and Test groups, plus Edge update channels.

### 5. Privileged access with PIM
Admin roles are **eligible by default** and activated just in time, so standing privilege is minimized. Most privileged-role assignments are eligible rather than active (Privileged Role Administrator, Conditional Access Administrator and Exchange Administrator are eligible-only; 3 of 5 Global Administrator assignments are eligible). See [PIM role assignments](docs/pim-role-assignments.md) for the per-role breakdown.

## Design principles

- **Least privilege**: eligible rather than permanent role assignment; local admin handled through LAPS and an elevation workflow rather than standing rights
- **Consistent naming**: `Platform - Scope - Function`, with prefixes grouping baselines, test and deprecated profiles
- **Baseline plus feature profiles**: a base profile per platform with feature-specific profiles (Defender, FileVault, SSO, updates) kept separate
- **Graduated noncompliance actions**: devices are marked noncompliant, the user is emailed, and mobile devices are added to the retire list after a grace period
- **Test before production**: separate test profiles and update rings

## Contents

- [Policy inventory](docs/policy-inventory.md)
- [PIM role assignments](docs/pim-role-assignments.md)
- Configuration exports (scrubbed of GUIDs, tenant IDs and keys): [Windows baseline](docs/configuration-exports/windows-baseline.md), [Windows Defender](docs/configuration-exports/windows-defender.md), [Defender baseline](docs/configuration-exports/defender-baseline.md), [ASR rules](docs/configuration-exports/asr-rules.md), [ASR admin policy](docs/configuration-exports/asr-admin.md), [browser extension control](docs/configuration-exports/windows-browser-extensions.md), [macOS Defender network filter](docs/configuration-exports/macos-defender-network-filter.md)

### Screenshots

**Compliance**
- [android byod](screenshots/compliance/android-byod.png)
- [android corp](screenshots/compliance/android-corp.png)
- [linux device encryption](screenshots/compliance/linux-device-encryption.png)
- [linux distros](screenshots/compliance/linux-distros.png)
- [linux password policy](screenshots/compliance/linux-password-policy.png)
- [macos](screenshots/compliance/macos.png)
- [macos baseline](screenshots/compliance/macos-baseline.png)
- [windows atp threat](screenshots/compliance/windows-atp-threat.png)
- [windows antivirus](screenshots/compliance/windows-antivirus.png)
- [windows bit locker](screenshots/compliance/windows-bit-locker.png)
- [windows firewall](screenshots/compliance/windows-firewall.png)
- [windows os](screenshots/compliance/windows-os.png)
- [windows secure boot](screenshots/compliance/windows-secure-boot.png)
- [windows spyware](screenshots/compliance/windows-spyware.png)
- [windows tpm](screenshots/compliance/windows-tpm.png)
- [windows user access control](screenshots/compliance/windows-user-access-control.png)
- [ios 15](screenshots/compliance/ios-15.png)
- [ios 16](screenshots/compliance/ios-16.png)
- [ios 17](screenshots/compliance/ios-17.png)
- [ios 18](screenshots/compliance/ios-18.png)
- [ios password policy](screenshots/compliance/ios-password-policy.png)

**Device configuration**
- [macos allow user login items and extensions](screenshots/device-configuration/macos-macos-allow-user-login-items-and-extensions.png)
- [macos baseline](screenshots/device-configuration/macos-macos-baseline.png)
- [macos baseline 2](screenshots/device-configuration/macos-macos-baseline-2.png)
- [macos bluetooth access](screenshots/device-configuration/macos-macos-bluetooth-access.png)
- [macos defender cnfig](screenshots/device-configuration/macos-macos-defender-cnfig.png)
- [macos edge extensions](screenshots/device-configuration/macos-macos-edge-extensions.png)
- [macos filevault](screenshots/device-configuration/macos-macos-filevault.png)
- [macos full disk access](screenshots/device-configuration/macos-macos-full-disk-access.png)
- [macos full disk access 2](screenshots/device-configuration/macos-macos-full-disk-access-2.png)
- [macos microsoft updates](screenshots/device-configuration/macos-macos-microsoft-updates.png)
- [macos netfilter defender](screenshots/device-configuration/macos-macos-netfilter-defender.png)
- [macos platform sso config](screenshots/device-configuration/macos-macos-platform-sso-config.png)
- [macos sys accessibility](screenshots/device-configuration/macos-macos-sys-accessibility.png)
- [macos sys background services](screenshots/device-configuration/macos-macos-sys-background-services.png)
- [macos sys notifications](screenshots/device-configuration/macos-macos-sys-notifications.png)
- [macos sys system extensions](screenshots/device-configuration/macos-macos-sys-system-extensions.png)
- [windows admin by request baseline](screenshots/device-configuration/windows-admin-by-request-baseline.png)
- [windows admin by request consent secure desktop](screenshots/device-configuration/windows-admin-by-request-consent-secure-desktop.png)
- [windows admin by request password on secure desktop](screenshots/device-configuration/windows-admin-by-request-password-on-secure-desktop.png)
- [windows application guard](screenshots/device-configuration/windows-application-guard.png)
- [windows bitlocker removeable drives](screenshots/device-configuration/windows-bitlocker-removeable-drives.png)
- [windows bitlocker removable drives baseline](screenshots/device-configuration/windows-bitlocker-removable-drives-baseline.png)
- [windows defender block macro](screenshots/device-configuration/windows-defender-block-macro.png)
- [windows edge smartscreen](screenshots/device-configuration/windows-edge-smartscreen.png)
- [windows microsoft store allow](screenshots/device-configuration/windows-microsoft-store-allow.png)
- [windows microsoft store block](screenshots/device-configuration/windows-microsoft-store-block.png)
- [windows office configuration autopatch](screenshots/device-configuration/windows-office-configuration-autopatch.png)
- [windows rdp settings physical device](screenshots/device-configuration/windows-rdp-settings-physical-device.png)
- [windows rdp settings virtual device](screenshots/device-configuration/windows-rdp-settings-virtual-device.png)
- [windows smartscreen off](screenshots/device-configuration/windows-smartscreen-off.png)
- [windows smartscreen on](screenshots/device-configuration/windows-smartscreen-on.png)
- [windows user atp](screenshots/device-configuration/windows-user-atp.png)
- [windows 10 laps](screenshots/device-configuration/windows-windows-10-laps.png)
- [ios sso config](screenshots/device-configuration/ios-sso-config.png)
- [macos onedrive config](screenshots/device-configuration/macos-onedrive-config.png) (GUIDs redacted)
- [macos defender onboarding](screenshots/device-configuration/macos-defender-onboarding.png) (GUIDs redacted)

**Endpoint security**
- [account protection](screenshots/endpoint-security/account-protection.png)
- [defender for endpoint setup](screenshots/endpoint-security/defender-for-endpoint-setup.png)
- [laps](screenshots/endpoint-security/laps.png)
- [application control](screenshots/endpoint-security/application-control.png)
- [web protection legacy](screenshots/endpoint-security/web-protection-legacy.png)

**Enrollment**
- [windows](screenshots/enrollment/windows.png)

## Tech

Microsoft Intune, Microsoft Entra ID, Entra PIM, Microsoft Defender for Endpoint, Windows Autopilot, Windows Autopatch, Windows LAPS, BitLocker, FileVault, Platform SSO
