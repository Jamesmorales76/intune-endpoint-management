# macOS Defender network filter profile

Exported from the Intune console. Tenant IDs, keys, GUIDs and organization-specific values are redacted.

\<?xml version="1.0" encoding="UTF-8"?\>

\<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd"\>

\<plist version="1"\>

\<dict\>

\<key\>PayloadUUID\</key\>

\<string\>[REDACTED-GUID]\</string\>

\<key\>PayloadType\</key\>

\<string\>Configuration\</string\>

\<key\>PayloadOrganization\</key\>

\<string\>Microsoft Corporation\</string\>

\<key\>PayloadIdentifier\</key\>

\<string\>com.microsoft.wdav.webcontentfilter\</string\>

\<key\>PayloadDisplayName\</key\>

\<string\>Defender - Network Filter\</string\>

\<key\>PayloadDescription\</key\>

\<string/\>

\<key\>PayloadVersion\</key\>

\<integer\>1\</integer\>

\<key\>PayloadEnabled\</key\>

\<true/\>

\<key\>PayloadRemovalDisallowed\</key\>

\<true/\>

\<key\>PayloadScope\</key\>

\<string\>System\</string\>

\<key\>PayloadContent\</key\>

\<array\>

\<dict\>

\<key\>FilterDataProviderBundleIdentifier\</key\>

\<string\>com.microsoft.wdav.netext\</string\>

\<key\>FilterDataProviderDesignatedRequirement\</key\>

\<string\>identifier "com.microsoft.wdav.netext" and anchor apple generic and certificate 1\[field.1.2.840.113635.100.6.2.6\] /\* exists \*/ and certificate leaf\[field.1.2.840.113635.100.6.1.13\] /\* exists \*/ and certificate leaf\[subject.OU\] = UBF8T346G9\</string\>

\<key\>FilterGrade\</key\>

\<string\>inspector\</string\>

\<key\>FilterPackets\</key\>

\<false/\>

\<key\>FilterSockets\</key\>

\<true/\>

\<key\>FilterType\</key\>

\<string\>Plugin\</string\>

\<key\>PayloadDisplayName\</key\>

\<string\>Web Content Filter Payload\</string\>

\<key\>PayloadIdentifier\</key\>

\<string\>[REDACTED-GUID]\</string\>

\<key\>PayloadOrganization\</key\>

\<string\>JAMF Software\</string\>

\<key\>PayloadType\</key\>

\<string\>com.apple.webcontent-filter\</string\>

\<key\>PayloadUUID\</key\>

\<string\>[REDACTED-GUID]\</string\>

\<key\>PayloadVersion\</key\>

\<integer\>1\</integer\>

\<key\>PluginBundleID\</key\>

\<string\>com.microsoft.wdav\</string\>

\<key\>UserDefinedName\</key\>

\<string\>Microsoft Defender Content Filter\</string\>

\</dict\>

\</array\>

\</dict\>

\</plist\>
