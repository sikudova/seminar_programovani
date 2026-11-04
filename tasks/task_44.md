# Cvičení 44: metody

**Cíl:** naučit se dělit kód do metod

Metody umožňují kód rozsekat na menší, přehledné a opakovaně použitelné části.

Zjednodušeně metoda: můžu jí dát nějaké vstupy, metoda provede operace, (něco spočítá/udělá), může mi vrátit výsledek.

V jiných programovacích jazycích se setkáváme s pojmem **funkce**. V C# používáme pojem **metoda**, jelikož je objektově orientovaný jazyk – kód nemůže být jen tak někde (vysvětlíme si později u OOP).

_Methods, also called functions, are a key part of keeping code structured, efficient, and readable. A method is a modular **unit of code**, and a fundamental programming concept. A method is often designed to perform a specific task and contains code to execute that task. The **name** of a method should clearly **reflect its task**, which improves code readability. Learning how to use methods will help you build feature-rich applications more quickly._

## Struktura metody

Základem metody je její název, návratová hodnota (co metoda vrací) a její parametry (co metodě dáme na vstup) = signature metody. 

```csharp
[návratový_typ] [NázevMetody]([parametry])
{
    // Tělo metody (kód, který se provede)
    return [výsledek]; // (pokud metoda něco vrací)
}
```

Z názvu metody by mělo být jasné, co dělá (např. `calculateAge`, `calculateRectangleArea`, `isAdult` atd.).

Metoda může vracet hodnoty různého datového typu (`bool`, `int`, `double` atd.), ale také nemusí vracet nic, jen něco provede. V tomto případě je návratovým typem `void`.

Parametry metody jsou uvedeny v závorce. Parametrů může být více, nemusí mít ale žádný (prázdné závorky).

Příklad signature metody (její deklarace):

```csharp
void SayHello();
```

Funkce nevrací nic (`void`), má název `SayHello` a nebere na vstup žádný parametr.

## Definice a použití metody

K definici metody používáme složené závorky `{}`, např.:

```csharp
void SayHello() 
{
    Console.WriteLine("Hello World!");
}
```

Tato metoda vypíše text `Hello World`.

K použití metody ji musíme zavolat (_call a method_). Metodu voláme pomocí jejího jména a potřebných parametrů. Metodu můžeme zavolat před i po její definic.

```csharp
SayHello();

void SayHello() 
{
    Console.WriteLine("Hello World!");
}
```

Jakmile je metoda zavolána, začne se provádět kód uvnitř ní. Jakmile je běh kódu dokončen, vrací se zpátky do místa, kde byla zavolána.

```csharp
Console.WriteLine("Before calling a method");
SayHello();
Console.WriteLine("After calling a method");

void SayHello() 
{
    Console.WriteLine("Hello World!");
}
```
```text
Before calling a method
Hello World!
After calling a method
```

## Best Practices u metod
* Název metody odráží to, co metoda dělá.
* Názvy metod používají tzv. `PascalCase` styl (např. `DisplayDate`, `ShowData`).
* Názvy parametrů popisují to, co parametry reprezentují.
```csharp
void ShowData(string a, int b, int c);
void DisplayDate(string month, int day, int year);
```
