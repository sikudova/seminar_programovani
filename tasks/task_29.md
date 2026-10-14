# Cvičení 29: ověření PINu

**Cíl:** procvičení `while-do` cyklu

Napiš program, který simuluje zadání bankovního PINu (nějaký si zvolte).

Uživatel má na zadání maximálně 3 pokusy. Pokud zadá správný PIN, program ho pustí dál. Pokud zadá špatný PIN, program ho upozorní, odečte pokus a zkusí to znovu. Pokud vyčerpá všechny 3 pokusy, karta se zablokuje.

_Poznámka: vstup jako text nebo reálné číslo teď neřeš._

```text
Enter a PIN: 8451

Access granted.
```

```text
Enter a PIN: 1234
Incorrect PIN. Attempts left: 2
Enter a PIN again: 1234
Incorrect PIN. Attempts left: 1
Enter a PIN again: 8451

Access granted.
```

```text
Enter a PIN: 1234
Incorrect PIN. Attempts left: 2
Enter a PIN again: 4567
Incorrect PIN. Attempts left: 1
Enter a PIN again: 87981513

Card blocked.
```
