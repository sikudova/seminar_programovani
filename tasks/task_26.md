# Cvičení 26: `while-do` cyklus 

**Cíl:** naučit se řídit program pomocí `while-do` cyklu – opakovat část kódu dokud je platná podmínka

## `while-do` cyklus

Zatímco `for` cyklus používáme tehdy, když předem víme, kolikrát se má kód opakovat (např. "opakuj 5krát" nebo "projdi pole od začátku do konce"), cyklus `while` se používá v situacích, kdy počet opakování předem neznáme.

Cyklus běží tak dlouho, dokud platí zadaná podmínka (je pravdivá/`true`). Jakmile podmínka přestane platit, cyklus skončí a program pokračuje dál.

_When the condition becomes false, program control passes to the line immediately following the loop._

Syntax `while` cyklu je následující:

```csharp
while (podmínka)
{
    // Tento kód se opakuje, dokud je podmínka true
}
```

<p align="center">
   <img width="300" alt="while_do_loop_flow_diagram" src="https://www.tutorialspoint.com/csharp/images/cpp_while_loop.jpg" />
</p>

**Podmínka na začátku:** Cyklus nejprve zkontroluje podmínku. Pokud je hned napoprvé nepravdivá (false), kód uvnitř se ani jednou nespustí.

**Řídicí proměnná:** U `for` cyklu je inicializace, podmínka i inkrementace pohromadě v závorce. U `while` cyklu se musí řídicí proměnná založit před cyklem a je nutné ji uvnitř cyklu měnit, jinak vznikne nekonečný cyklus!

_Here, key point of the while loop is that the loop might not ever run. When the condition is tested and the result is false, the loop body is skipped and the first statement after the while loop is executed._

Příklad jednoduchého `while-do` cyklu:

```csharp
/* local variable definition */
 int a = 10;

/* while loop execution */
while (a <= 20) {
  Console.WriteLine("value of a: {0}", a);
  a++;
}
Console.ReadLine();
```

### Aplikace `while-do` cyklu
* načítání vstupu do splnění podmínky,
* validace vstupu pomocí cyklu,
* čtení souboru řádek po řádku.
