# Cvičení 17: zaokrouhlování

**Cíl:** pochopit základní metody pro zaokrouhlování desetinných čísel

Když potřebujeme desetinné číslo zaokrouhlit na určitý počet míst/na nejbližší celé číslo, používáme metodu `Math.Round()`.

Další metody pro zaokrouhlování jsou `Math.Floor()` a `Math.Ceiling()`.

## `Math.Round()`

Kuk: [C# Math.Round](https://learn.microsoft.com/en-us/dotnet/api/system.math.round?view=net-10.0)

Zaokrouhlí hodnotu na nejbližší celé číslo nebo na zadaný počet desetinných číslic.

### `Round(Double)`
Kuk: [Round(Double)](https://learn.microsoft.com/en-us/dotnet/api/system.math.round?view=net-10.0#system-math-round(system-double))

Rounds a double-precision floating-point value to the **nearest integral value**, and rounds midpoint values to the nearest even number.

### `Round(Double, Int32)`
Kuk: [Round(Double, Int32)](https://learn.microsoft.com/en-us/dotnet/api/system.math.round?view=net-10.0#system-math-round(system-double-system-int32))

Rounds a double-precision floating-point value to a **specified number of fractional digits**, and rounds midpoint values to the nearest even number.

### `Round(Double, Int32, MidpointRounding)`
Kuk: [Round(Double, Int32, MidpointRounding)](https://learn.microsoft.com/en-us/dotnet/api/system.math.round?view=net-10.0#system-math-round(system-double-system-int32-system-midpointrounding))

Rounds a double-precision floating-point value to a specified number of fractional digits **using the specified [rounding convention](https://learn.microsoft.com/en-us/dotnet/api/system.midpointrounding?view=net-10.0)**.

```csharp
double price = 45.6789;

// Zaokrouhlení na celé číslo
double rounded1 = Math.Round(price); // Výsledek: 46

// Zaokrouhlení na 2 desetinná místa
double rounded2 = Math.Round(price, 2); // Výsledek: 45,68
```

## `Math.Ceiling()`

Kuk: [Math.Ceiling](https://learn.microsoft.com/en-us/dotnet/api/system.math.ceiling?view=net-10.0)

Returns the smallest integral value greater than or equal to the specified number.

## `Math.Floor()`

Kuk: [Math.Floor](https://learn.microsoft.com/en-us/dotnet/api/system.math.floor?view=net-10.0)

Returns the largest integral value less than or equal to the specified number.

| Value | Ceiling | Floor |
| :---: | :---: | :---: |
| 7.03 | 8 | 7 |
| 7.64 | 8 | 7 |
| 0.12 | 1 | 0 |
| -0.12 | 0 | -1 |
| -7.1 | -7 | -8 |
| -7.6 | -7 | -8 |

# Zaokrouhlovací chyby
Zkuste následující kód:

```csharp
double a = 0.1;
double b = 0.2;
double sum = a + b;

Console.WriteLine(sum); // 0,30000000000000004
```

Počítač má v paměti omezené místo, takže nekonečný binární zápis musí někde „uříznout“. Tím vznikne drobná nepřesnost – a ta se při sčítání kumuluje.

Podmínka `if (sum == 0.3)` může tedy klidně vyjít jako `false`.

Místo toho kontrolujeme, jestli je rozdíl menší než nějaká miniaturní odchylka (tzv. epsilon):

```csharp
// Zjišťujeme, jestli je to "skoro 0.3"
if (Math.Abs(sum - 0.3) < 0.00001) 
{
    Console.WriteLine("Je to 0.3!");
}
```

Kuk: [C# Double vs Decimal: Key Differences Explained](https://medium.com/@anushananu343/c-double-vs-decimal-key-differences-explained-823221bb2e83)
