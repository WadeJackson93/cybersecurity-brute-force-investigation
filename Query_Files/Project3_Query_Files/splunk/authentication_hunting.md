# Splunk Authentication Hunting

## Failed Logons

``` spl
index=windows EventCode=4625
| table _time host Account_Name Source_Network_Address Logon_Type
| sort -_time
```

## Successful Logons

``` spl
index=windows EventCode=4624
| table _time host Account_Name Source_Network_Address Logon_Type
| sort -_time
```

## Failed Logon Statistics

``` spl
index=windows EventCode=4625
| stats count by Account_Name
| sort -count
```
