# Cvičení 20: cykly – `for` cyklus 

**Cíl:** naučit se řídit program pomocí `for` cyklu – opakovat část kódu několikrát

## Cykly obecně

Cyklus (`loop`) je struktura, která umožňuje opakovaně provádět posloupnost příkazů. Opakování i ukončení cyklu se řídí nějakou podmínkou.

Typy cyklů:
* `for` cyklus,
* `while-do` cyklus,
* `do-while` cyklus,
* nekonečný cyklus.

K opakování používáme také pojem **iterace**.

_The statements are executed sequentially: The first statement in a function is executed first, followed by the second, and so on._

## `for` cyklus

`for` cyklus používáme, známe-li předem počet opakování, např. při procházení posloupnosti hodnot (interval celých čísel).

_The C# for loop is a repetition control structure that executes a block of code a specific number of times instead of writing the same code multiple times. It is especially useful when the number of iterations is known in advance._

Syntax `for` cyklu je následující:

```csharp
for ( init; condition; increment ) {
   statement(s);
}
```

<img width="300" alt="for_loop_flow_diagram" src="https://github.com/user-attachments/assets/33febc42-f189-4bdd-95e4-f1bc9393f345" />


Příklad jednoduchého `for` cyklu:

```csharp
/* for loop execution */
 for (int a = 10; a < 20; a = a + 1) {
    Console.WriteLine("value of a: {0}", a);
 }
 Console.ReadLine();
```
