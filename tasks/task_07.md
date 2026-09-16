# Cvičení 07: podmínky, větvení

**Cíl:** naučit se větvit program pomocí podmínek (`if`, `else`)

## 1. `if` aneb když

Pokud je podmínka v závorce pravdivá (`True`), provede se kód uvnitř složených závorek `{ ... }`. Pokud je nepravdivá, kód se jednoduše přeskočí.

```csharp
int age = 16;

if (age >= 18)
{
    Console.WriteLine("Jsi plnoletý, juchů.");
}
```
_Pokud bude v proměnné `age` číslo 20, text se vypíše. Pokud tam bude 16, program neudělá nic._

## 2. `if ... else` aneb dvě možnosti

V mnoha situacích je potřeba rozdělit program na 2 části: když platí nějaká podmínka, nebo když neplatí.

Pokud je podmínka pravdivá, provede se kód ve větvi `if`, jinak se provede kód ve větvi `else`.

```csharp
Console.Write("Zadej svůj věk: ");
int age = Convert.ToInt32(Console.ReadLine());

if (age >= 18)
{
    Console.WriteLine("Jsi dospělý, můžeš dál!");
}
else
{
    Console.WriteLine("Je mi líto, jsi stále moc mladý.");
}
```

## 3. Více možností za sebou: `else if`
Pokud chceme vybírat z více než dvou možností, propojíme podmínky pomocí konstrukce `else if`.

C# vyhodnocuje jednotlivé podmínky v pořadí a provede první blok, jehož podmínka je pravdivá, a zbytek přeskočí.

Poslední `else` zpracuje všechny zbývající případy.

```csharp
int score = 75;

if (score >= 90)
{
    Console.WriteLine("Známka: 1 (Výborně)");
}
else if (score >= 75)
{
    Console.WriteLine("Známka: 2 (Chvalitebně)");
}
else if (score >= 50)
{
    Console.WriteLine("Známka: 3 (Dobře)");
}
else
{
    Console.WriteLine("Nedostatečně, musíš se to doučit.");
}
```
