# Cvičení 42: validátor hesla

**Cíl:** procvičení práce se `stringy`

Napiš program, který provede následující:

* vyžádá si heslo,
* ověř, zda má heslo alespoň 12 znaků (pokud ne, vypiš varování),
* zjisti, zda obsahuje alespoň jednu číslice,
* zkontroluj, zda heslo obsahuje alespoň jedno velké písmeno.

Pokud heslo nesplňuje nějakou podmínku, vypiš uživateli o tom informaci.

```text
Given password: DlouheHeslo123HAHA
The password meets all security requirements.
```

```text
Given password: heslo
The password does not meet the security requirements:
- The password is too short (at least 12 characters are required).
- The password does not contain any digit.
- The password does not contain any capital letter.
```
