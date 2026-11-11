# Windows baseline settings

Exported from the Intune console. Tenant IDs, keys, GUIDs and organization-specific values are redacted.

### **Configuration settings**

#### **Administrative Templates**

**MS Security Guide**

Apply UAC restrictions to local accounts on network logons

Enabled

Configure SMB v1 client driver

Enabled

> Configure MrxSmb10 driver
>
> Disable driver (recommended)

Configure SMB v1 server

Disabled

**MSS (Legacy)**

MSS: (DisableIPSourceRouting IPv6) IP source routing protection level (protects against packet spoofing)

Enabled

> DisableIPSourceRoutingIPv6 (Device)
>
> Highest protection, source routing is completely disabled

MSS: (DisableIPSourceRouting) IP source routing protection level (protects against packet spoofing)

Enabled

> DisableIPSourceRouting (Device)
>
> Highest protection, source routing is completely disabled

**Printers**

Allow Print Spooler to accept client connections

Disabled

**Windows Components \> Windows Remote Management (WinRM) \> WinRM Service**

Allow Basic authentication

Disabled

Allow CredSSP authentication

Disabled

Allow remote server management through WinRM

Disabled

Allow unencrypted traffic

Disabled

Disallow Kerberos authentication

Disabled

Disallow Negotiate authentication

Disabled

Disallow WinRM from storing RunAs credentials

Enabled

Specify channel binding token hardening level

Disabled

Turn On Compatibility HTTP Listener

Disabled

Turn On Compatibility HTTPS Listener

Disabled

**Windows Components \> Windows Remote Management (WinRM) \> WinRM Client**

Allow unencrypted traffic

Disabled

Disallow Digest authentication

Disabled

Disallow Kerberos authentication

Disabled

Disallow Negotiate authentication

Disabled

Trusted Hosts

Disabled

**Windows Components \> Remote Desktop Services \> Remote Desktop Session Host \> Security**

Require user authentication for remote connections by using Network Level Authentication

Enabled

**Windows Components \> Internet Explorer**

Prevent bypassing SmartScreen Filter warnings about files that are not commonly downloaded from the Internet

Disabled

Prevent bypassing SmartScreen Filter warnings about files that are not commonly downloaded from the Internet (User)

Disabled

**Windows Components \> Internet Explorer \> Security Features \> Add-on Management**

Turn off blocking of outdated ActiveX controls for Internet Explorer

Disabled

Turn off blocking of outdated ActiveX controls for Internet Explorer (User)

Disabled

**Windows Components \> Internet Explorer \> Internet Control Panel \> Advanced Page**

Allow software to run or install even if the signature is invalid

Disabled

Allow software to run or install even if the signature is invalid (User)

Disabled

Check for signatures on downloaded programs

Enabled

Check for signatures on downloaded programs (User)

Enabled

**Windows Components \> Credential User Interface**

Enumerate administrator accounts on elevation

Disabled

**Windows Components \> BitLocker Drive Encryption**

Choose drive encryption method and cipher strength (Windows 10 \[Version 1511\] and later)

Enabled

> Select the encryption method for fixed data drives:
>
> XTS-AES 128-bit (default)
>
> Select the encryption method for operating system drives:
>
> XTS-AES 128-bit (default)
>
> Select the encryption method for removable data drives:
>
> AES-CBC 128-bit (default)

Provide the unique identifiers for your organization

Disabled

**Windows Components \> BitLocker Drive Encryption \> Fixed Data Drives**

Choose how BitLocker-protected fixed drives can be recovered

Enabled

> Allow 256-bit recovery key
>
> Configure user storage of BitLocker recovery information:
>
> Allow 48-digit recovery password
>
> Allow data recovery agent
>
> True
>
> Configure storage of BitLocker recovery information to AD DS:
>
> Backup recovery passwords and key packages
>
> Do not enable BitLocker until recovery information is stored to AD DS for fixed data drives
>
> True
>
> Omit recovery options from the BitLocker setup wizard
>
> True
>
> Save BitLocker recovery information to AD DS for fixed data drives
>
> True

Deny write access to fixed drives not protected by BitLocker

Enabled

Enforce drive encryption type on fixed data drives

Enabled

> Select the encryption type: (Device)
>
> Full encryption

**Windows Components \> BitLocker Drive Encryption \> Operating System Drives**

> Configure TPM startup key and PIN:
>
> Allow startup key and PIN with TPM
>
> Configure TPM startup:
>
> Allow TPM
>
> Allow BitLocker without a compatible TPM (requires a password or a startup key on a USB flash drive)
>
> True
>
> Configure TPM startup PIN:
>
> Allow startup PIN with TPM
>
> Configure TPM startup key:
>
> Allow startup key with TPM

Allow devices compliant with InstantGo or HSTI to opt out of pre-boot PIN.

Enabled

Allow enhanced PINs for startup

Enabled

Choose how BitLocker-protected operating system drives can be recovered

Enabled

> Allow 256-bit recovery key
>
> Configure user storage of BitLocker recovery information:
>
> Allow 48-digit recovery password
>
> Allow data recovery agent
>
> True
>
> Configure storage of BitLocker recovery information to AD DS:
>
> Store recovery passwords and key packages
>
> Do not enable BitLocker until recovery information is stored to AD DS for operating system drives
>
> True
>
> Omit recovery options from the BitLocker setup wizard
>
> True
>
> Save BitLocker recovery information to AD DS for operating system drives
>
> True

Configure minimum PIN length for startup

Disabled

Configure pre-boot recovery message and URL

Disabled

Disallow standard users from changing the PIN or password

Disabled

Enable use of BitLocker authentication requiring preboot keyboard input on slates

Disabled

Enforce drive encryption type on operating system drives

Enabled

> Select the encryption type: (Device)
>
> Full encryption

Require additional authentication at startup

Enabled

**Windows Components \> AutoPlay Policies**

> Turn off Autoplay on: (User)
>
> All drives

Disallow Autoplay for non-volume devices

Enabled

Disallow Autoplay for non-volume devices (User)

Enabled

Set the default behavior for AutoRun

Enabled

> Default AutoRun Behavior
>
> Do not execute any autorun commands

Set the default behavior for AutoRun (User)

Enabled

> Default AutoRun Behavior (User)
>
> Do not execute any autorun commands

Turn off Autoplay

Enabled

> Turn off Autoplay on:
>
> All drives

Turn off Autoplay (User)

Enabled

**System \> Remote Assistance**

Allow only Windows Vista or later connections

Disabled

Configure Offer Remote Assistance

Disabled

Configure Solicited Remote Assistance

Disabled

Customize warning messages

Disabled

Turn on bandwidth optimization

Disabled

Turn on session logging

Enabled

**System \> Device Installation \> Device Installation Restrictions**

> Prevented Classes
>
> {d48179be-ec20-11d1-b6b8-00c04fa372a7}
>
> Also apply to matching devices that are already installed.
>
> True

Allow administrators to override Device Installation Restriction policies

Enabled

Prevent installation of devices using drivers that match these device setup classes

Enabled

**Network \> Network Connections**

Prohibit use of Internet Connection Sharing on your DNS domain network

Enabled

Require domain users to elevate when setting a network's location

Enabled

#### **Authentication**

Enable Web Sign In

Enabled. Web Sign-in will be enabled for signing in to Windows

#### **BitLocker**

Allow Warning For Other Disk Encryption

Disabled

> Allow Standard User Encryption
>
> Enabled

#### **Browser**

Allow Password Manager

Block

Allow Password Manager (User)

Block

#### **Control Policy Conflict**

MDM Wins Over GP

The MDM policy is used and the GP policy is blocked.

#### **Delivery Optimization**

DO Allow VPN Peer Caching

Block

DO Download Mode

HTTP blended with peering behind the same NAT.

DO Restrict Peer Selection By

Subnet mask.

#### **Device Guard**

Credential Guard

(Enabled with UEFI lock) Turns on Credential Guard with UEFI lock.

#### **Device Health Monitoring**

Allow Device Health Monitoring

The DeviceHealthMonitoring connection is enabled.

#### **Device Lock**

Device Password Enabled

Enabled

> Allow Simple Device Password
>
> Not allowed.
>
> Alphanumeric Device Password Required
>
> Password, Numeric PIN, or Alphanumeric PIN required.
>
> Device Password Expiration
>
> 50
>
> Device Password History
>
> 24
>
> Max Device Password Failed Attempts
>
> 5
>
> Max Inactivity Time Device Lock
>
> 7
>
> Min Device Password Length
>
> 6

Minimum Password Age

1

#### **Dma Guard**

Device Enumeration Policy

Only after log in/screen unlock

#### **Firewall**

The Firewall configuration service provider configures the Windows Defender Firewall global settings, per profile settings, as well as the desired set of custom rules to be enforced on the device. Using the Firewall CSP the IT admin can now manage non-domain devices, and reduce the risk of network security threats across all systems connecting to the corporate network.

Disable Stateful Ftp

False

Enable Domain Network Firewall

True

> Allow Local Ipsec Policy Merge
>
> True
>
> Allow Local Policy Merge
>
> True
>
> Auth Apps Allow User Pref Merge
>
> True
>
> Default Inbound Action for Domain Profile
>
> Block
>
> Default Outbound Action
>
> Allow
>
> Disable Inbound Notifications
>
> True
>
> Disable Stealth Mode
>
> False
>
> Disable Stealth Mode Ipsec Secured Packet Exemption
>
> True
>
> Disable Unicast Responses To Multicast Broadcast
>
> False
>
> Global Ports Allow User Pref Merge
>
> True
>
> Shielded
>
> False

Enable Private Network Firewall

True

> Allow Local Ipsec Policy Merge
>
> False
>
> Allow Local Policy Merge
>
> False
>
> Auth Apps Allow User Pref Merge
>
> False
>
> Default Inbound Action for Private Profile
>
> Block
>
> Default Outbound Action
>
> Allow
>
> Disable Inbound Notifications
>
> True
>
> Disable Stealth Mode
>
> False
>
> Disable Stealth Mode Ipsec Secured Packet Exemption
>
> True
>
> Disable Unicast Responses To Multicast Broadcast
>
> False
>
> Global Ports Allow User Pref Merge
>
> True
>
> Shielded
>
> False

Enable Public Network Firewall

True

> Allow Local Ipsec Policy Merge
>
> False
>
> Allow Local Policy Merge
>
> False
>
> Auth Apps Allow User Pref Merge
>
> False
>
> Default Inbound Action for Public Profile
>
> Block
>
> Default Outbound Action
>
> Allow
>
> Disable Inbound Notifications
>
> True
>
> Disable Stealth Mode
>
> False
>
> Disable Stealth Mode Ipsec Secured Packet Exemption
>
> True
>
> Disable Unicast Responses To Multicast Broadcast
>
> False
>
> Global Ports Allow User Pref Merge
>
> True
>
> Shielded
>
> False

Preshared Key Encoding

UTF8

Security association idle time

300

#### **Google**

**Google Chrome**

Allow download restrictions

Enabled

> Download restrictions (Device)
>
> Block malicious downloads and dangerous file types.

Allow download restrictions (User)

Enabled

> Download restrictions (User)
>
> Block malicious downloads and dangerous file types.

Browser sign in settings

Enabled

> Browser sign in settings (Device)
>
> Disable browser sign-in

Browser sign in settings (User)

Enabled

> Browser sign in settings (User)
>
> Disable browser sign-in

Continue running background apps when Google Chrome is closed

Disabled

Controls the mode of DNS-over-HTTPS

Enabled

> Controls the mode of DNS-over-HTTPS (Device)
>
> Disable DNS-over-HTTPS

Controls the mode of DNS-over-HTTPS (User)

Enabled

> Controls the mode of DNS-over-HTTPS (User)
>
> Disable DNS-over-HTTPS

Enable third party software injection blocking

Enabled

**Google Chrome \> Password manager**

Enable leak detection for entered credentials

Enabled

Enable leak detection for entered credentials (User)

Enabled

Enable saving passwords to the password manager

Disabled

Enable saving passwords to the password manager (User)

Disabled

**Google Chrome \> Password manager**

Enable leak detection for entered credentials

Enabled

Enable leak detection for entered credentials (User)

Enabled

Enable saving passwords to the password manager

Disabled

Enable saving passwords to the password manager (User)

Disabled

**Google Chrome \> Startup Home page and New Tab page**

Configure the home page URL

Enabled

> Home page URL (Device)
>
> [REDACTED-URL]

Configure the home page URL (User)

Disabled

Configure the New Tab page URL

Enabled

> New Tab page URL (Device)
>
> [REDACTED-URL]

Configure the New Tab page URL (User)

Disabled

Use New Tab Page as homepage

Enabled

**Google Chrome - Default Settings users can override**

Block third party cookies (User)

Enabled

#### **Local Policies Security Options**

Accounts Enable Administrator Account Status

Disable

Accounts Enable Guest Account Status

Disable

Accounts Rename Administrator Account

FredFlintstone

Accounts Rename Guest Account

BarneyRubble

Interactive Logon Do Not Display Last Signed In

Disabled (username will be shown)

Interactive Logon Message Text For Users Attempting To Log On

[Organization-specific logon warning text removed]

Interactive Logon Message Title For Users Attempting To Log On

IMPORTANT NOTICE

Microsoft Network Client Digitally Sign Communications Always

Enable

Microsoft Network Client Digitally Sign Communications If Server Agrees

Enable

Microsoft Network Server Digitally Sign Communications Always

Enable

Microsoft Network Server Digitally Sign Communications If Client Agrees

Enable

Network Access Do Not Allow Anonymous Enumeration Of SAM Accounts

Enabled

Network Access Do Not Allow Anonymous Enumeration Of Sam Accounts And Shares

Enabled

Network Access Restrict Anonymous Access To Named Pipes And Shares

Enable

Network Security LAN Manager Authentication Level

Send LM and NTLMv2 responses only. Refuse LM and NTLM

#### **Microsoft Edge**

**Password manager and protection**

Allow users to be alerted if their passwords are found to be unsafe

Enabled

Allow users to be alerted if their passwords are found to be unsafe (User)

Enabled

Allow users to get a strong password suggestion whenever they are creating an account online

Disabled

Allow users to get a strong password suggestion whenever they are creating an account online (User)

Disabled

Configure password protection warning trigger

Enabled

> Configure password protection warning trigger (Device)
>
> Password protection warning is triggered by password reuse

Configure password protection warning trigger (User)

Enabled

> Configure password protection warning trigger (User)
>
> Password protection warning is triggered by password reuse

Enable saving passwords to the password manager

Disabled

Enable saving passwords to the password manager (User)

Disabled

**Startup, home page and new tab page**

> Set new tab page quick links (Device)
>
> [REDACTED-PINNED-SITES]

Configure the Microsoft Edge new tab page experience

Enabled

> New tab page experience (Device)
>
> Office 365 feed experience

Set new tab page quick links

Enabled

#### **Microsoft Office 2016**

**Shared paths**

> Workgroup templates path (User)
>
> C:\ProgramData\OfficeTemplates2020

Workgroup templates path (User)

Enabled

#### **OneDrive**

Block file downloads when users are low on disk space

Enabled

> Minimum available disk space: (Device)
>
> 200

Prevent users from redirecting their Windows known folders to their PC

Enabled

Silently move Windows known folders to OneDrive

Enabled

> Show notification to users after folders have been redirected: (Device)
>
> Yes
>
> Tenant ID: (Device)
>
> [REDACTED-GUID]

Silently sign in users to the OneDrive sync app with their Windows credentials

Enabled

Sync Admin Reports

Enabled

> Tenant Association Key: (Device)
>
> [REDACTED-KEY]

Use OneDrive Files On-Demand

Enabled

Warn users who are low on disk space

Enabled

> Minimum available disk space: (Device)
>
> 500

#### **Windows Hello For Business**

Use Security Key For Signin

Enabled

#### **Windows Logon**

------------------------------------------------------------------------

Enable First Logon Animation

Disabled
