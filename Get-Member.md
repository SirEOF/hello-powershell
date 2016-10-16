
## Get-Member

```
PS C:\Users\test> Get-Help -Parameter * Get-Member

-Force [<SwitchParameter>]
    Adds the intrinsic members (PSBase, PSAdapted, PSObject, PSTypeNames) and the compiler-generated get_ and set_ methods to the display. By default, Get-Member gets these properties in all views other than "Base" and "Adapted," but it does not display them.

    The following list describes the properties that are added when you use the Force parameter:

    -- PSBase:  The original properties of the .NET Framework object without extension or adaptation. These are the properties defined for the object class and listed in MSDN.

    -- PSAdapted: The properties and methods defined in the Windows PowerShell extended type system.

    -- PSExtended: The properties and methods that were added in the Types.ps1xml files or by using the Add-Member cmdlet.

    -- PSObject: The adapter that converts the base object to a Windows PowerShell PSObject object.

    -- PSTypeNames: A list of object types that describe the object, in order of specificity. When formatting the object, Windows PowerShell searches for the types in the Format.ps1xml files in the Windows PowerShell installation directory ($pshome). It uses the formatting definition for the first
    type that it finds.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-InputObject <PSObject>
    Specifies the object whose members are retrieved.

    Using the InputObject parameter is not the same as piping an object to Get-Member. The differences are as follows:

    -- When you pipe a collection of objects to Get-Member, Get-Member gets the members of the individual objects in the collection, such as the properties of each string in an array of strings.

    -- When you use InputObject to submit a collection of objects, Get-Member gets the members of the collection, such as the properties of the array in an array of strings.

    Required?                    false
    Position?                    named
    Default value
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false


-MemberType <PSMemberTypes>
    Gets only members with the specified member type. The default is All.

    The valid values for this parameter are: AliasProperty, All, CodeMethod, CodeProperty, Event, MemberSet, Method, Methods, Noteproperty, ParameterizedProperty, Properties, Property, PropertySet, ScriptMethod, and ScriptProperty.

    For information about these values, see "PSMemberTypes Enumeration" in MSDN at http://msdn.microsoft.com/library/windows/desktop/system.management.automation.psmembertypes(v=vs.85).aspx.

    Not all objects have every type of member. If you specify a member type that the object does not have, Windows PowerShell returns a null value.

    To get related types of members, such as all extended members, use the View parameter. If you use the MemberType parameter with the Static or View parameters, Get-Member gets the members that belong to both sets.

    Required?                    false
    Position?                    named
    Default value                All
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Name <String[]>
    Specifies the names of one or more properties or methods of the object. Get-Member gets only the specified properties and methods.

    If you use the Name parameter with the MemberType, View, or Static parameters, Get-Member gets only the members that satisfy the criteria of all parameters.

    To get a static member by name, use the Static parameter with the Name parameter.

    Required?                    false
    Position?                    1
    Default value
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Static [<SwitchParameter>]
    Gets only the static properties and methods of the object.

    Static properties and methods are defined on the class of objects, not on any particular instance of the class.

    If you use the Static parameter with the View parameter, the View parameter is ignored. If you use the Static parameter with the MemberType parameter, Get-Member gets only the members that belong to both sets.

    Required?                    false
    Position?                    named
    Default value                False
    Accept pipeline input?       false
    Accept wildcard characters?  false


-View <PSMemberViewTypes>
    Gets only particular types of members (properties and methods). Specify one or more of the values. The default is "Adapted, Extended".

    Valid values are:

    -- Base:  Gets only the original properties and methods of the .NET Framework object (without extension or adaptation).

    -- Adapted:  Gets only the properties and methods defined in the Windows PowerShell extended type system.

    -- Extended: Gets only the properties and methods that were added in the Types.ps1xml files or by using the Add-Member cmdlet.

    -- All: Gets the members in the Base, Adapted, and Extended views.

    The View parameter determines the members retrieved, not just the display of those members.

    To get particular member types, such as script properties, use the MemberType parameter. If you use the MemberType and View parameters in the same command, Get-Member gets the members that belong to both sets. If you use the Static and View parameters in the same command, the View parameter is
    ignored.

    Required?                    false
    Position?                    named
    Default value                "Adapted, Extended"
    Accept pipeline input?       false
    Accept wildcard characters?  false



```


```
PS C:\Users\test> (New-Object System.Net.WebClient) | Get-Member


   TypeName: System.Net.WebClient

Name                      MemberType Definition
----                      ---------- ----------
Disposed                  Event      System.EventHandler Disposed(System.Object, System.EventArgs)
DownloadDataCompleted     Event      System.Net.DownloadDataCompletedEventHandler DownloadDataCompleted(System.Object, System.Net.DownloadDataCompletedEventArgs)
DownloadFileCompleted     Event      System.ComponentModel.AsyncCompletedEventHandler DownloadFileCompleted(System.Object, System.ComponentModel.AsyncCompletedEventArgs)
DownloadProgressChanged   Event      System.Net.DownloadProgressChangedEventHandler DownloadProgressChanged(System.Object, System.Net.DownloadProgressChangedEventArgs)
DownloadStringCompleted   Event      System.Net.DownloadStringCompletedEventHandler DownloadStringCompleted(System.Object, System.Net.DownloadStringCompletedEventArgs)
OpenReadCompleted         Event      System.Net.OpenReadCompletedEventHandler OpenReadCompleted(System.Object, System.Net.OpenReadCompletedEventArgs)
OpenWriteCompleted        Event      System.Net.OpenWriteCompletedEventHandler OpenWriteCompleted(System.Object, System.Net.OpenWriteCompletedEventArgs)
UploadDataCompleted       Event      System.Net.UploadDataCompletedEventHandler UploadDataCompleted(System.Object, System.Net.UploadDataCompletedEventArgs)
UploadFileCompleted       Event      System.Net.UploadFileCompletedEventHandler UploadFileCompleted(System.Object, System.Net.UploadFileCompletedEventArgs)
UploadProgressChanged     Event      System.Net.UploadProgressChangedEventHandler UploadProgressChanged(System.Object, System.Net.UploadProgressChangedEventArgs)
UploadStringCompleted     Event      System.Net.UploadStringCompletedEventHandler UploadStringCompleted(System.Object, System.Net.UploadStringCompletedEventArgs)
UploadValuesCompleted     Event      System.Net.UploadValuesCompletedEventHandler UploadValuesCompleted(System.Object, System.Net.UploadValuesCompletedEventArgs)
WriteStreamClosed         Event      System.Net.WriteStreamClosedEventHandler WriteStreamClosed(System.Object, System.Net.WriteStreamClosedEventArgs)
CancelAsync               Method     void CancelAsync()
CreateObjRef              Method     System.Runtime.Remoting.ObjRef CreateObjRef(type requestedType)
Dispose                   Method     void Dispose(), void IDisposable.Dispose()
DownloadData              Method     byte[] DownloadData(string address), byte[] DownloadData(uri address)
DownloadDataAsync         Method     void DownloadDataAsync(uri address), void DownloadDataAsync(uri address, System.Object userToken)
DownloadDataTaskAsync     Method     System.Threading.Tasks.Task[byte[]] DownloadDataTaskAsync(string address), System.Threading.Tasks.Task[byte[]] DownloadDataTaskAsync(uri address)
DownloadFile              Method     void DownloadFile(string address, string fileName), void DownloadFile(uri address, string fileName)
DownloadFileAsync         Method     void DownloadFileAsync(uri address, string fileName), void DownloadFileAsync(uri address, string fileName, System.Object userToken)
DownloadFileTaskAsync     Method     System.Threading.Tasks.Task DownloadFileTaskAsync(string address, string fileName), System.Threading.Tasks.Task DownloadFileTaskAsync(uri address, string fileName)
DownloadString            Method     string DownloadString(string address), string DownloadString(uri address)
DownloadStringAsync       Method     void DownloadStringAsync(uri address), void DownloadStringAsync(uri address, System.Object userToken)
DownloadStringTaskAsync   Method     System.Threading.Tasks.Task[string] DownloadStringTaskAsync(string address), System.Threading.Tasks.Task[string] DownloadStringTaskAsync(uri address)
Equals                    Method     bool Equals(System.Object obj)
GetHashCode               Method     int GetHashCode()
GetLifetimeService        Method     System.Object GetLifetimeService()
GetType                   Method     type GetType()
InitializeLifetimeService Method     System.Object InitializeLifetimeService()
OpenRead                  Method     System.IO.Stream OpenRead(string address), System.IO.Stream OpenRead(uri address)
OpenReadAsync             Method     void OpenReadAsync(uri address), void OpenReadAsync(uri address, System.Object userToken)
OpenReadTaskAsync         Method     System.Threading.Tasks.Task[System.IO.Stream] OpenReadTaskAsync(string address), System.Threading.Tasks.Task[System.IO.Stream] OpenReadTaskAsync(uri address)
OpenWrite                 Method     System.IO.Stream OpenWrite(string address), System.IO.Stream OpenWrite(uri address), System.IO.Stream OpenWrite(string address, string method), System.IO.Stream OpenWrite(uri address, string method)
OpenWriteAsync            Method     void OpenWriteAsync(uri address), void OpenWriteAsync(uri address, string method), void OpenWriteAsync(uri address, string method, System.Object userToken)
OpenWriteTaskAsync        Method     System.Threading.Tasks.Task[System.IO.Stream] OpenWriteTaskAsync(string address), System.Threading.Tasks.Task[System.IO.Stream] OpenWriteTaskAsync(uri address), System.Threading.Tasks.Task[System.IO.Stream] OpenWriteTaskAsync(string address, string method), S...
ToString                  Method     string ToString()
UploadData                Method     byte[] UploadData(string address, byte[] data), byte[] UploadData(uri address, byte[] data), byte[] UploadData(string address, string method, byte[] data), byte[] UploadData(uri address, string method, byte[] data)
UploadDataAsync           Method     void UploadDataAsync(uri address, byte[] data), void UploadDataAsync(uri address, string method, byte[] data), void UploadDataAsync(uri address, string method, byte[] data, System.Object userToken)
UploadDataTaskAsync       Method     System.Threading.Tasks.Task[byte[]] UploadDataTaskAsync(string address, byte[] data), System.Threading.Tasks.Task[byte[]] UploadDataTaskAsync(uri address, byte[] data), System.Threading.Tasks.Task[byte[]] UploadDataTaskAsync(string address, string method, byt...
UploadFile                Method     byte[] UploadFile(string address, string fileName), byte[] UploadFile(uri address, string fileName), byte[] UploadFile(string address, string method, string fileName), byte[] UploadFile(uri address, string method, string fileName)
UploadFileAsync           Method     void UploadFileAsync(uri address, string fileName), void UploadFileAsync(uri address, string method, string fileName), void UploadFileAsync(uri address, string method, string fileName, System.Object userToken)
UploadFileTaskAsync       Method     System.Threading.Tasks.Task[byte[]] UploadFileTaskAsync(string address, string fileName), System.Threading.Tasks.Task[byte[]] UploadFileTaskAsync(uri address, string fileName), System.Threading.Tasks.Task[byte[]] UploadFileTaskAsync(string address, string met...
UploadString              Method     string UploadString(string address, string data), string UploadString(uri address, string data), string UploadString(string address, string method, string data), string UploadString(uri address, string method, string data)
UploadStringAsync         Method     void UploadStringAsync(uri address, string data), void UploadStringAsync(uri address, string method, string data), void UploadStringAsync(uri address, string method, string data, System.Object userToken)
UploadStringTaskAsync     Method     System.Threading.Tasks.Task[string] UploadStringTaskAsync(string address, string data), System.Threading.Tasks.Task[string] UploadStringTaskAsync(uri address, string data), System.Threading.Tasks.Task[string] UploadStringTaskAsync(string address, string metho...
UploadValues              Method     byte[] UploadValues(string address, System.Collections.Specialized.NameValueCollection data), byte[] UploadValues(uri address, System.Collections.Specialized.NameValueCollection data), byte[] UploadValues(string address, string method, System.Collections.Spec...
UploadValuesAsync         Method     void UploadValuesAsync(uri address, System.Collections.Specialized.NameValueCollection data), void UploadValuesAsync(uri address, string method, System.Collections.Specialized.NameValueCollection data), void UploadValuesAsync(uri address, string method, Syste...
UploadValuesTaskAsync     Method     System.Threading.Tasks.Task[byte[]] UploadValuesTaskAsync(string address, System.Collections.Specialized.NameValueCollection data), System.Threading.Tasks.Task[byte[]] UploadValuesTaskAsync(string address, string method, System.Collections.Specialized.NameVal...
AllowReadStreamBuffering  Property   bool AllowReadStreamBuffering {get;set;}
AllowWriteStreamBuffering Property   bool AllowWriteStreamBuffering {get;set;}
BaseAddress               Property   string BaseAddress {get;set;}
CachePolicy               Property   System.Net.Cache.RequestCachePolicy CachePolicy {get;set;}
Container                 Property   System.ComponentModel.IContainer Container {get;}
Credentials               Property   System.Net.ICredentials Credentials {get;set;}
Encoding                  Property   System.Text.Encoding Encoding {get;set;}
Headers                   Property   System.Net.WebHeaderCollection Headers {get;set;}
IsBusy                    Property   bool IsBusy {get;}
Proxy                     Property   System.Net.IWebProxy Proxy {get;set;}
QueryString               Property   System.Collections.Specialized.NameValueCollection QueryString {get;set;}
ResponseHeaders           Property   System.Net.WebHeaderCollection ResponseHeaders {get;}
Site                      Property   System.ComponentModel.ISite Site {get;set;}
UseDefaultCredentials     Property   bool UseDefaultCredentials {get;set;}


```
