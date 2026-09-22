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
