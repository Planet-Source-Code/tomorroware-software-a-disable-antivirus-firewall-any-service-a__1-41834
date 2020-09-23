<div align="center">

## A\+ \*\*Disable Antivirus, Firewall, any service\!\*\*\* A\+


</div>

### Description

This simple code will disable any service on the local machine, good to use to disable a firewall so your app can access the web to check for pirate serial without the user knowing etc, it will also start a service. To find a servicename goto Control Panel > Administrator Tools > Services..
 
### More Info
 
The ServiceName of a service you wish to END / START

Service Name!

Disables service, or starts one.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tomorroware Software](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tomorroware-software.md)
**Level**          |Beginner
**User Rating**    |4.0 (91 globes from 23 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Windows System Services](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/windows-system-services__1-35.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tomorroware-software-a-disable-antivirus-firewall-any-service-a__1-41834/archive/master.zip)

### API Declarations

None!


### Source Code

```
Private Sub Command1_Click()
'stops Norton Antivirus
StopService "Norton Antivirus Auto Protect Service"
End Sub
Private Sub Command2_Click()
'starts antivirus
StartService "Norton Antivirus Auto Protect Service"
End Sub
Sub StopService(ServiceName As String)
a = """" & ServiceName & """"
'uses the NET STOP function to stop the service
Shell "net stop " & a, vbHide
End Sub
Sub StartService(ServiceName As String)
a = """" & ServiceName & """"
'uses the NET START function to start the service
Shell "net start " & a, vbHide
End Sub
```

