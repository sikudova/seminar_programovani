# Cvičení 14: výběr  postavy do hry

**Cíl:** procvičení načítání vstupů, jeho kontrola pomocí podmínek, větvení kódu

Napiš program, který vyzve uživatele k výběru postavy do počítačové hry.

Aplikace uživatele přivítá, zkontroluje jeho věk, vybere si postavu a počáteční obnos peněz.

## Požadavky a průběh
### Uživatel zadá:
* jméno,
* věk,
* počet zlaťáků v peněžence.

### Věková kontrola
Pokud je uživateli méně než 12 let, nepokračuje dál, pouze mu program vypíše informativní hlášku o tom, že je zatím mladý na tuto hru.

### Výběr typu postavy
Uživatel si zvolí z následujících typů postavy:
* válečník (warrior),
* čaroděj (mage),
* rytíř (knight),
* zloděj (rogue).

Pokud si vybere něco mimo nabídku, pokračuje v roli návštevník (visitor).

### Nákup výbavy
Uživatel se rozhodne, zda si chce koupit magický lektvar za 50 zlaťáků. Odpoví na tuto otázku ano/ne (yes/no).

Program provede kontrolu nákupu: pokud uživatel odpověděl ano (yes) a má dostatek zlaťáků, proěhne nákup (vypíše se informativní hláška). V opačném případně nákup neproběhne (vypíše se informativní hláška).

```text
I will give you a music tip according to your music taste.
Choose a genre (pop, rock, country, česká klasika): nevim
Smolík, listen to Vysoký Jalovec.
```
