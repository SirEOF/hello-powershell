
## Start-BitsTransfer

```
PS C:\Windows\system32> Get-Help -Parameter * Start-BitsTransfer

-Asynchronous [<SwitchParameter>]
    Allows the BITS transfer job to be created and then processed in the background. The command prompt reappears immediately after the BITS transfer job is created. The returned BitsJob object can be used to monitor status and progress.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  true


-Authentication <string>
    Specifies the authentication mechanism to be used at the server. Possible values are:

    - Basic: Basic is a scheme in which the user name and password are sent in clear text to the server or proxy.
    - Digest: Digest is a challenge-response scheme that uses a server-specified data string for the challenge.
    - NTLM: NTLM is a challenge-response scheme that uses the credentials of the user for authentication in a Windows-based network environment.
    - Negotiate (the default): Negotiate is a challenge-response scheme that negotiates with the server or proxy to determine which scheme to use for authentication. For example, this parameter value allows negotiation to determine whether the Kerberos protocol or NTLM is used.
    - Passport: Passport is a centralized authentication service provided by Microsoft that offers a single logon for member sites.

    Required?                    false
    Position?                    named
    Default value                Negotiate
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Credential <PSCredential>
    Specifies the credentials to use to authenticate the user at the server. The default is the current user. Type a user name, such as "User01", "Domain01\User01", or "User@Contoso.com". Or, use the Get-Credential cmdlet to create the value for this parameter. When you type a user name, you will
    be prompted for a password.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Description <string>
    Describes the BITS transfer job. The description is limited to 1,024 characters.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Destination <string[]>
    Specifies the destination location and the names of the files that you want to transfer. The destination names are paired with the corresponding source file names. For example, the first file name specified in the Source parameter corresponds to the first file name in the Destination
    parameter, and the second file name in the Source parameter corresponds to the second file name in the Destination parameter. The Source and Destination parameters must have the same number of elements; otherwise, the command produces an error.

    Required?                    false
    Position?                    2
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-DisplayName <string>
    Specifies a display name for the BITS transfer job. The display name provides a user-friendly way to differentiate BITS transfer jobs.

    Required?                    false
    Position?                    named
    Default value                BitsJob
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Priority <string>
    Sets the priority of the BITS transfer job, which affects bandwidth usage. You can specify the following values:

    - Foreground (default): Transfers the job in the foreground. Foreground transfers compete for network bandwidth with other applications, which can impede the user's overall network experience. However, if the Start-BitsTransfer command is being used interactively, this is likely the best
    option. This is the highest priority level.
    - High: Transfers the job in the background with a high priority. Background transfers use the idle network bandwidth of the client computer to transfer files.
    - Normal: Transfers the job in the background with a normal priority. Background transfers use the idle network bandwidth of the client computer to transfer files.
    - Low: Transfers the job in the background with a low priority. Background transfers use the idle network bandwidth of the client to transfer files. This is the lowest background priority level.

    Required?                    false
    Position?                    named
    Default value                Normal
    Accept pipeline input?       false
    Accept wildcard characters?  false


-ProxyAuthentication <string>
    Specifies the authentication mechanism to use at the Web proxy. Possible values are:

    - Basic: Basic is a scheme in which the user name and password are sent in clear-text to the server or proxy.
    - Digest: Digest is a challenge-response scheme that uses a server-specified data string for the challenge.
    - NTLM: NTLM is a challenge-response scheme that uses the credentials of the user for authentication in a Windows-based network environment.
    - Negotiate (the default): Negotiate is a challenge-response scheme that negotiates with the server or proxy to determine which scheme to use for authentication. For example, this parameter value allows negotiation to determine whether  the Kerberos protocol or NTLM is used.
    - Passport: Passport is a centralized authentication service provided by Microsoft that offers a single logon for member sites.

    Required?                    false
    Position?                    named
    Default value                Negotiate
    Accept pipeline input?       false
    Accept wildcard characters?  false


-ProxyBypass <string[]>
    Specifies a list of host names to use for a direct connection. The hosts in the list are tried in order until a successful connection is achieved. Specifying this parameter bypasses the proxy. If this parameter is used, the ProxyUsage parameter must be set to Override; otherwise, an error
    occurs.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-ProxyCredential <PSCredential>
    Specifies the credentials to use to authenticate the user at the proxy. You can use the Get-Credential cmdlet to create a value for this parameter.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-ProxyList <Uri[]>
    Specifies a list of proxies to use. The proxies in the list are tried in order until a successful connection is achieved. If this parameter is specified and ProxyUsage is set to a value other than Override, an error occurs.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-ProxyUsage <string>
    Specifies the proxy usage settings. Possible values are:

    - SystemDefault (the default): Use the system default proxy settings.
    - NoProxy: Do not use a proxy to transfer files. Use this option when you transfer files within a local area network (LAN).
    - AutoDetect: Automatically detect proxy settings. BITS detects proxy settings for each file in the job.
    - Override: Specify the proxies or servers to use. If the ProxyList parameter is also specified, the proxies in that list are used. If the ProxyBypass parameter is also specified, the servers in that list are used. In both cases, the first member of the list is used. If the first member is
    unreachable, the subsequent members are tried until a member is contacted successfully.

    Required?                    false
    Position?                    named
    Default value                SystemDefault
    Accept pipeline input?       false
    Accept wildcard characters?  false


-RetryInterval <int>
    Specifies the minimum length of time, in seconds, that BITS waits before trying to transfer the file after BITS encounters a transient error. The minimum allowed value is 60 seconds. If this value exceeds the RetryTimeout value from the BitsJob object, BITS will not retry the transfer.
    Instead, BITS sets the state of the BITS transfer job to the Error state.

    The default is 600 seconds (10 minutes).

    Required?                    false
    Position?                    named
    Default value                600
    Accept pipeline input?       false
    Accept wildcard characters?  false


-RetryTimeout <int>
    Specifies the length of time, in seconds, that BITS tries to transfer the file after the first transient error occurs. Setting the retry period to 0 prevents retries and forces the job into the BG_JOB_STATE_ERROR state when an error occurs. If the retry period value exceeds the
    JobInactivityTimeout Group Policy setting (90-day default), BITS cancels the job after the JobInactivityTimeout Group Policy setting is exceeded.

    The default is 1,209,600 seconds (14 days).

    Required?                    false
    Position?                    named
    Default value                1209600
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Source <string[]>
    Specifies the source location and the names of the files that you want to transfer. The source file names are paired with the corresponding destination file names. For example, the first file name specified in the Source parameter corresponds to the first file name in the Destination
    parameter, and the second file name in the Source parameter corresponds to  the second file name in the Destination parameter. The Source and Destination parameters must have the same number of elements; otherwise, the command produces an error. You can use standard wildcard characters such as
    the asterisk (*) and the question mark (?). Or, you can use a range operator such as "[a-r]".

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       true (ByPropertyName)
    Accept wildcard characters?  false


-Suspended [<SwitchParameter>]
    Suspends the BITS transfer job. If the Suspended parameter is not specified, the job automatically begins the transfer job. If the Suspended parameter is specified, the command prompt returns immediately after the BITS transfer job is created. You can use the Resume-BitsTransfer cmdlet to
    start the transfer job.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-TransferType <string>
    Specifies the BITS transfer job type. Possible values are:

    - Download (the default): Specifies that the transfer job downloads files to the client computer.
    - Upload: Specifies that the transfer job uploads a file to the server.
    - UploadReply: Specifies that the transfer job uploads a file to the server and receives a reply file from the server.

    Required?                    false
    Position?                    named
    Default value                Download
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Confirm [<SwitchParameter>]
    Prompts you for confirmation before executing the command.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-WhatIf [<SwitchParameter>]
    Describes what would happen if you executed the command without actually executing the command.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false



```

----

```
Start-BitsTransfer http://192.168.0.114:8080/zmap-paper.pdf C:\Users\lab\Desktop\zmap-paper.pdf
```
