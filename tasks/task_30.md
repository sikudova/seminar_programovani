# Cvičení 30: vybíjení baterie

**Cíl:** procvičení `while-do` cyklu

Napiš program, který simuluje, jak dlouho vydrží baterie zařízení.

Uživatel zadá:
* počáteční kapacitu baterie v procentech (např. 100),
* rychlost vybíjení za hodinu v procentech (např. 25).

Pomocí `while` cyklu simuluj ubíhající hodiny. V každém kroku sniž kapacitu baterie o hodnotu vybíjení a vypiš aktuální stav baterie. Cyklus běží tak dlouho, dokud je baterie větší než nula. Na konci vypiš, za kolik hodin se zařízení vybilo.

**Bonus:** pokud máte čas, přidejte validaci vstupů (záporná čísla a nula).

```text
Enter a current battery percentage: 98
Enter a battery drain rate: 15
Hour 1: battery percentage is 83.
Hour 2: battery percentage is 68.
Hour 3: battery percentage is 53.
Hour 4: battery percentage is 38.
Hour 5: battery percentage is 23.
Hour 6: battery percentage is 8.
Hour 7: battery percentage is 0.
Battery died after 7 hours.
```

```text
Enter a current battery percentage: 100
Enter a battery drain rate: 20
Hour 1: battery percentage is 80.
Hour 2: battery percentage is 60.
Hour 3: battery percentage is 40.
Hour 4: battery percentage is 20.
Hour 5: battery percentage is 0.
Battery died after 5 hours.
```

```text
Enter a current battery percentage: 100
Enter a battery drain rate: 0
Battery drain rate must be greater than 0. Try again.
Enter a battery drain rate: -5
Battery drain rate must be greater than 0. Try again.
Enter a battery drain rate: 10
Hour 1: battery percentage is 90.
Hour 2: battery percentage is 80.
Hour 3: battery percentage is 70.
Hour 4: battery percentage is 60.
Hour 5: battery percentage is 50.
Hour 6: battery percentage is 40.
Hour 7: battery percentage is 30.
Hour 8: battery percentage is 20.
Hour 9: battery percentage is 10.
Hour 10: battery percentage is 0.
Battery died after 10 hours.
```

```text
Enter a current battery percentage: -15
Battery percentage can not be less than 0. Try again.
Enter a current battery percentage: 78
Enter a battery drain rate: 0
Battery drain rate must be greater than 0. Try again.
Enter a battery drain rate: -2
Battery drain rate must be greater than 0. Try again.
Enter a battery drain rate: 13
Hour 1: battery percentage is 65.
Hour 2: battery percentage is 52.
Hour 3: battery percentage is 39.
Hour 4: battery percentage is 26.
Hour 5: battery percentage is 13.
Hour 6: battery percentage is 0.
Battery died after 6 hours.
```

```text
Enter a current battery percentage: 0
Enter a battery drain rate: 15
Battery is already dead.
```
