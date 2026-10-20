# Cvičení 39: `string`

**Cíl:** naučit se používat datový typ `string`

Typ `string` je objekt, který reprezentuje sekvenci (posloupnost) znaků – tedy klasický text nebo větu.

Hodnoty se píšou do klasických dvojitých uvozovek `""`.

```csharp
string greeting = "Ahoj světe!";
string name = "Pavel";
```

## Immutability (neměnnost)

V C# je `string` neměnný (immutable). To znamená, že jakmile je řetězec jednou vytvořen a uložen v paměti, jeho obsah už nelze nikdy změnit.

Když se provede operace jako `text = text + "ahoj";`, C# ve skutečnosti nezmění původní řetězec v paměti. Místo toho vytvoří zcela nový objekt, do něj uloží výsledek a proměnná začne ukazovat na něj.

Pokud se provádí mnoho úprav textu za sebou (např. v cyklu), je to neefektivní pro paměť. Pro takové případy se v C# používá speciální třída `StringBuilder`.

## Indexování

`string` je v C# vnímán jako posloupnost znaků, může se tedy použít **indexování**.

_You can access the characters in a string by referring to its index number inside square brackets []._

Indexování je mechanismus, který umožňuje přistupovat ke konkrétním prvkům uvnitř uspořádané kolekce dat – například k jednotlivým znakům v textu (`string`).

K indexování se používají hranaté závorky `[]`. Každý znak má pevnou pozici – **index**.

**Důležité – indexuje se od 0:**
* `[0]` je první znak,
* `[1]` je druhý znak atd.,
* poslední prvek má index roven `Length - 1`, kde `Length` je délka řetězce.

Pokud má řetězec délku `5` znaků (`Length = 5`), jeho platné indexy jdou od `0` do `4`.

```csharp
string text = "Ahoj";

char firstChar = text[0]; // Vrací 'A'
char thirdChar = text[2]; // Vrací 'o'

// Poslední znak zjistíme pomocí délky mínus jedna
char lastChar = text[text.Length - 1]; // Vrací 'j'
```

### Range operátor `..`

`..` je operátor pro rozsah (range).

```csharp
Range operator ..(Index x, Index y);
```

Existuje typ `Range`, který představuje rozsah indexů od počátečního indexu (včetně) až po koncový index (vyjímaje).

Rozsah `Range` se zkonstruuje pomocí dvou indexů (typ `Index`):

```csharp
var firstQuad = new Range(0, 4);  // the indices from `0` to `3`
                                  // int values impicitly convert to `Index`
var nextQuad = new Range(4, 8);   // the indices from `4` to `7`
```

Operátor `..` definuje právě tento rozsah `Range`.

```csharp
var firstQuad = ..4; // the indices from `0` to `3`
var wholeSeq = ..;   // the indices from `0` to `N-1`
```

Operátor `..` je možné použít k "vyříznutí" části řetězce (`substring`).:

```csharp
string word = "Programování";

// Vezme znaky od indexu 0 do 7 
// (přičemž horní hranice 7 je exkluzivní – znak na indexu 7 už se nezahrne)
string sub = word[0..7]; 

Console.WriteLine(sub); // Vypíše: "Program"
```

_A range specifies the start and end of a range. The start of the range is inclusive, but the end of the range is exclusive, meaning the start is included in the range but the end isn't included in the range. The range `[0..^0]` represents the entire range, just as `[0..sequence.Length]` represents the entire range._

### Operátor stříšky `^`

Index from-end `^` je unární operátor, taky se mu říká _hat operator_.

```csharp
Index operator ^(int x);
```

Existuje typ `Index`, který nese informaci o indexu (čísle) a o tom, odkud se indexuje (od začátku/od konce).

Operátor `^` vrací hodnotu typu `from-end` `Index` (index a indexujeme od konce) – `^` se tedy používá k indexaci od konce řetězce.

`^n` se přepočítá podle vzorce: `skutečný index = Length - n`.

```csharp
string text = "Program";

char last = text[^1];    // 'm' (první od konce)
char secondLast = text[^2]; // 'a' (druhý od konce)
```

_Consider an array sequence. The `0` index is the same as `sequence[0]`. The `^0` index is the same as `sequence[sequence.Length]`. The expression `sequence[^0]` throws an exception, just as `sequence[sequence.Length]` does. For any number `n`, the index `^n` is the same as `sequence.Length - n`._

### Kombinace stříšky `^` s rozsahy `..`

Kombinace stříšky `^` a rozsahu `..` umožňuje definovat začátek i konec výřezu (range) s ohledem na konec řetězce, aniž by bylo nutné počítat celkovou délku řetězce.

#### Od indexu do bodu od konce `start..^end`

Pro oříznutí od nějakého pevného indexu zleva, ale konec výřezu se ořízne zprava (např. zahodit určitý počet posledních znaků).

```csharp
string text = "Programování"; // Délka = 12

// Vezmi od indexu 1 až po 3. prvek od konce
string result = text[1..^3]; 

Console.WriteLine(result); // Vypíše: "rogramová" (^3 je 3. od konce)
```

#### Od začátku do bodu od konce `..^end`

Pokud se vynechá levá stranu před tečkami `..`, C# automaticky doplní začátek (`0`) – umožňuje odstranit konec textu.

```csharp
string filename = "document.pdf";

// Vezmi všechno od začátku až po 4. prvek od konce (čímž uřízneš příponu ".pdf")
string nameWithoutExtension = filename[..^4]; 

Console.WriteLine(nameWithoutExtension); // Vypíše: "document"
```

#### Od bodu od konce do konce `^start..`

Pokud se vynechá pravá strana za tečkami `..`, C# automaticky doplní `^0` (až do samého konce) – umožňuje získat koncovou část textu.

```csharp
string filename = "document.pdf";

// Vezmi od 4. prvku od konce až do úplného konce
string extension = filename[^4..]; 

Console.WriteLine(extension); // Vypíše: ".pdf"
```

#### Mezi dvěma body od konce `^start..^end`

Oba okraje je možné definovat pomocí stříšky `^`.

Levá hranice rozsahu musí v textu předcházet té pravé. Protože indexy od konce rostou směrem doleva, číslo u levé stříšky musí být větší než číslo u pravé stříšky.

```csharp
string text = "Programování"; // Délka = 12

// Vezmi od 8. prvku od konce až po 3. prvek od konce
string result = text[^8..^3]; 

Console.WriteLine(result); // Vypíše: "ramov"
```

## Metody na `string`

Seznam metod na datovém typu `string`: [`string` metody]().

Níže jsou uvedené často používané metody.
