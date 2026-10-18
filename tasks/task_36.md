# Cvičení 26: `break` a `continue` příkazy

**Cíl:** naučit se ukončovat cykly a přeskakovat určité kroky v cyklu

Příkazy `break` a `continue` slouží k přeruší cyklu.

## `break` příkaz

Příkaz break **ukončuje aktuální cyklus**.

Jakmile program narazí na `break`, ignoruje zbytek těla cyklu, už se nevrací k podmínce a pokračuje kódem, který je až za cyklem.

_When the break statement is encountered inside a loop, the loop is immediately terminated and program control resumes at the next statement following the loop._

_It can be used to terminate a case in the switch statement._

**Použití:** Při hledání v cyklu – při nalezení nemá smysl dál hledat (např. hledání konkrétního čísla v řadě).

Syntax `break` je následující:

```csharp
break;
```

<p align="center">
   <img width="300" alt="break_flow_diagram" src="https://www.tutorialspoint.com/csharp/images/cpp_break_statement.jpg" />
</p>

Příklad použití `break` v cyklu:

```csharp
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    break;
  }
  Console.WriteLine(i);
}
```

_Výstup: 0 1 2 3_

## `continue` příkaz

Příkaz `continue` neukončuje celý cyklus, ale okamžitě **ukončí pouze aktuální průchod (iteraci)**. Všechno, co je v těle cyklu za `continue`, se pro daný průchod preskočí a program skočí rovnou na vyhodnocení podmínky (případně na začátek dalšího kroku).

_The continue statement in C# works somewhat like the break statement. Instead of forcing termination, however, continue forces the next iteration of the loop to take place, skipping any code in between._

**Použití:** Při procházení kolekce je potřeba ignorovat/přeskočit určité prvky (např. sudá čísla).

Syntax `continue` je následující:

```csharp
continue;
```

<p align="center">
   <img width="300" alt="continue_flow_diagram" src="https://www.tutorialspoint.com/csharp/images/cpp_continue_statement.jpg" />
</p>

Příklad použití `continue` v cyklu:

```csharp
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    continue;
  }
  Console.WriteLine(i);
}
```

_Výstup: 0 1 2 3 5 6 7 8 9_
