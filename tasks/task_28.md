# Cvičení 28: validace vstupu

**Cíl:** procvičení `while-do` cyklu

Napiš program, který se uživatele zeptá na zadání hodnocení v rozmezí od 1 do 5.

Pomocí klasického `while` cyklu ověřuj, zda je vstup platný. Pokud uživatel zadá neplatné celé číslo, program ho bude vyzývat k opakování tak dlouho, dokud nezadá správnou hodnotu.

_Poznámka: vstup jako text nebo reálné číslo teď neřeš._

```text
Enter a rating (1-5): 10
Invalid rating. Please try again (1-5): 11
Invalid rating. Please try again (1-5): 42
Invalid rating. Please try again (1-5): 6
Invalid rating. Please try again (1-5): 0
Invalid rating. Please try again (1-5): -2
Invalid rating. Please try again (1-5): 3

Thank you! Rating 3 has been saved.
```
