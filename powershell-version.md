
## How to get powershell version ?

**$PSVersionTable**

```
PS C:\Users\test> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      4.0
WSManStackVersion              3.0
SerializationVersion           1.1.0.1
CLRVersion                     4.0.30319.17929
BuildVersion                   6.3.9600.16406
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0}
PSRemotingProtocolVersion      2.2

```

----

**$PSVersionTable.PSVersion**

```
PS C:\Users\test> $PSVersionTable.PSVersion

Major  Minor  Build  Revision
-----  -----  -----  --------
4      0      -1     -1
```
