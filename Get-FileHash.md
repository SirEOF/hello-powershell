
## Get-FileHash

```
PS C:\Windows\system32> Get-Help -Parameter * Get-FileHash

-Algorithm <String>
    Specifies the cryptographic hash function to use for computing the hash value of the contents of the specified file. A cryptographic hash function includes the property that it is not possible
    to find two distinct inputs that generate the same hash values. Hash functions are commonly used with digital signatures and for data integrity. Valid values for this parameter are SHA1, SHA256,
    SHA384, SHA512, MACTripleDES, MD5, and RIPEMD160. If no value is specified, or if the parameter is omitted, the default value is SHA256.

    For security reasons, MD5 and SHA1, which are no longer considered secure, should only be used for simple change validation, and should not be used to generate hash values for files that require
    protection from attack or tampering.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-LiteralPath <String[]>
    Specifies the path to a file. Unlike the Path parameter, the value of the LiteralPath parameter is used exactly as it is typed. No characters are interpreted as wildcard characters. If the path
    includes escape characters, enclose the path in single quotation marks. Single quotation marks instruct Windows PowerShell not to interpret characters as escape sequences.

    Required?                    true
    Position?                    named
    Default value
    Accept pipeline input?       True (ByPropertyName)
    Accept wildcard characters?  false


-Path <String[]>
    Specifies the path to one or more files. Wildcard characters are permitted.

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false

```

**-Algorithm**

```
PS C:\Windows\system32> Get-FileHash -Algorithm MACTripleDES cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
MACTRIPLEDES    9390CDEB4A3CCB36                                                       C:\Windows\system32\cmd.exe


PS C:\Windows\system32> Get-FileHash -Algorithm MD5 cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
MD5             AD7B9C14083B52BC532FBA5948342B98                                       C:\Windows\system32\cmd.exe


PS C:\Windows\system32> Get-FileHash -Algorithm RIPEMD160 cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
RIPEMD160       2F6B429E361D2DAC6E37039CAD7CD8BE873E1BDE                               C:\Windows\system32\cmd.exe


PS C:\Windows\system32> Get-FileHash -Algorithm SHA1 cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA1            EE8CBF12D87C4D388F09B4F69BED2E91682920B5                               C:\Windows\system32\cmd.exe


PS C:\Windows\system32> Get-FileHash -Algorithm SHA256 cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA256          17F746D82695FA9B35493B41859D39D786D32B23A9D2E00F4011DEC7A02402AE       C:\Windows\system32\cmd.exe


PS C:\Windows\system32> Get-FileHash -Algorithm SHA384 cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA384          2692D0724E4D6A98F59D7AFCC30D12A611C1EFE1BF2CFC31B1F677D865F7FA6B4DE... C:\Windows\system32\cmd.exe


PS C:\Windows\system32> Get-FileHash -Algorithm SHA512 cmd.exe

Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA512          E12AAD20C824187B39EDB3C7943709290B5DDBF1B4032988DB46F2E86DA3CF7E778... C:\Windows\system32\cmd.exe
```

If you want the whole hash, please try:

```
PS C:\Windows\system32> Get-FileHash -Algorithm SHA512 cmd.exe | Format-Table Algorithm,Hash

Algorithm                                                                                                                                             Hash
---------                                                                                                                                             ----
SHA512                                                                                                                                                E12AAD20C824187B39EDB3C7943709290B5DDBF1B4032988DB46F2E86DA3CF7E7783F78C82E4DC5DA232F666B8F9799A260A1F8E2694EB4D0CDAF78DA710FDE1
```
