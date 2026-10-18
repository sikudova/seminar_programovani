# Cvičení 37: sčítačka kladných čísel

**Cíl:** procvičení příkazů `break` a `continue`

Napiš program, který se bude v nekonečném (`while (true)`) cyklu opakovaně ptát uživatele na zadání celého čísla. S tímto číslem nalož následovně:
* **Ukončení (`break`):** Pokud uživatel zadá `0`, cyklus se okamžitě ukončí (program se rozloučí a vypíše výsledky).
* **Přeskočení (`continue`):** Pokud uživatel zadá záporné číslo, program ho ignoruje, vypíše varování, že záporná čísla se nepočítají, a pomocí `continue` přeskočí zbytek kódu na začátek dalšího cyklu.
* **Zpracování:** Pokud je číslo kladné, přičti ho ke kumulativnímu součtu a zvedni počítadlo platných čísel.

```text
Welcome to intelligent sumator.
Enter a positive number (0 for exit): 1
Added number 1.
Enter a positive number (0 for exit): 2
Added number 2.
Enter a positive number (0 for exit): 3
Added number 3.
Enter a positive number (0 for exit): -5
Negative numbers are ignored.
Enter a positive number (0 for exit): -8
Negative numbers are ignored.
Enter a positive number (0 for exit): 5
Added number 5.
Enter a positive number (0 for exit): 0
Exiting the loop...
------------------------
Loop terminated.
Total valid numbers entered: 4.
Total sum of valid numbers: 11.
```
