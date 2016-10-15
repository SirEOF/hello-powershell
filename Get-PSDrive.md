
## Get-PSDrive

```
PS C:\Users\test\Desktop> Get-Help -Parameter * Get-PSDrive

-LiteralName <String[]>
    Specifies the name of the drive.

    The value of LiteralName is used exactly as it is typed. No characters are interpreted as wildcards. If the name includes escape characters, enclose it in single quotation marks. Single quotation marks tell Windows PowerShell not to interpret any characters as escape sequences.

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       true (ByValue, ByPropertyName)
    Accept wildcard characters?  false


-Name <String[]>
    Gets only the specified drives. Type the drive name or letter without a colon (:).

    Required?                    false
    Position?                    1
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-PSProvider <String[]>
    Gets only the drives supported by the specified Windows PowerShell provider. Type the name of a provider, such as FileSystem, Registry, or Certificate.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-Scope <String>
    Gets only drives in the specified scope. Valid values are "Global", "Local", or "Script", or a number relative to the current scope (0 through the number of scopes, where 0 is the current scope and 1 is its parent). "Local" is the default. For more information, see about_Scopes
    (http://go.microsoft.com/fwlink/?LinkID=113260).

    Required?                    false
    Position?                    named
    Default value                Local
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-UseTransaction [<SwitchParameter>]
    Includes the command in the active transaction. This parameter can only be used when a transaction is in progress. For more information, see about_Transactions.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false

```

```
PS C:\Users\test\Desktop> Get-PSDrive

Name           Used (GB)     Free (GB) Provider      Root
----           ---------     --------- --------      ----
Alias                                  Alias
C                  26.69         33.21 FileSystem    C:\
Cert                                   Certificate   \
D                                      FileSystem    D:\
Env                                    Environment
Function                               Function
HKCU                                   Registry      HKEY_CURRENT_USER
HKLM                                   Registry      HKEY_LOCAL_MACHINE
Variable                               Variable
WSMan                                  WSMan
```
