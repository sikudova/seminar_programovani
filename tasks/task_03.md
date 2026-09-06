# Cvičení 03: vstup od uživatele

**Cíl:** naučit se načítat vstup od uživatele pomocí `Console.ReadLine()` a převádět ho na čísla (`int`)

## 1. Načítání vstupu z konzole

Pro načítání textu od uživatele (z konzole) používáme v C# příkaz `Console.ReadLine()`.

```csharp
string userInput = Console.ReadLine();
```

**❗Důležité:**

`Console.ReadLine()` **VŽDY** vrací datový typ `string` (text).

I když uživatel na klávesnici zadá číslo (např. `42`), program jej načte jako textový řetězec `"18"`. S tímto textem nelze provádět matematické operace (např. sčítání nebo násobení).

```csharp
// CHYBA - Kód nejde zkompilovat:
int age = Console.ReadLine(); 

// CHYBA - Provede se spojení textů ("18" + "1" = "181"), nikoliv matematický součet:
string input = Console.ReadLine(); // Uživatel zadal 18
Console.WriteLine(input + 1);      // Vypíše "181"
```

## 2. Převod textu na číslo (Parsing & Conversion)

Abychom mohli se zadaným číslem počítat, musíme `string` převést (konvertovat) na typ `int`/`double`/jiný číselný typ. K tomu se nejčastěji používají metody:
* `int.Parse()`,
* `Convert.ToInt32()`/`Convert.ToDouble()`/`Convert.To___()`.

### `int.Parse`
Metoda `int.Parse` převádí textový řetězec přímo na celé číslo (`string` → `int`).

Pokud nelze řetězec parsovat jako celé číslo, metoda `int.Parse` vyvolá výjimku `FormatException`. Je doporučeno tuto výjimku zpracovat (probereme později, teď neřešíme).

Vrací 32bitové celé číslo se znaménkem, které odpovídá číslu obsaženému v řetězci.

```csharp
Console.Write("Enter your age: ");
string inputAge = Console.ReadLine();
int age = int.Parse(inputAge); // converts string to int
Console.WriteLine("Your age is " + age);
```

### `Convert.ToInt32()`
Metoda `Convert.ToInt32(string value)` převádí zadanou hodnotu `value` na 32bitové celé číslo se znaménkem.

V případě `null` vrací `0`.

V případě prázdného řetězce nebo hodnoty mimo povolený rozsah vyvolává metoda výjimky (probereme později, teď neřešíme).

```csharp
Console.Write("Enter your age: ");
inputAge = Console.ReadLine();
age = Convert.ToInt32(inputAge); // converts string to int
Console.WriteLine("your age is " + age);
```

### `Convert.ToDouble()`
Metoda `Convert.ToDouble()` převádí zadanou hodnotu `value` na desetinné číslo typu `double`.

V případě `null` vrací `0`.

V případě prázdného řetězce nebo hodnoty mimo povolený rozsah vyvolává metoda výjimky (probereme později, teď neřešíme).

```csharp
Console.Write("Enter a value: ");
string inputValue = Console.ReadLine();
double value = Convert.ToDouble(inputValue); // converts string to double
Console.WriteLine("Your value is " + value);
```
