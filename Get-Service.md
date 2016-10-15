
## Get-Service

```
PS C:\Users\test> Get-Help -Parameter * Get-Service

-ComputerName <String[]>
    Gets the services running on the specified computers. The default is the local computer.

    Type the NetBIOS name, an IP address, or a fully qualified domain name of a remote computer. To specify the local computer, type the computer name, a dot (.), or "localhost".

    This parameter does not rely on Windows PowerShell remoting. You can use the ComputerName parameter of Get-Service even if your computer is not configured to run remote commands.

    Required?                    false
    Position?                    named
    Default value                Local computer
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-DependentServices [<SwitchParameter>]
    Gets only the services that depend upon the specified service.

    By default, Get-Service gets all services.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-DisplayName <String[]>
    Specifies the display names of services to be retrieved. Wildcards are permitted. By default, Get-Service gets all services on the computer.

    Required?                    true
    Position?                    named
    Default value                All services
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Exclude <String[]>
    Omits the specified services. The value of this parameter qualifies the Name parameter. Enter a name element or pattern, such as "s*". Wildcards are permitted.

    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Include <String[]>
    Retrieves only the specified services. The value of this parameter qualifies the Name parameter. Enter a name element or pattern, such as "s*". Wildcards are permitted.

    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  true


-InputObject <ServiceController[]>
    Specifies ServiceController objects representing the services to be retrieved. Enter a variable that contains the objects, or type a command or expression that gets the objects. You can also pipe a service object to Get-Service.

    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false


-Name <String[]>
    Specifies the service names of services to be retrieved. Wildcards are permitted. By default, Get-Service gets all of the services on the computer.

    Required?                    false
    Position?                    1
    Default value                All services
    Accept pipeline input?       true (ByPropertyName, ByValue)
    Accept wildcard characters?  true


-RequiredServices [<SwitchParameter>]
    Gets only the services that this service requires.

    This parameter gets the value of the ServicesDependedOn property of the service. By default, Get-Service gets all services.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false
```

**-DependentServices**

```
PS C:\Users\test> Get-Service -DependentServices AudioEndpointBuilder

Status   Name               DisplayName
------   ----               -----------
Running  Audiosrv           Windows Audio
```

**-DisplayName**

```
PS C:\Users\test> Get-Service -DependentServices AudioEndpointBuilder

Status   Name               DisplayName
------   ----               -----------
Running  Audiosrv           Windows Audio


PS C:\Users\test> Get-Service -DisplayName A*

Status   Name               DisplayName
------   ----               -----------
Stopped  AeLookupSvc        Application Experience
Stopped  ALG                Application Layer Gateway Service
Running  AppHostSvc         Application Host Helper Service
Stopped  AppIDSvc           Application Identity
Running  Appinfo            Application Information
Stopped  AppMgmt            Application Management
Stopped  aspnet_state       ASP.NET State Service
Stopped  AxInstSV           ActiveX Installer (AxInstSV)
Stopped  SensrSvc           Adaptive Brightness

```

**-Include**

```
PS C:\Users\test> Get-Service -Include A*

Status   Name               DisplayName
------   ----               -----------
Running  AeLookupSvc        Application Experience
Stopped  ALG                Application Layer Gateway Service
Running  AppHostSvc         Application Host Helper Service
Stopped  AppIDSvc           Application Identity
Running  Appinfo            Application Information
Stopped  AppMgmt            Application Management
Stopped  aspnet_state       ASP.NET State Service
Running  AudioEndpointBu... Windows Audio Endpoint Builder
Running  Audiosrv           Windows Audio
Stopped  AxInstSV           ActiveX Installer (AxInstSV)
```

**-RequiredServices**

```
PS C:\Users\test> Get-Service -RequiredServices SharedAccess

Status   Name               DisplayName
------   ----               -----------
Running  BFE                Base Filtering Engine
Stopped  RasMan             Remote Access Connection Manager
Running  Netman             Network Connections
Running  WinMgmt            Windows Management Instrumentation
```

**How to get Running services ?**

```
PS C:\Users\test> Get-Service | Sort-Object Status
```

```
PS C:\Users\test> Get-Service | where-object {$_.Status -eq "Running"}

Status   Name               DisplayName
------   ----               -----------
Running  AppHostSvc         Application Host Helper Service
Running  Appinfo            Application Information
Running  AudioEndpointBu... Windows Audio Endpoint Builder
Running  Audiosrv           Windows Audio
Running  BFE                Base Filtering Engine
Running  BITS               Background Intelligent Transfer Ser...
Running  Browser            Computer Browser
Running  clr_optimizatio... Microsoft .NET Framework NGEN v4.0....
Running  CryptSvc           Cryptographic Services
Running  CscService         Offline Files
Running  DcomLaunch         DCOM Server Process Launcher
Running  Dhcp               DHCP Client
Running  DiagTrack          Diagnostics Tracking Service
Running  Dnscache           DNS Client
Running  DPS                Diagnostic Policy Service
Running  eventlog           Windows Event Log
Running  EventSystem        COM+ Event System
Running  FontCache          Windows Font Cache Service
Running  gpsvc              Group Policy Client
Running  IKEEXT             IKE and AuthIP IPsec Keying Modules
Running  iphlpsvc           IP Helper
Running  LanmanServer       Server
Running  LanmanWorkstation  Workstation
Running  lmhosts            TCP/IP NetBIOS Helper
Running  MpsSvc             Windows Firewall
Running  MSDTC              Distributed Transaction Coordinator
Running  Netman             Network Connections
Running  netprofm           Network List Service
Running  NlaSvc             Network Location Awareness
Running  nsi                Network Store Interface Service
Running  PcaSvc             Program Compatibility Assistant Ser...
Running  PlugPlay           Plug and Play
Running  PolicyAgent        IPsec Policy Agent
Running  Power              Power
Running  ProfSvc            User Profile Service
Running  RpcEptMapper       RPC Endpoint Mapper
Running  RpcSs              Remote Procedure Call (RPC)
Running  SamSs              Security Accounts Manager
Running  Schedule           Task Scheduler
Running  SENS               System Event Notification Service
Running  ShellHWDetection   Shell Hardware Detection
Running  Spooler            Print Spooler
Running  SSDPSRV            SSDP Discovery
Running  SysMain            Superfetch
Running  Themes             Themes
Running  TorchCrashHandler  Torch Crash Handler
Running  TPAutoConnSvc      TP AutoConnect Service
Running  TrkWks             Distributed Link Tracking Client
Running  UxSms              Desktop Window Manager Session Manager
Running  VGAuthService      VMware Alias Manager and Ticket Ser...
Running  VMTools            VMware Tools
Running  VMware Physical... VMware Physical Disk Helper Service
Running  WdiServiceHost     Diagnostic Service Host
Running  WinDefend          Windows Defender
Running  Winmgmt            Windows Management Instrumentation
Running  wscsvc             Security Center
Running  WSearch            Windows Search
Running  wuauserv           Windows Update
Running  wudfsvc            Windows Driver Foundation - User-mo...
```
