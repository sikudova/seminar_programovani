# Cvičení 38: `char`

**Cíl:** naučit se používat datový typ `char`

Typ `char` (zkratka z `character`) slouží k uložení jednoho jediného znaku (písmeno, číslice, symbol, mezera).

Hodnoty se píšou do jednoduchých uvozovek `''`.

Zabírá v paměti 2 bajty – _it represents a **Unicode UTF-16** code unit, typically a UTF-16 character_.

```csharp
char letter = 'A';
char digit = '9';
char symbol = '$';
char czechChar = 'ř';
```

_The char type represents unsigned 16-bit integers with values **from 0 to 65535**, inclusive, as a **UTF-16** code unit._

## `char` jako celá čísla

`char` se implicitně konvertuje na celočíselný datový typ `int` (i další), protože obsahuje **číselný kód** znaku (charakteru).

Více o konverzi `char`: [C# Char Conversions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/char#conversions)

Ke konverzi se používá ASCII/Unicode kód tabulka: [tabulka](https://symbl.cc/en/unicode-table/).

### Explicitní přetypování

Při **explicitním přetypování** `char` na `int` C# vrací číselnou hodnotu, kterou má znak v tabulce.

```csharp
char letter = 'A';
int asciiCode = (int)letter; // Výsledek je 65
```

Číslo reprezentující ASCII/Unicode kód je možné přetypovat na `char`:

```csharp
int code = 65;
char character = (char)code; // Výsledek je 'A'
```

### Unicode sekvence `\u`
_a Unicode escape sequence, which is '\u' followed by the four-symbol hexadecimal representation of a character code_

Hodnotu je možné zadat také pomocí **čtyřmístného hexadecimálního kódu** v tabulce Unicode s předponou **'\u'**:

```csharp
char letter = '\u006A';
Console.WriteLine(letter); // výsledek je 'j'
```

### Hexadecimální sekvennce `\x`
_a hexadecimal escape sequence, which is `\x` followed by the hexadecimal representation of a character code_

Hodnotu je možné zadat také pomocí **hexadecimálního kódu** (může se zkracovat) v tabulce Unicode s předponou **'\x'**:

```csharp
char letter = '\x006A';
Console.WriteLine(letter); // výsledek je 'j'
```

## Metody na `char`

Seznam metod na datovém typu `char`: [`char` metody](https://learn.microsoft.com/en-us/dotnet/api/system.char?view=net-10.0#methods).

Níže jsou uvedené často používané metody.

### `CompareTo(Char)`
C# dokumentace: [CompareTo](https://learn.microsoft.com/en-us/dotnet/api/system.char.compareto?view=net-10.0)

```csharp
public int CompareTo(char value);
```

_Compares this instance to a specified Char object and indicates whether this instance precedes, follows, or appears in the same position in the sort order as the specified Char object._

| Return Value | Description |
| :--- | :--- |
| Less than zero | This instance precedes `value`. |
| Zero | This instance has the same position in the sort order as `value`. |
| Greater than zero | This instance follows `value`. |


### `Equals(Char)`
C# dokumentace: [Equals](https://learn.microsoft.com/en-us/dotnet/api/system.char.equals?view=net-10.0)

```csharp
public bool Equals(char obj);
```

_Returns a value that indicates whether this instance is equal to the specified Char object._

_Returns `true` if the obj parameter equals the value of this instance; otherwise, `false`._


### `IsDigit(Char)`
C# dokumentace: [Equals](https://learn.microsoft.com/en-us/dotnet/api/system.char.isdigit?view=net-10.0)

```csharp
public static bool IsDigit(char c);
```

_Indicates whether a Unicode character is categorized as a decimal digit._

_Returns `true` if `c` is a decimal digit; otherwise, `false`._

### `IsLetter(Char)`
C# dokumentace: [Equals](https://learn.microsoft.com/en-us/dotnet/api/system.char.isletter?view=net-10.0)

```csharp
public static bool IsLetter(char c);
```

_Indicates whether the specified Unicode character is categorized as a Unicode letter._

_Returns `true` if `c` is a letter; otherwise, `false`._

### `IsLetterOrDigit(Char)`
C# dokumentace: [Equals](https://learn.microsoft.com/en-us/dotnet/api/system.char.isletterordigit?view=net-10.0)

```csharp
public static bool IsLetterOrDigit(char c);
```

_Indicates whether the specified Unicode character is categorized as a letter or a decimal digit._

_Returns `true` if `c` is a letter or a decimal digit; otherwise, `false`._


### `ToString(Char)`
C# dokumentace: [Equals](https://learn.microsoft.com/en-us/dotnet/api/system.char.tostring?view=net-10.0)

```csharp
public static string ToString(char c);
```

_Converts the specified Unicode character to its equivalent string representation._

_Returns the string representation of the value of `c`._
