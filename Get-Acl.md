
## Get-Acl

```
PS C:\Windows\system32> Get-Help -Parameter * Get-Acl

-Audit [<SwitchParameter>]
    Gets the audit data for the security descriptor from the system access control list (SACL).

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Exclude <String[]>
    Omits the specified items. The value of this parameter qualifies the Path parameter. Enter a path element or pattern, such as "*.txt". Wildcards are permitted.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Filter <String>
    Specifies a filter in the provider's format or language. The value of this parameter qualifies the Path parameter. The syntax of the filter, including the use of wildcards, depends on the provider. Filters are more efficient than other parameters, because the provider applies them when
    gettting the objects, rather than having Windows PowerShell filter the objects after they are retrieved.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Include <String[]>
    Gets only the specified items. The value of this parameter qualifies the Path parameter. Enter a path element or pattern, such as "*.txt". Wildcards are permitted.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  true


-Path <String[]>
    Specifies the path to a resource. Get-Acl gets the security descriptor of the resource indicated by the path. Wildcards are permitted. If you omit the Path parameter, Get-Acl gets the security descriptor of the current directory.

    The parameter name ("Path") is optional.

    Required?                    false
    Position?                    1
    Default value
    Accept pipeline input?       true (ByValue, ByPropertyName)
    Accept wildcard characters?  true


-AllCentralAccessPolicies [<SwitchParameter>]
    Gets information about all central access policies that are enabled on the computer.

    Beginning in Windows Serverr 2012, administrators can use Active Directory and Group Policy to set central access policies for users and groups. For more information, see "Central Access Policies" at http://go.microsoft.com/fwlink/?LinkId=238408.

    This parameter is introduced in Windows PowerShell 3.0.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-InputObject <PSObject>
    Gets the security descriptor for the specified object. Enter a variable that contains the object or a command that gets the object.

    You cannot pipe an object, other than a path, to Get-Acl. Instead, use the InputObject parameter explicitly in the command.

    This parameter is introduced in Windows PowerShell 3.0.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-LiteralPath <String[]>
    Specifies the path to a resource. Unlike Path, the value of the LiteralPath parameter is used exactly as it is typed. No characters are interpreted as wildcards. If the path includes escape characters, enclose it in single quotation marks. Single quotation marks tell Windows PowerShell not to
    interpret any characters as escape sequences.

    This parameter is introduced in Windows PowerShell 3.0.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       true (ByValue, ByPropertyName)
    Accept wildcard characters?  false


-UseTransaction [<SwitchParameter>]
    Includes the command in the active transaction. This parameter is valid only when a transaction is in progress. For more information, see

    Required?                    false
    Position?                    named
    Default value                false
    Accept pipeline input?       false
    Accept wildcard characters?  false
```

**-Audit**

```
PS C:\Windows\system32> Get-Acl -Audit * | Sort-Object Access | more
```

**-Path**

```
PS C:\Windows\system32> Get-Acl -Path * | Sort-Object Owner | more


    Directory: C:\Windows\system32


Path                                                                                                Owner                                                                                               Access
----                                                                                                -----                                                                                               ------
NetworkList                                                                                         BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
Packet.dll                                                                                          BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
vmbuspipe.dll                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
NDF                                                                                                 BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
VmbusCoinstaller.dll                                                                                BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
Network_LLU.log                                                                                     BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
Recovery                                                                                            BUILTIN\Administrators                                                                              NT AUTHORITY\ANONYMOUS LOGON Deny  FullControl...
Printing_Admin_Scripts                                                                              BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
pthreadVC.dll                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
MUI                                                                                                 BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
VmdCoinstall.dll                                                                                    BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
msvcp120D.dll                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
system32_1.bin                                                                                      BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
LogFiles                                                                                            BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
umstartup.etl                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
vmbusres.dll                                                                                        BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
MRT                                                                                                 BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
Microsoft                                                                                           BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
umstartup000.etl                                                                                    BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
MRT.exe                                                                                             BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
vm3dum_10.dll                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
IcCoinstall.dll                                                                                     BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
Tasks                                                                                               BUILTIN\Administrators                                                                              CREATOR OWNER Allow  FullControl...
vm3dum.dll                                                                                          BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
CIRCoInst.dll                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
winrm                                                                                               BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
winevt                                                                                              BUILTIN\Administrators                                                                              NT AUTHORITY\Authenticated Users Allow  Read, Synchronize...
wdi                                                                                                 BUILTIN\Administrators                                                                              NT AUTHORITY\ANONYMOUS LOGON Deny  268435456...
wfp                                                                                                 BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
icrav03.rat                                                                                         BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
slmgr                                                                                               BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
SMI                                                                                                 BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
InstallPackage_ETW.Log                                                                              BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
ticrf.rat                                                                                           BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
Speech                                                                                              BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
dmvscres.dll                                                                                        BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
vm3dgl.dll                                                                                          BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
spool                                                                                               BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
spp                                                                                                 BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
Local_LLU.log                                                                                       BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
streamci.dll                                                                                        BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
NOISE.THA                                                                                           BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
noise.kor                                                                                           BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
EventProviders                                                                                      BUILTIN\Administrators                                                                              NT SERVICE\TrustedInstaller Allow  FullControl...
vmstorfltres.dll                                                                                    BUILTIN\Administrators                                                                              NT AUTHORITY\SYSTEM Allow  FullControl...
....
```
