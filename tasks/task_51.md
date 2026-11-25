# Cvičení 51: validátor českého rodného čísla

**Cíl:** procvičení tvorby a používání metod

Napište program, který očistí rodné číslo, ověří jeho platnost a zjistí z něj pohlaví a datum narození.

Rodné číslo se skládá z devíti nebo deseti číslic.

**Prvních šest číslic** v obou případech popisuje datum narození ve formátu **RRMMDD**, tj. po dvou číslicích pro rok, měsíc a den narození (s případnou úvodní nulou). Např. 701020 označuje datum narození 20. října 1970. Přitom ženy mají k měsíci narození **připočteno číslo 50** (tzn. 706020 označuje ženu narozenou 20. října 1970).

Zbytek rodného čísla (tzv. koncovka rodného čísla) odlišuje osoby stejného pohlaví narozené ve stejný den a zpravidla se odděluje lomítkem. Pro osoby narozené do roku 1953 včetně za lomítkem následovaly tři cifry, od roku 1954 přibyla čtvrtá číslice, která slouží ke kontrole platnosti rodného čísla jako **kontrolní číslice**.

Desetimístná rodná čísla (tzn. rodná čísla od roku 1954) jsou **beze zbytku dělitelná jedenácti**, aby bylo možno snadno rozpoznat překlepy anebo jiné náhodné chyby. Poslední číslice desetimístného rodného čísla slouží jako kontrolní číslice, přičemž jde o zbytek po celočíselném dělení (tzv. modulo) prvních devíti čísel desetimístného rodného čísla jedenácti.

Metody:
* SanitizeBirthNumber (očištění rodného čísla),
* IsAllDigits (jsou všechny znaky číslice),
* IsValidBirthNumber (je rodné číslo validní),
* GetGender (určí pohlaví),
* GetDateOfBirth (urči datum narození).
