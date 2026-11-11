# Defender baseline

Exported from the Intune console. Tenant IDs, keys, GUIDs and organization-specific values are redacted.

### **Configuration settings**

#### **Settings**

#### **Attack Surface Reduction Rules**

Block Office communication apps from creating child processes

Enable

Block Adobe Reader from creating child processes

Enable

Block Office applications from injecting code into other processes

Block

Block Office applications from creating executable content

Block

Block JavaScript or VBScript from launching downloaded executable content

Block

Enable network protection

Enable

Block untrusted and unsigned processes that run from USB

Warn

Block credential stealing from the Windows local security authority subsystem (lsass.exe)

Warn

Block executable content download from email and webmail clients

Block

Block all Office applications from creating child processes

Warn

Block execution of potentially obfuscated scripts (js/vbs/ps)

Warn

Block Win32 API calls from Office macro

Warn

#### **BitLocker**

BitLocker system drive policy

- Configure

  > Not configured

Startup authentication required

- Yes

  > Not configured

Compatible TPM startup PIN

Not configured

Compatible TPM startup key

Not configured

Disable BitLocker on devices where TPM is incompatible

- Yes

  > Not configured

Configure encryption method for Operating System drives

Not configured

Standby states when sleeping while on battery

Enabled

Standby states when sleeping while plugged in

Enabled

Enable Full disk or Used Space only encryption for OS and fixed data drives

- Yes

  > Not configured

BitLocker fixed drive policy

- Configure

  > Not configured

Block write access to fixed data-drives not protected by BitLocker

- Yes

  > Not configured

Configure encryption method for fixed data-drives

AES 128bit XTS

BitLocker removable drive policy

- Configure

  > Not configured

Configure encryption method for removable data-drives

AES 128bit CBC

Block write access to removable data-drives not protected by BitLocker

- Yes

  > Not configured

#### **Device Guard**

Turn on Credential Guard

Enable with UEFI lock

#### **Device Installation**

Block hardware device installation by setup classes

Yes

Remove matching hardware devices

- Yes

  > Not configured

Block list

1 item

#### **DMA Guard**

Enumeration of external devices incompatible with Kernel DMA Protection

Block all

#### **Firewall**

Stateful File Transfer Protocol (FTP)

Disabled

Number of seconds a security association can be idle before it's deleted

Preshared key encoding

UTF8

Certificate revocation list (CRL) verification

Not configured

Packet queuing

Not configured

Firewall profile private

- Configure

  > Not configured

Inbound connections blocked

- Yes

  > Not configured

Unicast responses to multicast broadcasts required

- Yes

  > Not configured

Outbound connections required

- Yes

  > Not configured

Inbound notifications blocked

- Yes

  > Not configured

Global port rules from group policy merged

- Yes

  > Not configured

Firewall enabled

Allowed

Authorized application rules from group policy not merged

- Yes

  > Not configured

Connection security rules from group policy not merged

- Yes

  > Not configured

Incoming traffic required

- Yes

  > Not configured

Policy rules from group policy not merged

- Yes

  > Not configured

Firewall profile public

- Configure

  > Not configured

Inbound connections blocked

- Yes

  > Not configured

Unicast responses to multicast broadcasts required

- Yes

  > Not configured

Outbound connections required

- Yes

  > Not configured

Authorized application rules from group policy merged

- Yes

  > Not configured

Inbound notifications blocked

- Yes

  > Not configured

Global port rules from group policy merged

- Yes

  > Not configured

Firewall enabled

Allowed

Connection security rules from group policy not merged

- Yes

  > Not configured

Incoming traffic required

- Yes

  > Not configured

Policy rules from group policy not merged

- Yes

  > Not configured

Firewall profile domain

- Configure

  > Not configured

Unicast responses to multicast broadcasts required

- Yes

  > Not configured

Authorized application rules from group policy merged

- Yes

  > Not configured

Inbound notifications blocked

- Yes

  > Not configured

Global port rules from group policy merged

- Yes

  > Not configured

Firewall enabled

Allowed

Connection security rules from group policy not merged

- Yes

  > Not configured

Policy rules from group policy not merged

- Yes

  > Not configured

#### **Microsoft Defender**

Turn on real-time protection

- Yes

  > Not configured

Additional amount of time (0-50 seconds) to extend cloud protection timeout

Scan all downloaded files and attachments

- Yes

  > Not configured

Scan type

Quick scan

Defender schedule scan day

Everyday

Scheduled scan start time

Not configured

Defender sample submission consent

Send safe samples automatically

Cloud-delivered protection level

Not configured

Scan removable drives during full scan

- Yes

  > Not configured

Defender potentially unwanted app action

Block

Turn on cloud-delivered protection

- Yes

  > Not configured

#### **Smart Screen**

Block users from ignoring SmartScreen warnings

- Yes

  > Not configured

Turn on Windows SmartScreen

- Yes

  > Not configured

Require SmartScreen for Microsoft Edge Legacy

- Yes

  > Not configured

Block malicious site access

- Yes

  > Not configured

Block unverified file download

- Yes

  > Not configured

Configure Microsoft Defender SmartScreen

Enabled

Prevent bypassing Microsoft Defender SmartScreen prompts for sites

Not configured

Prevent bypassing of Microsoft Defender SmartScreen warnings about downloads

Not configured

Configure Microsoft Defender SmartScreen to block potentially unwanted apps

Not configured
