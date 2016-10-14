## Get-Command

```
PS /> Get-Command -All *process*

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Function        Get-PSMetaConfigurationProcessed                   0.0        PSDesiredStateConfiguration
Function        Set-PSMetaConfigDocInsProcessedBeforeMeta          0.0        PSDesiredStateConfiguration
Cmdlet          Debug-Process                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Enter-PSHostProcess                                3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Exit-PSHostProcess                                 3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Process                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-PSHostProcessInfo                              3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Start-Process                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Stop-Process                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Wait-Process                                       3.1.0.0    Microsoft.PowerShell.Management
```

**-CommandType**


```
PS /> Get-Command -CommmandType Alias
PS /> Get-Command -CommmandType All
PS /> Get-Command -CommmandType Application
PS /> Get-Command -CommmandType Cmdlet
PS /> Get-Command -CommandType ExternalScript
PS /> Get-Command -CommandType Filter
PS /> Get-Command -CommandType Function
PS /> Get-Command -CommandType Script
PS /> Get-Command -CommandType Workflow
```

**-ShowCommandInfo**

```
PS /> Get-Command -ShowCommandInfo Get-Process


Name          : Get-Process
ModuleName    : Microsoft.PowerShell.Management
Module        : @{Name=Microsoft.PowerShell.Management}
CommandType   : Cmdlet
Definition    :
                Get-Process [[-Name] <string[]>] [-ComputerName <string[]>] [-Module] [-FileVersionInfo] [<CommonParameters>]

                Get-Process [[-Name] <string[]>] -IncludeUserName [<CommonParameters>]

                Get-Process -Id <int[]> [-ComputerName <string[]>] [-Module] [-FileVersionInfo] [<CommonParameters>]

                Get-Process -Id <int[]> -IncludeUserName [<CommonParameters>]

                Get-Process -InputObject <Process[]> [-ComputerName <string[]>] [-Module] [-FileVersionInfo] [<CommonParameters>]

                Get-Process -InputObject <Process[]> -IncludeUserName [<CommonParameters>]

ParameterSets : {@{Name=Name; IsDefault=True; Parameters=System.Management.Automation.PSObject[]}, @{Name=NameWithUserName; IsDefault=False;
                Parameters=System.Management.Automation.PSObject[]}, @{Name=Id; IsDefault=False; Parameters=System.Management.Automation.PSObject[]},
                @{Name=IdWithUserName; IsDefault=False; Parameters=System.Management.Automation.PSObject[]}...}

```

**-Syntax**

```
PS /> Get-Command -Syntax Get-Process

Get-Process [[-Name] <string[]>] [-ComputerName <string[]>] [-Module] [-FileVersionInfo] [<CommonParameters>]

Get-Process [[-Name] <string[]>] -IncludeUserName [<CommonParameters>]

Get-Process -Id <int[]> [-ComputerName <string[]>] [-Module] [-FileVersionInfo] [<CommonParameters>]

Get-Process -Id <int[]> -IncludeUserName [<CommonParameters>]

Get-Process -InputObject <Process[]> [-ComputerName <string[]>] [-Module] [-FileVersionInfo] [<CommonParameters>]

Get-Process -InputObject <Process[]> -IncludeUserName [<CommonParameters>]

```

**-ParameterName**

```
PS /> Get-Command -ParameterName Id

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Clear-History                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Connect-PSSession                                  3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Debug-Job                                          3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Debug-Process                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Debug-Runspace                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Disable-PSBreakpoint                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Disconnect-PSSession                               3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Enable-PSBreakpoint                                3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Enter-PSHostProcess                                3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Enter-PSSession                                    3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Event                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-EventSubscriber                                3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-History                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Job                                            3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Process                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-PSBreakpoint                                   3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-PSHostProcessInfo                              3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-PSSession                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Runspace                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Invoke-History                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Receive-Job                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Receive-PSSession                                  3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-Job                                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-PSBreakpoint                                3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Remove-PSSession                                   3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Stop-Job                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Stop-Process                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Wait-Job                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Wait-Process                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Write-Progress                                     3.1.0.0    Microsoft.PowerShell.Utility

```

**-ParameterType**


```
PS /> Get-Command -ParameterType a

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Remove-TypeData                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Update-TypeData                                    3.1.0.0    Microsoft.PowerShell.Utility


PS /> Get-Command -ParameterType i

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Connect-PSSession                                  3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Enter-PSSession                                    3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Module                                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-PSSession                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Import-Module                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Invoke-Command                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Invoke-RestMethod                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Invoke-WebRequest                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          New-ModuleManifest                                 3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-PSSession                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Receive-PSSession                                  3.0.0.0    Microsoft.PowerShell.Core


PS /> Get-Command -ParameterType b

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Cmdlet          Debug-Job                                          3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Receive-Job                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-Job                                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Stop-Job                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Wait-Job                                           3.0.0.0    Microsoft.PowerShell.Core

```

----

```
PS /> Get-Command

CommandType     Name                                               Version    Source
-----------     ----                                               -------    ------
Function        Add-NodeKeys                                       0.0        PSDesiredStateConfiguration
Function        AddDscResourceProperty                             0.0        PSDesiredStateConfiguration
Function        AddDscResourcePropertyFromMetadata                 0.0        PSDesiredStateConfiguration
Function        AfterAll                                           3.3.9      Pester
Function        AfterEach                                          3.3.9      Pester
Function        Assert-MockCalled                                  3.3.9      Pester
Function        Assert-VerifiableMocks                             3.3.9      Pester
Function        BeforeAll                                          3.3.9      Pester
Function        BeforeEach                                         3.3.9      Pester
Function        cd..
Function        cd\
Function        CheckResourceFound                                 0.0        PSDesiredStateConfiguration
Function        Clear-Host
Function        Compress-Archive                                   1.0.1.0    Microsoft.PowerShell.Archive
Function        Configuration                                      0.0        PSDesiredStateConfiguration
Function        Context                                            3.3.9      Pester
Function        ConvertTo-MOFInstance                              0.0        PSDesiredStateConfiguration
Function        Describe                                           3.3.9      Pester
Function        Expand-Archive                                     1.0.1.0    Microsoft.PowerShell.Archive
Function        Find-Command                                       1.0.0.1    PowerShellGet
Function        Find-DscResource                                   1.0.0.1    PowerShellGet
Function        Find-Module                                        1.0.0.1    PowerShellGet
Function        Find-RoleCapability                                1.0.0.1    PowerShellGet
Function        Find-Script                                        1.0.0.1    PowerShellGet
Function        Format-Hex                                         3.1.0.0    Microsoft.PowerShell.Utility
Function        Generate-VersionInfo                               0.0        PSDesiredStateConfiguration
Function        Get-CompatibleVersionAddtionaPropertiesStr         0.0        PSDesiredStateConfiguration
Function        Get-ComplexResourceQualifier                       0.0        PSDesiredStateConfiguration
Function        Get-ConfigurationErrorCount                        0.0        PSDesiredStateConfiguration
Function        Get-DscResource                                    0.0        PSDesiredStateConfiguration
Function        Get-DSCResourceModules                             0.0        PSDesiredStateConfiguration
Function        Get-EncryptedPassword                              0.0        PSDesiredStateConfiguration
Function        Get-FileHash                                       3.1.0.0    Microsoft.PowerShell.Utility
Function        Get-InnerMostErrorRecord                           0.0        PSDesiredStateConfiguration
Function        Get-InstalledModule                                1.0.0.1    PowerShellGet
Function        Get-InstalledScript                                1.0.0.1    PowerShellGet
Function        Get-MockDynamicParameters                          3.3.9      Pester
Function        Get-MofInstanceName                                0.0        PSDesiredStateConfiguration
Function        Get-MofInstanceText                                0.0        PSDesiredStateConfiguration
Function        Get-PositionInfo                                   0.0        PSDesiredStateConfiguration
Function        Get-PSCurrentConfigurationNode                     0.0        PSDesiredStateConfiguration
Function        Get-PSDefaultConfigurationDocument                 0.0        PSDesiredStateConfiguration
Function        Get-PSMetaConfigDocumentInstVersionInfo            0.0        PSDesiredStateConfiguration
Function        Get-PSMetaConfigurationProcessed                   0.0        PSDesiredStateConfiguration
Function        Get-PSRepository                                   1.0.0.1    PowerShellGet
Function        Get-PSTopConfigurationName                         0.0        PSDesiredStateConfiguration
Function        Get-PublicKeyFromFile                              0.0        PSDesiredStateConfiguration
Function        Get-PublicKeyFromStore                             0.0        PSDesiredStateConfiguration
Function        Get-TestDriveItem                                  3.3.9      Pester
Function        Get-Verb
Function        GetCompositeResource                               0.0        PSDesiredStateConfiguration
Function        GetImplementingModulePath                          0.0        PSDesiredStateConfiguration
Function        GetModule                                          0.0        PSDesiredStateConfiguration
Function        GetPatterns                                        0.0        PSDesiredStateConfiguration
Function        GetResourceFromKeyword                             0.0        PSDesiredStateConfiguration
Function        GetSyntax                                          0.0        PSDesiredStateConfiguration
Function        help
Function        Import-PowerShellDataFile                          3.1.0.0    Microsoft.PowerShell.Utility
Function        ImportCimAndScriptKeywordsFromModule               0.0        PSDesiredStateConfiguration
Function        ImportClassResourcesFromModule                     0.0        PSDesiredStateConfiguration
Function        ImportSystemModules
Function        In                                                 3.3.9      Pester
Function        Initialize-ConfigurationRuntimeState               0.0        PSDesiredStateConfiguration
Function        InModuleScope                                      3.3.9      Pester
Function        Install-Module                                     1.0.0.1    PowerShellGet
Function        Install-Script                                     1.0.0.1    PowerShellGet
Function        Invoke-Mock                                        3.3.9      Pester
Function        Invoke-Pester                                      3.3.9      Pester
Function        IsHiddenResource                                   0.0        PSDesiredStateConfiguration
Function        IsPatternMatched                                   0.0        PSDesiredStateConfiguration
Function        It                                                 3.3.9      Pester
Function        Mock                                               3.3.9      Pester
Function        more
Function        New-DscChecksum                                    0.0        PSDesiredStateConfiguration
Function        New-Fixture                                        3.3.9      Pester
Function        New-Guid                                           3.1.0.0    Microsoft.PowerShell.Utility
Function        New-ScriptFileInfo                                 1.0.0.1    PowerShellGet
Function        New-TemporaryFile                                  3.1.0.0    Microsoft.PowerShell.Utility
Function        Node                                               0.0        PSDesiredStateConfiguration
Function        oss
Function        Pause
Function        prompt
Function        PSConsoleHostReadline                              1.2        PSReadLine
Function        Publish-Module                                     1.0.0.1    PowerShellGet
Function        Publish-Script                                     1.0.0.1    PowerShellGet
Function        ReadEnvironmentFile                                0.0        PSDesiredStateConfiguration
Function        Register-PSRepository                              1.0.0.1    PowerShellGet
Function        Save-Module                                        1.0.0.1    PowerShellGet
Function        Save-Script                                        1.0.0.1    PowerShellGet
Function        Set-DynamicParameterVariables                      3.3.9      Pester
Function        Set-NodeExclusiveResources                         0.0        PSDesiredStateConfiguration
Function        Set-NodeManager                                    0.0        PSDesiredStateConfiguration
Function        Set-NodeResources                                  0.0        PSDesiredStateConfiguration
Function        Set-NodeResourceSource                             0.0        PSDesiredStateConfiguration
Function        Set-PSCurrentConfigurationNode                     0.0        PSDesiredStateConfiguration
Function        Set-PSDefaultConfigurationDocument                 0.0        PSDesiredStateConfiguration
Function        Set-PSMetaConfigDocInsProcessedBeforeMeta          0.0        PSDesiredStateConfiguration
Function        Set-PSMetaConfigVersionInfoV2                      0.0        PSDesiredStateConfiguration
Function        Set-PSRepository                                   1.0.0.1    PowerShellGet
Function        Set-PSTopConfigurationName                         0.0        PSDesiredStateConfiguration
Function        Setup                                              3.3.9      Pester
Function        Should                                             3.3.9      Pester
Function        StrongConnect                                      0.0        PSDesiredStateConfiguration
Function        TabExpansion2
Function        Test-ConflictingResources                          0.0        PSDesiredStateConfiguration
Function        Test-ModuleReloadRequired                          0.0        PSDesiredStateConfiguration
Function        Test-MofInstanceText                               0.0        PSDesiredStateConfiguration
Function        Test-NodeManager                                   0.0        PSDesiredStateConfiguration
Function        Test-NodeResources                                 0.0        PSDesiredStateConfiguration
Function        Test-NodeResourceSource                            0.0        PSDesiredStateConfiguration
Function        Test-ScriptFileInfo                                1.0.0.1    PowerShellGet
Function        ThrowError                                         0.0        PSDesiredStateConfiguration
Function        Uninstall-Module                                   1.0.0.1    PowerShellGet
Function        Uninstall-Script                                   1.0.0.1    PowerShellGet
Function        Unregister-PSRepository                            1.0.0.1    PowerShellGet
Function        Update-ConfigurationDocumentRef                    0.0        PSDesiredStateConfiguration
Function        Update-ConfigurationErrorCount                     0.0        PSDesiredStateConfiguration
Function        Update-DependsOn                                   0.0        PSDesiredStateConfiguration
Function        Update-LocalConfigManager                          0.0        PSDesiredStateConfiguration
Function        Update-Module                                      1.0.0.1    PowerShellGet
Function        Update-ModuleManifest                              1.0.0.1    PowerShellGet
Function        Update-ModuleVersion                               0.0        PSDesiredStateConfiguration
Function        Update-Script                                      1.0.0.1    PowerShellGet
Function        Update-ScriptFileInfo                              1.0.0.1    PowerShellGet
Function        ValidateNoCircleInNodeResources                    0.0        PSDesiredStateConfiguration
Function        ValidateNodeExclusiveResources                     0.0        PSDesiredStateConfiguration
Function        ValidateNodeManager                                0.0        PSDesiredStateConfiguration
Function        ValidateNodeResources                              0.0        PSDesiredStateConfiguration
Function        ValidateNodeResourceSource                         0.0        PSDesiredStateConfiguration
Function        ValidateNoNameNodeResources                        0.0        PSDesiredStateConfiguration
Function        ValidateUpdate-ConfigurationData                   0.0        PSDesiredStateConfiguration
Function        Write-Log                                          0.0        PSDesiredStateConfiguration
Function        Write-MetaConfigFile                               0.0        PSDesiredStateConfiguration
Function        Write-NodeMOFFile                                  0.0        PSDesiredStateConfiguration
Function        WriteFile                                          0.0        PSDesiredStateConfiguration
Cmdlet          Add-Content                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Add-History                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Add-Member                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Add-Type                                           3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Clear-Content                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Clear-History                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Clear-Item                                         3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Clear-ItemProperty                                 3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Clear-Variable                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Compare-Object                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Connect-PSSession                                  3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Convert-Path                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          ConvertFrom-Csv                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          ConvertFrom-Json                                   3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          ConvertFrom-SecureString                           3.0.0.0    Microsoft.PowerShell.Security
Cmdlet          ConvertFrom-StringData                             3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          ConvertTo-Csv                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          ConvertTo-Json                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          ConvertTo-SecureString                             3.0.0.0    Microsoft.PowerShell.Security
Cmdlet          ConvertTo-Xml                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Copy-Item                                          3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Copy-ItemProperty                                  3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Debug-Job                                          3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Debug-Process                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Debug-Runspace                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Disable-PSBreakpoint                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Disable-PSSessionConfiguration                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Disable-RunspaceDebug                              3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Disconnect-PSSession                               3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Enable-PSBreakpoint                                3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Enable-PSSessionConfiguration                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Enable-RunspaceDebug                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Enter-PSHostProcess                                3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Enter-PSSession                                    3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Exit-PSHostProcess                                 3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Exit-PSSession                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Export-Alias                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Export-Clixml                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Export-Csv                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Export-FormatData                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Export-ModuleMember                                3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Find-Package                                       1.0.0.1    PackageManagement
Cmdlet          Find-PackageProvider                               1.0.0.1    PackageManagement
Cmdlet          ForEach-Object                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Format-Custom                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Format-List                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Format-Table                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Format-Wide                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Alias                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-ChildItem                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-Command                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Content                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-Credential                                     3.0.0.0    Microsoft.PowerShell.Security
Cmdlet          Get-Culture                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Date                                           3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Event                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-EventSubscriber                                3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-ExecutionPolicy                                3.0.0.0    Microsoft.PowerShell.Security
Cmdlet          Get-FormatData                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Help                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-History                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Host                                           3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Item                                           3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-ItemProperty                                   3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-ItemPropertyValue                              3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-Job                                            3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Location                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-Member                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Module                                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Package                                        1.0.0.1    PackageManagement
Cmdlet          Get-PackageProvider                                1.0.0.1    PackageManagement
Cmdlet          Get-PackageSource                                  1.0.0.1    PackageManagement
Cmdlet          Get-Process                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-PSBreakpoint                                   3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-PSCallStack                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-PSDrive                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-PSHostProcessInfo                              3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-PSProvider                                     3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Get-PSReadlineKeyHandler                           1.2        PSReadLine
Cmdlet          Get-PSReadlineOption                               1.2        PSReadLine
Cmdlet          Get-PSSession                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-PSSessionCapability                            3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-PSSessionConfiguration                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Get-Random                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Runspace                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-RunspaceDebug                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-TraceSource                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-TypeData                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-UICulture                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Unique                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Get-Variable                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Group-Object                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Import-Alias                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Import-Clixml                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Import-Csv                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Import-LocalizedData                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Import-Module                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Import-PackageProvider                             1.0.0.1    PackageManagement
Cmdlet          Install-Package                                    1.0.0.1    PackageManagement
Cmdlet          Install-PackageProvider                            1.0.0.1    PackageManagement
Cmdlet          Invoke-Command                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Invoke-Expression                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Invoke-History                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Invoke-Item                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Invoke-RestMethod                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Invoke-WebRequest                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Join-Path                                          3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Measure-Command                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Measure-Object                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Move-Item                                          3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Move-ItemProperty                                  3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          New-Alias                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          New-Event                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          New-Item                                           3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          New-ItemProperty                                   3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          New-Module                                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-ModuleManifest                                 3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-Object                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          New-PSDrive                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          New-PSRoleCapabilityFile                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-PSSession                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-PSSessionConfigurationFile                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-PSSessionOption                                3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-PSTransportOption                              3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          New-TimeSpan                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          New-Variable                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Out-Default                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Out-File                                           3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Out-Host                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Out-Null                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Out-String                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Pop-Location                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Push-Location                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Read-Host                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Receive-Job                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Receive-PSSession                                  3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Register-ArgumentCompleter                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Register-EngineEvent                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Register-ObjectEvent                               3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Register-PackageSource                             1.0.0.1    PackageManagement
Cmdlet          Register-PSSessionConfiguration                    3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-Event                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Remove-Item                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Remove-ItemProperty                                3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Remove-Job                                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-Module                                      3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-PSBreakpoint                                3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Remove-PSDrive                                     3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Remove-PSReadlineKeyHandler                        1.2        PSReadLine
Cmdlet          Remove-PSSession                                   3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Remove-TypeData                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Remove-Variable                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Rename-Item                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Rename-ItemProperty                                3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Resolve-Path                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Save-Help                                          3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Save-Package                                       1.0.0.1    PackageManagement
Cmdlet          Select-Object                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Select-String                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Select-Xml                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Set-Alias                                          3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Set-Content                                        3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Set-Date                                           3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Set-ExecutionPolicy                                3.0.0.0    Microsoft.PowerShell.Security
Cmdlet          Set-Item                                           3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Set-ItemProperty                                   3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Set-Location                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Set-PackageSource                                  1.0.0.1    PackageManagement
Cmdlet          Set-PSBreakpoint                                   3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Set-PSDebug                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Set-PSReadlineKeyHandler                           1.2        PSReadLine
Cmdlet          Set-PSReadlineOption                               1.2        PSReadLine
Cmdlet          Set-PSSessionConfiguration                         3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Set-StrictMode                                     3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Set-TraceSource                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Set-Variable                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Sort-Object                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Split-Path                                         3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Start-Job                                          3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Start-Process                                      3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Start-Sleep                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Start-Transcript                                   3.0.0.0    Microsoft.PowerShell.Host
Cmdlet          Stop-Job                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Stop-Process                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Stop-Transcript                                    3.0.0.0    Microsoft.PowerShell.Host
Cmdlet          Tee-Object                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Test-ModuleManifest                                3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Test-Path                                          3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Test-PSSessionConfigurationFile                    3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Trace-Command                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Uninstall-Package                                  1.0.0.1    PackageManagement
Cmdlet          Unregister-Event                                   3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Unregister-PackageSource                           1.0.0.1    PackageManagement
Cmdlet          Unregister-PSSessionConfiguration                  3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Update-FormatData                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Update-Help                                        3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Update-TypeData                                    3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Wait-Debugger                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Wait-Event                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Wait-Job                                           3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Wait-Process                                       3.1.0.0    Microsoft.PowerShell.Management
Cmdlet          Where-Object                                       3.0.0.0    Microsoft.PowerShell.Core
Cmdlet          Write-Debug                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Error                                        3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Host                                         3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Information                                  3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Output                                       3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Progress                                     3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Verbose                                      3.1.0.0    Microsoft.PowerShell.Utility
Cmdlet          Write-Warning                                      3.1.0.0    Microsoft.PowerShell.Utility
```
