# Cvičení 32: `do-while` cyklus 

**Cíl:** naučit se řídit program pomocí `do-while` cyklu

## `do-while` cyklus

Zatímco obyčejný `while` cyklus nejdříve kontroluje podmínku a teprve potom provádí kód uvnitř (takže se může stát, že se kód nespustí ani jednou), `do-while` cyklus funguje opačně:
* Nejprve proběhne kód uvnitř bloku `do { ... }`.
* Teprve na konci se vyhodnotí podmínka v závorce za `while (...)`.

Pokud je podmínka `true`, cyklus se opakuje. Pokud je `false`, cyklus končí.

**Hlavní vlastnost:** Tělo `do-while` cyklu se vždy provede minimálně jednou, bez ohledu na to, jaká je počáteční podmínka.

Syntax `do-while` cyklu je následující:

```csharp
do {
   statement(s);
} while( condition );
```

<p align="center">
   <img width="300" alt="while_do_loop_flow_diagram" src="https://www.tutorialspoint.com/csharp/images/cpp_do_while_loop.jpg" />
</p>

Příklad jednoduchého `do-while` cyklu:

```csharp
/* local variable definition */
int a = 10;

/* do loop execution */
do {
  Console.WriteLine("value of a: {0}", a);
  a = a + 1;
} 
while (a < 20);
Console.ReadLine();
```

### Aplikace `while-do` cyklu
* načítání vstupu do splnění podmínky,
* validace vstupu pomocí cyklu.
