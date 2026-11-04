# Cvičení 45: jednoduché metody

**Cíl:** procvičení tvorby metod

## Čára

Napiš metodu, která vypíše čáru. Tuto čáru budeme používat k oddělování jednotlivých výstupu tohoto cvičení. Jelikož tato metoda nic nevrací, návratový typ je `void`.

```csharp
static void Line();
```
## Pozdrav uživatele

Napiš metodu, která pozdraví uživatele. Potom vytvoř další metodu, která pozdraví uživatele jménem.

```csharp
static void SayHello();
static void GreetUser(string name);
```

## Ověření sudosti a lichosti čísla

Napiš metody, které ověří, zda je zadané číslo sudé/liché. K návratu hodnoty se používá klíčové slovo `return`.

```csharp
static bool IsEven(int number);
static bool IsOdd(int number);
```

## Obsah a obvod obdélníku

Napiš metody pro výpočet obvodu a obsahu obdélníku.

```csharp
static double CalculateRectangleArea(double height, double width);
static double CalculateRectanglePerimeter(double height, double width);
```

## Větší číslo

Napiš metodu, která ze dvou celých čísel vrátí to větší z nich.

```csharp
static int GetMaximum(int a, int b);
```
