# Cvičení 06: operátory

**Cíl:** procvičit si matematické a relační operátory, které jsou potřeba pro další konstrukce (podmínky, cykly)

## Aritmetické operátory (matematika)
Aritmetické operátory provádějí matematické operace (sčítání, odčítání, násobení, dělení a modulus) mezi číselnými datovými typy (`int`, `double` atd.).

Jedná se o binární operátory - k provedení operace potřebují dva operandy.

| Operátor | Význam | Příklad v C# | Výsledek |
| :---: | :--- | :--- | :--- |
| **`+`** | Sčítání | `10 + 5` | `15` |
| **`-`** | Odčítání | `10 - 5` | `5` |
| **`*`** | Násobení | `10 * 5` | `50` |
| **`/`** | Dělení | `10 / 5` | `2` |
| **`%`** | Modulo (zbytek po dělení) | `10 % 3` | `1` |

Binární aritmetické operátory jsou asociativní zleva - tzn. operátory se stejnou prioritou se vyhodnocují zleva doprava.

Pomocí závorek `( )` je možné změnit pořadí vyhodnocování dané prioritou a asociativitou operátorů.

### Celočíselné dělení
U celočíselných typů je výsledek `/` (dělení) celočíselného typu - podíl obou operandů zaokrouhlený k nule.

### Dělení desetinných čísel
Pokud je alespoň jeden operand číslo s plovoucí desetinnou čárkou (`float`, `double`, `decimal`), provede se dělení s plovoucí desetinnou čárkou.

### Modulo aneb zbytek po dělení
Modulo vrací **zbytek** po celočíselném dělení dvou čísel.

Operátor modulo se v C# zapisuje pomocí znaku procenta (`%`). 

#### Příklad 01: poslední číslice
Napiš program, který vyzve uživatele k zadání libovolného celého čísla. Program následně vypíše poslední číslici tohoto čísla.

```text
Enter a number (integer): 457
Last digit of number 457 is 7.
```

#### Příklad 02: pokladna
Napiš program, který vyzve uživatele k zadání libovolné celé částky v Kč. Program následně vypíše, kolik stovek uživatel dostane a kolik drobných mu zbývá.

```text
Enter the total amount in CZK: 1235
You will receive 12 hundreds, leaving 35 CZK.
```

## Relační operátory (porovnávání)
Relační operátory porovnávají dva operandy a vracejí logickou hodnotu (`true`, nebo `false`).

Tyto operátory se používají při rozhodování a cykly.

| Operátor | Význam | Příklad | Výsledek (`bool`) |
| :---: | :--- | :--- | :---: |
| **`==`** | Je rovno | `5 == 5` | `true` |
| **`!=`** | Není rovno (Je různé) | `5 != 3` | `true` |
| **`>`** | Je větší než | `5 > 10` | `false` |
| **`<`** | Je menší než | `5 < 10` | `true` |
| **`>=`** | Je větší nebo rovno | `5 >= 5` | `true` |
| **`<=`** | Je menší nebo rovno | `4 <= 3` | `false` |

#### Příklad 03: kontrola věku
Napiš program, který vyzve uživatele k zadání věku. Program následně vypíše, zda je osoba s daným věkem dospělá.

```text
Enter your age: 17
Is adult: False
```

#### Příklad 04: rychlostní radar
Napiš program, který vyzve uživatele k zadání rychlosti auta/motorky. V programu máš uložený rychlostní limit, např, 50 km/h. Program následně vypíše, zda řidič překročil tento limit.

```text
Enter your current speed (in km/h): 183
Speeding: True
```

#### Příklad 05: tajné číslo
Napiš program, který vyzve uživatele k hádání čísla. V programu máš uloženou hodnotu svého tajného čísla. Program následně vypíše, zda uživatel uhádl tajné číslo.

```text
Guess the secret number: 14
You've guessed correctly: False
That's a bad tip: True
```
