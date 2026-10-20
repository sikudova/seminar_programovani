# Cvičení 41: procházení řetězce

**Cíl:** naučit se procházet řetězce pomocí cyklů

Jelikož je `string` posloupnost znaků, dá se procházet. K tomu slouží cykly – `foreach`, `for` i `while`.

## `foreach` cyklus
Cyklus `foreach` je cyklus, který slouží k procházení prvků v kolekci (v poli, v řetězci).

Elegantním řešením ke čtení znaků v řetězci je právě tento cyklus – není potřeba řešit indexy a projde přes každý znak.

```csharp
foreach (type variableName in stringName) 
{
  // code block to be executed
}
```

```csharp
string text = "Ahoj";

foreach (char c in text)
{
    Console.WriteLine(c);
}
```

## `for` cyklus
Pokud je potřeba znát index/pozici jednotlivých znaků, lze požít `for` cyklus (např. při porovnávání sousedních znaků).

K procházení řetězce se používá vlastnosti `Length` a indexování `[]`. Důležité je dát si pozor na hranice – aby index nebyl mimo řetězec.

```csharp
string text = "Ahoj";

for (int i = 0; i < text.Length; i++)
{
    Console.WriteLine($"Znak na indexu {i} je {text[i]}");
}
```

## `while` cyklus
Je možné taky použít `while` cyklus – je potřeba si vytvořit řídicí proměnnou a tu inkrementovat.

```csharp
string text = "Ahoj";
int i = 0; 

while (i < text.Length)
{
    Console.WriteLine(text[i]);
    i++;
}
```
