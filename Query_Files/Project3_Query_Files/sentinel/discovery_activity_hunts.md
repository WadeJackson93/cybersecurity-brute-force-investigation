# Discovery Activity Hunts

## Host Discovery

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has "hostname"
```

## Process Discovery

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has "tasklist"
```

## Network Configuration

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has "ipconfig"
```

## Network Connections

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has "netstat"
```

## Logged-on Users

``` kusto
DeviceProcessEvents
| where ProcessCommandLine has "query user"
```
