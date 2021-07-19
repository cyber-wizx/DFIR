# Investigation notes
Malwares were caught in **_C:\Windows\Temp_** folder with the naming convention **_<10 digits>.<6-7 digits>.dll_**

Various threat names were found, including Hacktool, etc

They are found to be remnants of the Insecure Deserialization vulnerability in Telerik Web UI
- CVE-2019-18935
- CVE-2017-11317

The whole exploitation sequence includes known earlier CVE **_CVE-2017-11317 (Unrestricted File Upload via Weak Encryption)_** to upload payloads, followed by **_CVE-2019-18935 (Remote Code Execution via Insecure Deserialization)_** to perform a RCE.

## 1. Locating vulnerable TelerikUI dll
Locate the file named **_Telerik.Web.UI.dll_** in the affected system, and verify if its version is affected by both the CVEs.

## 2. Patching the vulnerable TelerikUI dll
Removing the vulnerable dll file if they are not in used, otherwise patching should be done against the whole Telerik application. You would probably consider performing a final round of validation to search for any existence of the vulnerable Telerik dll in case the dll file are located in orphan folders.

# Malware Analysis
https://github.com/cyber-wizx/MARE/blob/main/Analyzing_TelerikUI_Deserialization_Remnant.md

# Reference
https://labs.bishopfox.com/tech-blog/cve-2019-18935-remote-code-execution-in-telerik-ui
https://www.cvedetails.com/cve/CVE-2017-11317/
https://www.cvedetails.com/cve/CVE-2019-18935/
