# Policy inventory

Counts of the 166 configuration profiles in the tenant, grouped by capability. Names are generalized; organization-specific and vendor-branded profiles are not listed individually.

## By platform

| Platform | Profiles |
|---|---:|
| Windows | 104 |
| macOS | 54 |
| iOS/iPadOS | 4 |
| Android Enterprise | 4 |

## By capability

| Capability | Profiles |
|---|---:|
| Disk encryption and device protection | 39 |
| Microsoft 365 apps, browsers and updates | 35 |
| Other (kiosk/test, printing, misc.) | 29 |
| Microsoft Defender for Endpoint and ASR | 26 |
| Certificates and trusted roots | 19 |
| Network, Wi-Fi and VPN | 15 |
| Identity and SSO | 3 |

## Naming convention

Profiles use a consistent `Platform - Scope - Function` pattern (for example `macOS - Device - Sys - FileVault`) with prefix characters that sort production baselines, test profiles and deprecated profiles into separate groups in the console.
