
## Get-Process

```
PS C:\Users\test> Get-Help -Parameter * Get-Process

-ComputerName <String[]>
    Gets the processes running on the specified computers. The default is the local computer.

    Type the NetBIOS name, an IP address, or a fully qualified domain name of one or more computers. To specify the
    local computer, type the computer name, a dot (.), or "localhost".

    This parameter does not rely on Windows PowerShell remoting. You can use the ComputerName parameter of Get-Process
    even if your computer is not configured to run remote commands.

    Required?                    false
    Position?                    named
    Default value                Local computer
    Accept pipeline input?       True (ByPropertyName)
    Accept wildcard characters?  false


-FileVersionInfo [<SwitchParameter>]
    Gets the file version information for the program that runs in the process.

    On Windows Vista and later versions of Windows, you must open Windows PowerShell with the "Run as administrator"
    option to use this parameter on processes that you do not own.

    You cannot use the FileVersionInfo and ComputerName parameters of the Get-Process cmdlet in the same command. To
    get file version information for a process on a remote computer, use the Invoke-Command cmdlet.

    Using this parameter is equivalent to getting the MainModule.FileVersionInfo property of each process object. When
    you use this parameter, Get-Process returns a FileVersionInfo object (System.Diagnostics.FileVersionInfo), not a
    process object. So, you cannot pipe the output of the command to a cmdlet that expects a process object, such as
    Stop-Process.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Id <Int32[]>
    Specifies one or more processes by process ID (PID). To specify multiple IDs, use commas to separate the IDs. To
    find the PID of a process, type "get-process".

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       True (ByPropertyName)
    Accept wildcard characters?  false


-IncludeUserName [<SwitchParameter>]
    Specifies that the UserName value of the Process object is returned with results of the command.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-InputObject <Process[]>
    Specifies one or more process objects. Enter a variable that contains the objects, or type a command or expression
    that gets the objects.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       True (ByValue)
    Accept wildcard characters?  false


-Module [<SwitchParameter>]
    Gets the modules that have been loaded by the processes.

    On Windows Vista and later versions of Windows, you must open Windows PowerShell with the "Run as administrator"
    option to use this parameter on processes that you do not own.

    You cannot use the Module and ComputerName parameters of the Get-Process cmdlet in the same command. To get the
    modules that have been loaded by a process on a remote computer, use the Invoke-Command cmdlet.

    This parameter is equivalent to getting the Modules property of each process object. When you use this parameter,
    Get-Process returns a ProcessModule object (System.Diagnostics.ProcessModule), not a process object. So, you
    cannot pipe the output of the command to a cmdlet that expects a process object, such as Stop-Process.

    When you use both the Module and FileVersionInfo parameters in the same command, Get-Process returns a
    FileVersionInfo object with information about the file version of all modules.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Name <String[]>
    Specifies one or more processes by process name. You can type multiple process names (separated by commas) and use
    wildcard characters. The parameter name ("Name") is optional.

    Required?                    false
    Position?                    1
    Default value
    Accept pipeline input?       True (ByPropertyName)
    Accept wildcard characters?  true
```

## How to use Get-Process ?

```
PS C:\Users\test> Get-Process

Handles  NPM(K)    PM(K)      WS(K) VM(M)   CPU(s)     Id ProcessName
-------  ------    -----      ----- -----   ------     -- -----------
    114       4    14988      13932    40     0.12   3692 audiodg
     52       3     1672       6356    46     0.16    908 conhost
     33       2      632       2272    30     0.00   3516 conhost
     95       4     2560      12432    73     0.50   3540 conhost
    488       6     1360       3064    31             360 csrss
    205       8     9484       3656    38             412 csrss
    195       8     2988       6516    36            2160 dllhost
    115       6    56424      49972   129     0.36   3368 dwm
    639      21    17864      28340   145     0.95   3428 explorer
      0       0        0         24     0               0 Idle
    739      12     2968       7032    29             516 lsass
    146       4     1088       2604    14             524 lsm
     97       5     7396       9844    53            3084 mscorsvw
    154       9     2516       4552    40            2432 msdtc
     57       3      972       4080    55     0.03   2176 notepad
    339      15    54852      27940   199     1.95    912 powershell
    391      17    57300      67356   208     2.39   2280 powershell
    119       5     3036       6532    47             620 SearchFilterHost
    735      21    26264      30620   174            3580 SearchIndexer
    326       6     4140       6044    47            2608 SearchProtocolHost
    220       7     3548       5092    30             504 services
     75       5      968       3376    38            1548 SLadmin
    289       9     2664       3992    44            1612 SLSmtp
     29       1      220        744     3             272 smss
    367      13     8484       9876    81            1360 spoolsv
    409      24    50560      18068   222             304 svchost
    353       7     2592       5756    31             628 svchost
    290       8     2512       5008    24             720 svchost
    471      11    14484      11436    53             820 svchost
    457      11    41868      43932   109             892 svchost
    538      11     4584       6908    51             940 svchost
   1230     103   105216      69500   207             976 svchost
    465      15     8128       9628    52            1268 svchost
    102       7     1228       3604    22            1296 svchost
    307      25     7788       6568    49            1396 svchost
    268       9     3660       5716    61            1492 svchost
    120       7     1136       3924    20            2508 svchost
    558       0       56       1788     3               4 System
     75       3      912       3656    21            2284 taskeng
    221      11     7404       7824    74     0.08   3308 taskhost
    120       5     3528       5896   105            1712 TorchCrashHandler
    121       5     1952       6620    73     0.06   3508 TPAutoConnect
    139       6     1984       5164    53             328 TPAutoConnSvc
    215       7    14056      19308    92            3292 TrustedInstaller
     86       5     4820       3908    48            1736 VGAuthService
     54       3      812       2960    32             688 vmacthlp
    339      12     7372      11620    72            1768 vmtoolsd
    265      12    12176      11848   110     1.90   3672 vmtoolsd
     74       5      928       3020    29             404 wininit
    121       5     1588       4644    46             448 winlogon
    208       7     5780      10416    35            1660 WmiPrvSE
    250       7    19832      11900    48            2804 WmiPrvSE
```

**-FileVersionInfo**

```
PS C:\Users\test> Get-Process -FileVersionInfo notepad

ProductVersion   FileVersion      FileName
--------------   -----------      --------
6.1.7600.16385   6.1.7600.1638... C:\Windows\system32\notepad.exe
```

**-Id**

```
PS C:\Users\test> Get-Process -id 2176

Handles  NPM(K)    PM(K)      WS(K) VM(M)   CPU(s)     Id ProcessName
-------  ------    -----      ----- -----   ------     -- -----------
     57       3      972       4080    55     0.03   2176 notepad
```

**-IncludeUserName**

```
PS C:\Users\test> Get-Process -IncludeUserName notepad
Get-Process : The 'IncludeUserName' parameter requires elevated user rights. Try running the command again in a session that has been opened with elevated user ri
At line:1 char:1
+ Get-Process -IncludeUserName notepad
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (:) [Get-Process], InvalidOperationException
    + FullyQualifiedErrorId : IncludeUserNameRequiresElevation,Microsoft.PowerShell.Commands.GetProcessCommand
```

Try to start powershell with administratora rights,

```
PS C:\Windows\system32> Get-Process -IncludeUserName notepad

Handles      WS(K) VM(M)   CPU(s)     Id UserName          ProcessName
-------      ----- -----   ------     -- --------          -----------
     57       4080    55     0.03   2176 lab\test          notepad
```

**-Module**

```
PS C:\Users\test> Get-Process notepad -Module

   Size(K) ModuleName                                         FileName
   ------- ----------                                         --------
       192 notepad.exe                                        C:\Windows\system32\notepad.exe
      1288 ntdll.dll                                          C:\Windows\SYSTEM32\ntdll.dll
       852 kernel32.dll                                       C:\Windows\system32\kernel32.dll
       300 KERNELBASE.dll                                     C:\Windows\system32\KERNELBASE.dll
       644 ADVAPI32.dll                                       C:\Windows\system32\ADVAPI32.dll
       688 msvcrt.dll                                         C:\Windows\system32\msvcrt.dll
       100 sechost.dll                                        C:\Windows\SYSTEM32\sechost.dll
       648 RPCRT4.dll                                         C:\Windows\system32\RPCRT4.dll
       312 GDI32.dll                                          C:\Windows\system32\GDI32.dll
       804 USER32.dll                                         C:\Windows\system32\USER32.dll
        40 LPK.dll                                            C:\Windows\system32\LPK.dll
       628 USP10.dll                                          C:\Windows\system32\USP10.dll
       492 COMDLG32.dll                                       C:\Windows\system32\COMDLG32.dll
       348 SHLWAPI.dll                                        C:\Windows\system32\SHLWAPI.dll
      1656 COMCTL32.dll                                       C:\Windows\WinSxS\x86_microsoft.windows.common-controls_6595b64144ccf1df_6.0.7601.18837_none_41e855142bd5705d\COMCTL32.dll
     12592 SHELL32.dll                                        C:\Windows\system32\SHELL32.dll
       324 WINSPOOL.DRV                                       C:\Windows\system32\WINSPOOL.DRV
      1396 ole32.dll                                          C:\Windows\system32\ole32.dll
       580 OLEAUT32.dll                                       C:\Windows\system32\OLEAUT32.dll
        36 VERSION.dll                                        C:\Windows\system32\VERSION.dll
       124 IMM32.DLL                                          C:\Windows\system32\IMM32.DLL
       816 MSCTF.dll                                          C:\Windows\system32\MSCTF.dll
        48 CRYPTBASE.dll                                      C:\Windows\system32\CRYPTBASE.dll
       256 uxtheme.dll                                        C:\Windows\system32\uxtheme.dll
        76 dwmapi.dll                                         C:\Windows\system32\dwmapi.dll
```

**-Name**

```
PS C:\Users\test> Get-Process -Name powershell

Handles  NPM(K)    PM(K)      WS(K) VM(M)   CPU(s)     Id ProcessName
-------  ------    -----      ----- -----   ------     -- -----------
    334      15    57612      44772   199     2.00    912 powershell
    405      17    55740      65868   208     2.45   2280 powershell
```
