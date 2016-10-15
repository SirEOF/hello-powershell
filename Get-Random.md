
## Get-Random

```
PS C:\Windows\system32> Get-Help -Parameter * Get-Random

-Count <Int32>
    Determines how many objects are returned. The default is 1. If the value of Count exceeds the number of objects in the collection, Get-Random returns all of the objects in random order.

    Required?                    false
    Position?                    named
    Default value                1
    Accept pipeline input?       false
    Accept wildcard characters?  false


-InputObject <Object[]>
    Specifies a collection of objects. Get-Random gets randomly selected objects in random order from the collection. Enter the objects, a variable that contains the objects, or a command or expression that gets the objects. You can also pipe a collection of objects to Get-Random.

    Required?                    true
    Position?                    1
    Default value
    Accept pipeline input?       true (ByValue)
    Accept wildcard characters?  false


-Maximum <Object>
    Specifies a maximum value for the random number. Get-Random returns a value that is less than the maximum (not equal). Enter a 32-bit integer or a double-precision floating-point number, or an object that can be converted to an integer or double, such as a numeric string ("100"). On a 64-bit
    computer, you can also enter a 64-bit integer.

    The value of Maximum must be greater than (not equal to) the value of Minimum.

    If the value of Maximum or Minimum is a floating-point number, Get-Random returns a randomly selected floating-point number. If the value of Minimum is a double (a floating-point number), the default value of Maximum is Double.MaxValue. Otherwise, the default value is Int32.MaxValue.

    On a 64-bit computer, if the value of Minimum is a 32-bit integer, the  default value of Maximum is Int32.MaxValue. If the value of Minimum is a double (a floating-point number), the default value of Maximum is Double.MaxValue. Otherwise, the default value is Int64.MaxValue.

    Required?                    false
    Position?                    1
    Default value                Int32.MaxValue, Double.MaxValue, Int64.MaxValue
    Accept pipeline input?       false
    Accept wildcard characters?  false


-Minimum <Object>
    Specifies a minimum value for the random number. Enter a 32-bit integer or a double-precision floating-point number, or an object that can be converted to an integer or double, such as a numeric string ("100"). On a 64-bit computer, you can enter a 64-bit integer. The default value is 0 (zero).

    The value of Minimum must be less than (not equal to) the value of Maximum. If the value of Maximum or Minimum is a floating-point number, Get-Random returns a randomly selected floating-point number.

    Required?                    false
    Position?                    named
    Default value                0
    Accept pipeline input?       false
    Accept wildcard characters?  false


-SetSeed <Int32>
    Specifies a seed value for the random number generator. This seed value is used for the current command and for all subsequent Get-Random commands in the current session until you use SetSeed again or close the session. You cannot reset the seed to its default, clock-based value.

    The SetSeed parameter is not required. By default, Get-Random uses the system clock to generate a seed value. Because SetSeed results in non-random behavior, it is typically used only when trying to reproduce behavior, such as when debugging or analyzing a script that includes Get-Random
    commands.

    Required?                    false
    Position?                    named
    Default value                System clock
    Accept pipeline input?       false
    Accept wildcard characters?  false

```

**-Maximum / -Minimum**

```
PS C:\Windows\system32> Get-Random -Maximum 400 -Minimum 200
241
```

**-SetSeed**

```
PS C:\Windows\system32> Get-Random -SetSeed 1
534011718
```
