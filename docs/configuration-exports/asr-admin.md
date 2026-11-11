# Attack Surface Reduction: admin policy

Exported from the Intune console. Tenant IDs, keys, GUIDs and organization-specific values are redacted.

### **Configuration settings**

#### **Settings**

#### **Attack Surface Reduction Rules**

Block persistence through WMI event subscription

Block

Block credential stealing from the Windows local security authority subsystem (lsass.exe)

Enable

Block Adobe Reader from creating child processes

Enable

Block Office applications from injecting code into other processes

Warn

Block Office applications from creating executable content

Warn

Block all Office applications from creating child processes

Warn

Block Win32 API calls from Office macro

Block

Block Office communication apps from creating child processes

Enable

Block execution of potentially obfuscated scripts (js/vbs/ps)

Warn

Block JavaScript or VBScript from launching downloaded executable content

Block

Block process creations originating from PSExec and WMI commands

Block

Block untrusted and unsigned processes that run from USB

Block

Block executable files from running unless they meet a prevalence, age, or trusted list criteria

Warn

Block executable content download from email and webmail clients

Block

Use advanced protection against ransomware

Enable

Enable folder protection

Enable

List of additional folders that need to be protected

0 items

- Add

- Import

- Export

- Sort

- Delete

> Additional guarded folders

NO ITEMS

List of apps that have access to protected folders

0 items

- Add

- Import

- Export

- Sort

- Delete

> Allowed app paths

NO ITEMS

Exclude files and paths from attack surface reduction rules

4 items

- Add

- Import

- Export

- Sort

- Delete

> Path
>
> %localappdata%\Mail Manager\Program Files
>
> %localappdata%\Mail Manager\Program Files\Support
>
> %localappdata%\Mail Manager\Program Files\x64
>
> %localappdata%\Mail Manager\Program Files\x86
