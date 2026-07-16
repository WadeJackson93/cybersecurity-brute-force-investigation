# Device Process Hunts

``` kusto
DeviceProcessEvents
| where FileName =~ "powershell.exe"
```

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has_any ("whoami /priv","whoami /groups")
```

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has "net localgroup administrators"
```
