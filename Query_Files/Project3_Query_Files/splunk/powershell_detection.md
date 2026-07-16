# Splunk PowerShell Detection

``` spl
index=windows EventCode=1 Image="*powershell.exe*"
| table _time host User Image CommandLine ParentImage
| sort -_time
```
