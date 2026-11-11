# Attack Surface Reduction: rules

Exported from the Intune console. Tenant IDs, keys, GUIDs and organization-specific values are redacted.

### **Configuration settings**

#### **Settings**

#### **Attack Surface Reduction Rules**

Block persistence through WMI event subscription

Block

Block credential stealing from the Windows local security authority subsystem (lsass.exe)

Warn

Block Adobe Reader from creating child processes

Enable

Block Office applications from injecting code into other processes

Warn

Block Office applications from creating executable content

Warn

Block all Office applications from creating child processes

Block

Block Win32 API calls from Office macro

Audit mode

Block Office communication apps from creating child processes

Audit mode

Block execution of potentially obfuscated scripts (js/vbs/ps)

Audit mode

Block JavaScript or VBScript from launching downloaded executable content

Block

Block process creations originating from PSExec and WMI commands

Block

Block untrusted and unsigned processes that run from USB

Block

Block executable files from running unless they meet a prevalence, age, or trusted list criteria

Audit mode

Block executable content download from email and webmail clients

Block

Use advanced protection against ransomware

Enable

Enable folder protection

Audit mode

List of additional folders that need to be protected

0 items

List of apps that have access to protected folders

0 items

Exclude files and paths from attack surface reduction rules

2 items

- Add

- Import

- Export

- Sort

- Delete

> Path
>
> \*\*\PulseSecureAppLauncher.msi
>
> C:\Windows\System32\wbem\WmiPrvSE.exe
