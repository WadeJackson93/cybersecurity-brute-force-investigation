# Splunk Process Creation

``` spl
index=windows EventCode=4688
| table _time Account_Name New_Process_Name Process_Command_Line
| sort -_time
```

## Administrative Activity

``` spl
index=windows EventCode=4688
(New_Process_Name="*powershell.exe*" OR New_Process_Name="*cmd.exe*" OR New_Process_Name="*net.exe*" OR New_Process_Name="*arp.exe*")
| table _time Account_Name New_Process_Name Process_Command_Line Creator_Process_Name
```
