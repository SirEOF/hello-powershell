
## Get-AppLockerPolicy

```
PS C:\Users\test\Desktop> Get-Help -Parameter * Get-AppLockerPolicy

-Local <Boolean>
    Gets the AppLocker policy from the local GPO.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Domain <Boolean>
    Gets the AppLocker policy from the GPO that is specified by the path in the LDAP parameter.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Effective <Boolean>
    Gets the effective AppLocker policy on the local computer. The effective policy is the merge of the local AppLocker policy and any applied domain policies on the local computer.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-LDAP <String>
    The LDAP path of the Group Policy object. Must specify a unique GPO.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-XML <Boolean>
    Specifies that the AppLocker policy be output as an XML-formatted string.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


```

**-Local**

```
PS C:\Users\test\Desktop> Get-AppLockerPolicy -local

                                                                                            Version RuleCollections                                                                                     RuleCollectionTypes
                                                                                            ------- ---------------                                                                                     -------------------
                                                                                                  1 {}                                                                                                  {}

```
