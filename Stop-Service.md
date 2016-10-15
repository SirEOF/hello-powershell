
## Stop-Service

```
PS C:\Users\test> Get-Help -Parameter * Stop-Service

-DisplayName <String[]>
    Specifies the display names of the services to be stopped. Wildcards are permitted.

    Required?                    true
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Exclude <String[]>
    Omits the specified services. The value of this parameter qualifies the Name parameter. Enter a name element or pattern, such as "s*". Wildcards are permitted.

    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Force [<SwitchParameter>]
    Allows the cmdlet to stop a service even if that service has dependent services.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Include <String[]>
    Stops only the specified services. The value of this parameter qualifies the Name parameter. Enter a name element or pattern, such as "s*". Wildcards are permitted.

    Required?                    false
    Position?                    named
    Default value                
    Accept pipeline input?       false
    Accept wildcard characters?  true


-InputObject <ServiceController[]>
    Specifies ServiceController objects representing the services to be stopped. Enter a variable that contains the objects, or type a command or expression that gets the objects.

    Required?                    true
    Position?                    1
    Default value                
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false


-Name <String[]>
    Specifies the service names of the services to be stopped. Wildcards are permitted.

    The parameter name is optional. You can use "Name" or its alias, "ServiceName", or you can omit the parameter name.

    Required?                    true
    Position?                    1
    Default value                
    Accept pipeline input?       true (ByPropertyName, ByValue)
    Accept wildcard characters?  true


-PassThru [<SwitchParameter>]
    Returns an object representing the service. By default, this cmdlet does not generate any output.

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

**-Name**

```
PS C:\Windows\system32> Stop-Service -Name "WSearch"
```

or

```
PS C:\Windows\system32> Get-Service -Name WSearch | Stop-Service
```

**-DisplayName**

```
PS C:\Windows\system32> Stop-Service -DisplayName "Windows Search"
```

**-Force**

```
PS C:\Windows\system32> Stop-Service -Name "WSearch"
```

**-Confirm**

```
PS C:\Windows\system32> Stop-Service -Confirm -Name WSearch

Confirm
Are you sure you want to perform this action?
Performing the operation "Stop-Service" on target "Windows Search (WSearch)".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): Y
```
