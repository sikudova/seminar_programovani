# Cvičení 12: switch case

**Cíl:** naučit se větvit program pomocí `switch case`

## Switch case

Příkaz `switch case` nám umožňuje provádět různé bloky kódu v závislosti na hodnotě proměnné tím, že ji porovnáváme s řadou možných hodnot jednotlivých případů.

`Switch` umožňuje zpřehlednit zápis některých složitých podmínek.

```csharp
switch (promenna)
{
    case hodnota1:
        // Co se stane, když promenna == hodnota1
        break;

    case hodnota2:
        // Co se stane, když promenna == hodnota2
        break;

    default:
        // Co se stane, když hodnota neodpovídá ani jedné z výše uvedených (funguje jako 'else')
        break;
}
```

Ve `switchi` je možné více případů (`cases`) spojit dohromady:

```csharp
switch (promenna)
{
    // Více case nad sebou bez kódu a breaku (sdílejí jednu akci)
    case hodnota1:
    case hodnota2:
    case hodnota3:
        // Kód, který se provede, pokud je proměnná rovna 
        // hodnotě 1, 2 NEBO 3
        break; // Tady už break být musí!

    // Samostatný případ
    case hodnota4:
        // Kód pouze pro hodnotu 4
        break;

    // Záchranná síť pro všechno ostatní
    default:
        // Kód, když hodnota nezapadá nikam jinam
        break;
}
```

#### Příklad 01: typ platby

Napiš program, který vyzve uživatele k výběru platební metody (card, cash, crypto). Pokud uživatel zadá jinou možnost, program vypíše varovnou hlášku.

```text
Choose a payment method (card, cash, crypto): card
Please, tap your card on the terminal.
```

```text
Choose a payment method (card, cash, crypto): cash
Please, prepare your money :).
```

```text
Choose a payment method (card, cash, crypto): crypto
Please, prepare your crypto wallet QR code.
```

```text
Choose a payment method (card, cash, crypto): oblička
Unknown payment method enetered!
```
