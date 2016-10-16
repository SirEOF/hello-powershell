
**Int**

```
PS C:\Users\test> $a = 123
PS C:\Users\test> $a.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     Int32                                    System.ValueType
```

```
PS C:\Users\test> $a | Get-Member


   TypeName: System.Int32

Name        MemberType Definition
----        ---------- ----------
CompareTo   Method     int CompareTo(System.Object value), int CompareTo(int value), int IComparable.CompareTo(System.Object obj), int IComparable[int].CompareTo(int other)
Equals      Method     bool Equals(System.Object obj), bool Equals(int obj), bool IEquatable[int].Equals(int other)
GetHashCode Method     int GetHashCode()
GetType     Method     type GetType()
GetTypeCode Method     System.TypeCode GetTypeCode(), System.TypeCode IConvertible.GetTypeCode()
ToBoolean   Method     bool IConvertible.ToBoolean(System.IFormatProvider provider)
ToByte      Method     byte IConvertible.ToByte(System.IFormatProvider provider)
ToChar      Method     char IConvertible.ToChar(System.IFormatProvider provider)
ToDateTime  Method     datetime IConvertible.ToDateTime(System.IFormatProvider provider)
ToDecimal   Method     decimal IConvertible.ToDecimal(System.IFormatProvider provider)
ToDouble    Method     double IConvertible.ToDouble(System.IFormatProvider provider)
ToInt16     Method     int16 IConvertible.ToInt16(System.IFormatProvider provider)
ToInt32     Method     int IConvertible.ToInt32(System.IFormatProvider provider)
ToInt64     Method     long IConvertible.ToInt64(System.IFormatProvider provider)
ToSByte     Method     sbyte IConvertible.ToSByte(System.IFormatProvider provider)
ToSingle    Method     float IConvertible.ToSingle(System.IFormatProvider provider)
ToString    Method     string ToString(), string ToString(string format), string ToString(System.IFormatProvider provider), string ToString(string format, System.IFormatProvider provider), string IFormattable.ToString(string format, System.IFormatProvider formatProvider), string IConvertible.ToS...
ToType      Method     System.Object IConvertible.ToType(type conversionType, System.IFormatProvider provider)
ToUInt16    Method     uint16 IConvertible.ToUInt16(System.IFormatProvider provider)
ToUInt32    Method     uint32 IConvertible.ToUInt32(System.IFormatProvider provider)
ToUInt64    Method     uint64 IConvertible.ToUInt64(System.IFormatProvider provider)
```

**String**

```
PS C:\Users\test> $a = "hello"
PS C:\Users\test> $a.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     String                                   System.Object
```

```
PS C:\Users\test> $a | Get-Member


   TypeName: System.String

Name             MemberType            Definition
----             ----------            ----------
Clone            Method                System.Object Clone(), System.Object ICloneable.Clone()
CompareTo        Method                int CompareTo(System.Object value), int CompareTo(string strB), int IComparable.CompareTo(System.Object obj), int IComparable[string].CompareTo(string other)
Contains         Method                bool Contains(string value)
CopyTo           Method                void CopyTo(int sourceIndex, char[] destination, int destinationIndex, int count)
EndsWith         Method                bool EndsWith(string value), bool EndsWith(string value, System.StringComparison comparisonType), bool EndsWith(string value, bool ignoreCase, cultureinfo culture)
Equals           Method                bool Equals(System.Object obj), bool Equals(string value), bool Equals(string value, System.StringComparison comparisonType), bool IEquatable[string].Equals(string other)
GetEnumerator    Method                System.CharEnumerator GetEnumerator(), System.Collections.IEnumerator IEnumerable.GetEnumerator(), System.Collections.Generic.IEnumerator[char] IEnumerable[char].GetEnumerator()
GetHashCode      Method                int GetHashCode()
GetType          Method                type GetType()
GetTypeCode      Method                System.TypeCode GetTypeCode(), System.TypeCode IConvertible.GetTypeCode()
IndexOf          Method                int IndexOf(char value), int IndexOf(char value, int startIndex), int IndexOf(char value, int startIndex, int count), int IndexOf(string value), int IndexOf(string value, int startIndex), int IndexOf(string value, int startIndex, int count), int IndexOf(str...
IndexOfAny       Method                int IndexOfAny(char[] anyOf), int IndexOfAny(char[] anyOf, int startIndex), int IndexOfAny(char[] anyOf, int startIndex, int count)
Insert           Method                string Insert(int startIndex, string value)
IsNormalized     Method                bool IsNormalized(), bool IsNormalized(System.Text.NormalizationForm normalizationForm)
LastIndexOf      Method                int LastIndexOf(char value), int LastIndexOf(char value, int startIndex), int LastIndexOf(char value, int startIndex, int count), int LastIndexOf(string value), int LastIndexOf(string value, int startIndex), int LastIndexOf(string value, int startIndex, int...
LastIndexOfAny   Method                int LastIndexOfAny(char[] anyOf), int LastIndexOfAny(char[] anyOf, int startIndex), int LastIndexOfAny(char[] anyOf, int startIndex, int count)
Normalize        Method                string Normalize(), string Normalize(System.Text.NormalizationForm normalizationForm)
PadLeft          Method                string PadLeft(int totalWidth), string PadLeft(int totalWidth, char paddingChar)
PadRight         Method                string PadRight(int totalWidth), string PadRight(int totalWidth, char paddingChar)
Remove           Method                string Remove(int startIndex, int count), string Remove(int startIndex)
Replace          Method                string Replace(char oldChar, char newChar), string Replace(string oldValue, string newValue)
Split            Method                string[] Split(Params char[] separator), string[] Split(char[] separator, int count), string[] Split(char[] separator, System.StringSplitOptions options), string[] Split(char[] separator, int count, System.StringSplitOptions options), string[] Split(string[...
StartsWith       Method                bool StartsWith(string value), bool StartsWith(string value, System.StringComparison comparisonType), bool StartsWith(string value, bool ignoreCase, cultureinfo culture)
Substring        Method                string Substring(int startIndex), string Substring(int startIndex, int length)
ToBoolean        Method                bool IConvertible.ToBoolean(System.IFormatProvider provider)
ToByte           Method                byte IConvertible.ToByte(System.IFormatProvider provider)
ToChar           Method                char IConvertible.ToChar(System.IFormatProvider provider)
ToCharArray      Method                char[] ToCharArray(), char[] ToCharArray(int startIndex, int length)
ToDateTime       Method                datetime IConvertible.ToDateTime(System.IFormatProvider provider)
ToDecimal        Method                decimal IConvertible.ToDecimal(System.IFormatProvider provider)
ToDouble         Method                double IConvertible.ToDouble(System.IFormatProvider provider)
ToInt16          Method                int16 IConvertible.ToInt16(System.IFormatProvider provider)
ToInt32          Method                int IConvertible.ToInt32(System.IFormatProvider provider)
ToInt64          Method                long IConvertible.ToInt64(System.IFormatProvider provider)
ToLower          Method                string ToLower(), string ToLower(cultureinfo culture)
ToLowerInvariant Method                string ToLowerInvariant()
ToSByte          Method                sbyte IConvertible.ToSByte(System.IFormatProvider provider)
ToSingle         Method                float IConvertible.ToSingle(System.IFormatProvider provider)
ToString         Method                string ToString(), string ToString(System.IFormatProvider provider), string IConvertible.ToString(System.IFormatProvider provider)
ToType           Method                System.Object IConvertible.ToType(type conversionType, System.IFormatProvider provider)
ToUInt16         Method                uint16 IConvertible.ToUInt16(System.IFormatProvider provider)
ToUInt32         Method                uint32 IConvertible.ToUInt32(System.IFormatProvider provider)
ToUInt64         Method                uint64 IConvertible.ToUInt64(System.IFormatProvider provider)
ToUpper          Method                string ToUpper(), string ToUpper(cultureinfo culture)
ToUpperInvariant Method                string ToUpperInvariant()
Trim             Method                string Trim(Params char[] trimChars), string Trim()
TrimEnd          Method                string TrimEnd(Params char[] trimChars)
TrimStart        Method                string TrimStart(Params char[] trimChars)
Chars            ParameterizedProperty char Chars(int index) {get;}
Length           Property              int Length {get;}

```

**Array**

```
PS C:\Users\test> $a = 1,2,3
PS C:\Users\test> $a.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     Object[]                                 System.Array

```

```
PS C:\Users\test> $a | Get-Member


   TypeName: System.String

Name             MemberType            Definition
----             ----------            ----------
Clone            Method                System.Object Clone(), System.Object ICloneable.Clone()
CompareTo        Method                int CompareTo(System.Object value), int CompareTo(string strB), int IComparable.CompareTo(System.Object obj), int IComparable[string].CompareTo(string other)
Contains         Method                bool Contains(string value)
CopyTo           Method                void CopyTo(int sourceIndex, char[] destination, int destinationIndex, int count)
EndsWith         Method                bool EndsWith(string value), bool EndsWith(string value, System.StringComparison comparisonType), bool EndsWith(string value, bool ignoreCase, cultureinfo culture)
Equals           Method                bool Equals(System.Object obj), bool Equals(string value), bool Equals(string value, System.StringComparison comparisonType), bool IEquatable[string].Equals(string other)
GetEnumerator    Method                System.CharEnumerator GetEnumerator(), System.Collections.IEnumerator IEnumerable.GetEnumerator(), System.Collections.Generic.IEnumerator[char] IEnumerable[char].GetEnumerator()
GetHashCode      Method                int GetHashCode()
GetType          Method                type GetType()
GetTypeCode      Method                System.TypeCode GetTypeCode(), System.TypeCode IConvertible.GetTypeCode()
IndexOf          Method                int IndexOf(char value), int IndexOf(char value, int startIndex), int IndexOf(char value, int startIndex, int count), int IndexOf(string value), int IndexOf(string value, int startIndex), int IndexOf(string value, int startIndex, int count), int IndexOf(str...
IndexOfAny       Method                int IndexOfAny(char[] anyOf), int IndexOfAny(char[] anyOf, int startIndex), int IndexOfAny(char[] anyOf, int startIndex, int count)
Insert           Method                string Insert(int startIndex, string value)
IsNormalized     Method                bool IsNormalized(), bool IsNormalized(System.Text.NormalizationForm normalizationForm)
LastIndexOf      Method                int LastIndexOf(char value), int LastIndexOf(char value, int startIndex), int LastIndexOf(char value, int startIndex, int count), int LastIndexOf(string value), int LastIndexOf(string value, int startIndex), int LastIndexOf(string value, int startIndex, int...
LastIndexOfAny   Method                int LastIndexOfAny(char[] anyOf), int LastIndexOfAny(char[] anyOf, int startIndex), int LastIndexOfAny(char[] anyOf, int startIndex, int count)
Normalize        Method                string Normalize(), string Normalize(System.Text.NormalizationForm normalizationForm)
PadLeft          Method                string PadLeft(int totalWidth), string PadLeft(int totalWidth, char paddingChar)
PadRight         Method                string PadRight(int totalWidth), string PadRight(int totalWidth, char paddingChar)
Remove           Method                string Remove(int startIndex, int count), string Remove(int startIndex)
Replace          Method                string Replace(char oldChar, char newChar), string Replace(string oldValue, string newValue)
Split            Method                string[] Split(Params char[] separator), string[] Split(char[] separator, int count), string[] Split(char[] separator, System.StringSplitOptions options), string[] Split(char[] separator, int count, System.StringSplitOptions options), string[] Split(string[...
StartsWith       Method                bool StartsWith(string value), bool StartsWith(string value, System.StringComparison comparisonType), bool StartsWith(string value, bool ignoreCase, cultureinfo culture)
Substring        Method                string Substring(int startIndex), string Substring(int startIndex, int length)
ToBoolean        Method                bool IConvertible.ToBoolean(System.IFormatProvider provider)
ToByte           Method                byte IConvertible.ToByte(System.IFormatProvider provider)
ToChar           Method                char IConvertible.ToChar(System.IFormatProvider provider)
ToCharArray      Method                char[] ToCharArray(), char[] ToCharArray(int startIndex, int length)
ToDateTime       Method                datetime IConvertible.ToDateTime(System.IFormatProvider provider)
ToDecimal        Method                decimal IConvertible.ToDecimal(System.IFormatProvider provider)
ToDouble         Method                double IConvertible.ToDouble(System.IFormatProvider provider)
ToInt16          Method                int16 IConvertible.ToInt16(System.IFormatProvider provider)
ToInt32          Method                int IConvertible.ToInt32(System.IFormatProvider provider)
ToInt64          Method                long IConvertible.ToInt64(System.IFormatProvider provider)
ToLower          Method                string ToLower(), string ToLower(cultureinfo culture)
ToLowerInvariant Method                string ToLowerInvariant()
ToSByte          Method                sbyte IConvertible.ToSByte(System.IFormatProvider provider)
ToSingle         Method                float IConvertible.ToSingle(System.IFormatProvider provider)
ToString         Method                string ToString(), string ToString(System.IFormatProvider provider), string IConvertible.ToString(System.IFormatProvider provider)
ToType           Method                System.Object IConvertible.ToType(type conversionType, System.IFormatProvider provider)
ToUInt16         Method                uint16 IConvertible.ToUInt16(System.IFormatProvider provider)
ToUInt32         Method                uint32 IConvertible.ToUInt32(System.IFormatProvider provider)
ToUInt64         Method                uint64 IConvertible.ToUInt64(System.IFormatProvider provider)
ToUpper          Method                string ToUpper(), string ToUpper(cultureinfo culture)
ToUpperInvariant Method                string ToUpperInvariant()
Trim             Method                string Trim(Params char[] trimChars), string Trim()
TrimEnd          Method                string TrimEnd(Params char[] trimChars)
TrimStart        Method                string TrimStart(Params char[] trimChars)
Chars            ParameterizedProperty char Chars(int index) {get;}
Length           Property              int Length {get;}


```

**Hash**
```
PS C:\Users\test> $a.GetType()

IsPublic IsSerial Name                                     BaseType
-------- -------- ----                                     --------
True     True     Hashtable                                System.Object


```

```
PS C:\Users\test> $a | Get-Member


   TypeName: System.Collections.Hashtable

Name              MemberType            Definition
----              ----------            ----------
Add               Method                void Add(System.Object key, System.Object value), void IDictionary.Add(System.Object key, System.Object value)
Clear             Method                void Clear(), void IDictionary.Clear()
Clone             Method                System.Object Clone(), System.Object ICloneable.Clone()
Contains          Method                bool Contains(System.Object key), bool IDictionary.Contains(System.Object key)
ContainsKey       Method                bool ContainsKey(System.Object key)
ContainsValue     Method                bool ContainsValue(System.Object value)
CopyTo            Method                void CopyTo(array array, int arrayIndex), void ICollection.CopyTo(array array, int index)
Equals            Method                bool Equals(System.Object obj)
GetEnumerator     Method                System.Collections.IDictionaryEnumerator GetEnumerator(), System.Collections.IDictionaryEnumerator IDictionary.GetEnumerator(), System.Collections.IEnumerator IEnumerable.GetEnumerator()
GetHashCode       Method                int GetHashCode()
GetObjectData     Method                void GetObjectData(System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingContext context), void ISerializable.GetObjectData(System.Runtime.Serialization.SerializationInfo info, System.Runtime.Serialization.StreamingCont...
GetType           Method                type GetType()
OnDeserialization Method                void OnDeserialization(System.Object sender), void IDeserializationCallback.OnDeserialization(System.Object sender)
Remove            Method                void Remove(System.Object key), void IDictionary.Remove(System.Object key)
ToString          Method                string ToString()
Item              ParameterizedProperty System.Object Item(System.Object key) {get;set;}
Count             Property              int Count {get;}
IsFixedSize       Property              bool IsFixedSize {get;}
IsReadOnly        Property              bool IsReadOnly {get;}
IsSynchronized    Property              bool IsSynchronized {get;}
Keys              Property              System.Collections.ICollection Keys {get;}
SyncRoot          Property              System.Object SyncRoot {get;}
Values            Property              System.Collections.ICollection Values {get;}


```
