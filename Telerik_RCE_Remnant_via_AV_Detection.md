# Investigation notes
Malwares were caught in **_C:\Windows\Temp_** folder with the naming convention **_<10 digits>.<6-7 digits>.dll_**

Various threat names were found, including Hacktool, etc

They are found to be remnants of the Insecure Deserialization vulnerability in Telerik Web UI
- CVE-2019-18935
- CVE-2017-11317

The whole exploitation sequence includes known earlier CVE **_CVE-2017-11317 (Unrestricted File Upload via Weak Encryption)_** to upload payloads, followed by **_CVE-2019-18935 (Remote Code Execution via Insecure Deserialization)_** to perform a RCE.

# Reference
https://labs.bishopfox.com/tech-blog/cve-2019-18935-remote-code-execution-in-telerik-ui
