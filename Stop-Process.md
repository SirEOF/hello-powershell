
## Stop-Process

```
PS C:\Users\test> Get-Help -Parameter * Stop-Process

-Force [<SwitchParameter>]
    Stops the specified processes without prompting for confirmation. By default, Stop-Process prompts for
    confirmation before stopping any process that is not owned by the current user.

    To find the owner of a process, use the Get-WmiMethod cmdlet to get a Win32_Process object that represents the
    process, and then use the GetOwner method of the object.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Id <Int32[]>
    Specifies the process IDs of the processes to be stopped. To specify multiple IDs, use commas to separate the IDs.
    To find the PID of a process, type "get-process". The parameter name ("Id") is optional.

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-InputObject <Process[]>
    Stops the processes represented by the specified process objects. Enter a variable that contains the objects, or
    type a command or expression that gets the objects.

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false


-Name <String[]>
    Specifies the process names of the processes to be stopped. You can type multiple process names (separated by
    commas) or use wildcard characters.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  true


-PassThru [<SwitchParameter>]
    Returns an object representing the process. By default, this cmdlet does not generate any output.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Confirm [<SwitchParameter>]
    Prompts you for confirmation before running the cmdlet.

    Required?                    false
    Position?                    named
    Default value                false
    Accept pipeline input?       false
    Accept wildcard characters?  false


-WhatIf [<SwitchParameter>]
    Shows what would happen if the cmdlet runs. The cmdlet is not run.

    Required?                    false
    Position?                    named
    Default value                false
    Accept pipeline input?       false
    Accept wildcard characters?  false


```

**-Id**

```
PS C:\Users\test> Start-Process -PassThru notepad -WindowStyle Hidden

Handles  NPM(K)    PM(K)      WS(K) VM(M)   CPU(s)     Id ProcessName
-------  ------    -----      ----- -----   ------     -- -----------
      0       1      288         80     2     0.00   2836 notepad


PS C:\Users\test> Stop-Process -Id 2836
```

**-Name**

```
PS C:\Users\test> Stop-Process -Name notepad
```

**-Confirm**

```
PS C:\Users\test> Get-Process -Name notepad

Handles  NPM(K)    PM(K)      WS(K) VM(M)   CPU(s)     Id ProcessName
-------  ------    -----      ----- -----   ------     -- -----------
     57       3      972       3488    55     0.03   2176 notepad
     57       3      984       4152    64     0.00   3320 notepad


PS C:\Users\test> Get-Process -Name notepad | Stop-Process -Confirm

Confirm
Are you sure you want to perform this action?
Performing the operation "Stop-Process" on target "notepad (2176)".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): A
```

**Stop-Process + Get-Process**

```
PS C:\>get-process notepad | stop-process
```
