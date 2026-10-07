# Cvičení 23: vnořený `for` cyklus (grafika)

**Cíl:** naučit se vnořovat `for` cykly

## Vnořené `for` cykly (nested `for` loops)

Vnořený cyklus je situace, kdy se uvnitř těla jednoho cyklu (vnějšího) nachází celý další cyklus (vnitřní).

_The "inner loop" will be executed one time for each iteration of the "outer loop":_

```csharp
// Outer loop
for (int i = 1; i <= 2; ++i) 
{
  Console.WriteLine("Outer: " + i);  // Executes 2 times

  // Inner loop
  for (int j = 1; j <= 3; j++) 
  {
    Console.WriteLine(" Inner: " + j); // Executes 6 times (2 * 3)
  }
}
```

```text
Outer: 1
 Inner: 1
 Inner: 2
 Inner: 3
Outer: 2
 Inner: 1
 Inner: 2
 Inner: 3
```

## Vykreslení obdélníku ze symbolů `#`

Napiš program, který se uživatele zeptá na dva parametry: **šířku** (počet sloupců) a **výšku** (počet řádků).
Pomocí vnořených for cyklů potom program vykreslí obdélník vyplněný symbolem `#`.

```text
Enter the width (number of columns): 7
Enter the height (number of rows): 4

# # # # # # #
# # # # # # #
# # # # # # #
# # # # # # #
```

## Vykreslení prázdného obdélníku
Napiš program, který se uživatele zeptá na šířku a výšku obdélníku.
Program vykreslí obdélník, který má vyplněný pouze okraj pomocí symbolu #, ale uvnitř je prázdný (obsahuje mezery).

```text
Enter the width (number of columns): 8
Enter the height (number of rows): 5

# # # # # # # #
#             #
#             #
#             #
# # # # # # # #
```

## Šachovnice
Napiš program, který se uživatele zeptá na velikost šachovnice ($n$).
Pomocí vnořených cyklů program vykreslí čtvercovou mřížku o rozměrech $n \times n$, kde se symboly `#` a `.` střídají jako na šachovnici.

```text
Enter the size of the chessboard: 8
# . # . # . # .
. # . # . # . #
# . # . # . # .
. # . # . # . #
# . # . # . # .
. # . # . # . #
# . # . # . # .
. # . # . # . #
```
