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
