# Cvičení 16: přetypování (type casting)

**Cíl:** pochopit implicitní a explicitní přetypování

Type casting is when you assign a value of one data type to another type.

V C# máme 2 typy přetypování:
* **implicitní přetypování** (automatické): converting a smaller type to a larger type size
* **explicitní přetypování** (manuální): converting a larger type to a smaller size type

## Implicitní přetypování
Děje se samo, když ukládáš **menší typ do většího** (např. celé číslo int do desetinného čísla double). C# ví, že se nic neztratí, tak to udělá za tebe.

```csharp
int myInt = 9;
double myDouble = myInt;       // Automatic casting: int to double

Console.WriteLine(myInt);      // Outputs 9
Console.WriteLine(myDouble);   // Outputs 9
```

```csharp
// Implicit conversion. A long can
// hold any value an int can hold, and more!
int num = 2147483647;
long bigNum = num;
```

Kuk: [C#: Implicit numeric conversions](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/numeric-conversions#implicit-numeric-conversions)

_Implicit conversions: No special syntax is required because the conversion **always succeeds and no data is lost**. Examples include conversions from smaller to larger integral types._

## Explicitní přetypování
Explicit casting must be done manually by placing the type in parentheses in front of the value:

```csharp
double myDouble = 9.78;
int myInt = (int) myDouble;    // Manual casting: double to int

Console.WriteLine(myDouble);   // Outputs 9.78
Console.WriteLine(myInt);      // Outputs 9
```

_However, if a conversion can't be made without a risk of losing information, the compiler requires that you **perform an explicit conversion, which is called a cast**. A cast is a way of explicitly making the conversion. It indicates you're aware data loss might occur, or the cast might fail at run time. To perform a cast, specify the destination type in parentheses before the expression you want converted._

_The following program casts a double to an int. The program doesn't compile without the cast._

```csharp
double x = 1234.7;
int a;
// Cast double to int.
a = (int)x;
Console.WriteLine(a);
// Output: 1234
```

Dalším způsobem je použít built-in metody k přetypování, např.: `Convert.ToBoolean`, `Convert.ToDouble`, `Convert.ToString`, `Convert.ToInt32`:

```csharp
int myInt = 10;
double myDouble = 5.25;
bool myBool = true;

Console.WriteLine(Convert.ToString(myInt));    // convert int to string
Console.WriteLine(Convert.ToDouble(myInt));    // convert int to double
Console.WriteLine(Convert.ToInt32(myDouble));  // convert double to int
Console.WriteLine(Convert.ToString(myBool));   // convert bool to string```
```

_Explicit conversions (casts): Explicit conversions require a cast expression. Casting is required when **information might be lost in the conversion**, or when the **conversion might not succeed** for other reasons. Typical examples include numeric conversion to a type that has less precision or a smaller range._
