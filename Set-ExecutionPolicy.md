
## Set-ExecutionPolicy

```
PS C:\Windows\system32> Get-Help -Parameter * Set-ExecutionPolicy

-ExecutionPolicy <ExecutionPolicy>
    Specifies the new execution policy. Valid values are:

    -- Restricted: Does not load configuration files or run scripts. "Restricted" is the default execution policy.

    -- AllSigned: Requires that all scripts and configuration files be signed by a trusted publisher, including scripts that you write on the local computer.

    -- RemoteSigned: Requires that all scripts and configuration files downloaded from the Internet be signed by a trusted publisher.

    -- Unrestricted: Loads all configuration files and runs all scripts. If you run an unsigned script that was downloaded from the Internet, you are prompted for permission before it runs.

    -- Bypass: Nothing is blocked and there are no warnings or prompts.

    -- Undefined: Removes the currently assigned execution policy from the current scope. This parameter will not remove an execution policy that is set in a Group Policy scope.

    Required?                    true
    Position?                    1
    Default value                None
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false


-Force [<SwitchParameter>]
    Suppresses all prompts. By default, Set-ExecutionPolicy displays a warning whenever you change the execution policy.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Scope <ExecutionPolicyScope>
    Specifies the scope of the execution policy. The default is LocalMachine.

    Valid values are:

    -- Process: The execution policy affects only the current Windows PowerShell process.

    -- CurrentUser: The execution policy affects only the current user.

    -- LocalMachine: The execution policy affects all users of the computer.

    To remove an execution policy from a particular scope, set the execution policy for that scope to Undefined.

    When the value of the Scope parameter is Process, the execution policy is saved in the PSExecutionPolicyPreference environment variable ($env:PSExecutionPolicyPreference), instead of the registry, and the variable is deleted when the process is closed. You cannot change the execution policy of
    the process by editing the variable.

    Required?                    false
    Position?                    2
    Default value                LocalMachine
    Accept pipeline input?       true (ByPropertyName)
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

```
PS C:\Windows\system32> Set-ExecutionPolicy -Force -ExecutionPolicy Bypass
```

**Demo**

Please put PowerSploit AntivirusBypass into

```
PS C:\Windows\system32> $env:PSModulePath
C:\Users\test\Documents\WindowsPowerShell\Modules;C:\Program Files\WindowsPowerShell\Modules;C:\Windows\system32\WindowsPowerShell\v1.0\Modules\
```

```
PS C:\Windows\system32> Get-ChildItem -Path C:\Users\test\Documents\WindowsPowerShell\Modules\AntivirusBypass


    Directory: C:\Users\test\Documents\WindowsPowerShell\Modules\AntivirusBypass


Mode                LastWriteTime     Length Name
----                -------------     ------ ----
-a---        10/14/2016   9:48 AM        844 AntivirusBypass.psd1
-a---        10/14/2016   9:48 AM         67 AntivirusBypass.psm1
-a---        10/14/2016   9:47 AM       6583 Find-AVSignature.ps1

```

```
powershell -Command "Set-ExecutionPolicy -Force -ExecutionPolicy Bypass;Import-Module -Force AntivirusBypass;Get-Command -Module AntivirusBypass"
```
