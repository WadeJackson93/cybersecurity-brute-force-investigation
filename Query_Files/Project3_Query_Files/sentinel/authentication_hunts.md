# Microsoft Sentinel Authentication Hunts

``` kusto
SecurityEvent
| where EventID==4625
| project TimeGenerated,Account,Computer,IpAddress
```

``` kusto
SecurityEvent
| where EventID==4624
| project TimeGenerated,Account,Computer,IpAddress
```
