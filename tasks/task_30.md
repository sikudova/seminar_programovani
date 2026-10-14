# Cvičení 30: vybíjení baterie

**Cíl:** procvičení `while-do` cyklu

Napiš program, který simuluje, jak dlouho vydrží baterie zařízení.

Uživatel zadá:
* počáteční kapacitu baterie v procentech (např. 100),
* rychlost vybíjení za hodinu v procentech (např. 25).

Pomocí `while` cyklu simuluj ubíhající hodiny. V každém kroku sniž kapacitu baterie o hodnotu vybíjení a vypiš aktuální stav baterie. Cyklus běží tak dlouho, dokud je baterie větší než nula. Na konci vypiš, za kolik hodin se zařízení vybilo.

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
