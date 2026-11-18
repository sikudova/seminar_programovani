# Cvičení 48: passing by reference vs. passing by value

**Cíl:** naučit se předávat argumenty do metod

_The method definition specifies the names and types of any **parameters** that are required. When calling code calls the method, it provides concrete values called **arguments** for each parameter.
The arguments must be compatible with the parameter type but the argument name (if any) used in the calling code doesn't have to be the same as the parameter named defined in the method._

## Value type

By default, when an **instance of a value type** is passed to a method, its **copy is passed instead of the instance itself**. Therefore, changes to the argument have no effect on the original instance in the calling method.

To pass a value-type **instance by reference**, use the `ref` keyword.

In general, **passing by reference** means you pass a reference that refers to an object. Therefore, we use the variable directly without creating any new copy. 

To **pass arguments by reference** instead of by value, use one of the following modifiers in a parameter declaration:
* **ref:** Initialize the argument before calling the method. The method can assign a new value to the parameter, but it isn't required to.
* **out:** The calling method doesn't need to initialize the argument before calling the method. The method must assign a value to the parameter.
* **ref readonly:** Initialize the argument before calling the method. The method can't assign a new value to the parameter.
* **in:** Initialize the argument before calling the method. The method can't assign a new value to the parameter. The compiler might create a temporary variable to hold a copy of the argument to in parameters.

Kuk: [Reference parameters](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/method-parameters#reference-parameters)

### Value types
Value types: [zde](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/value-types)

C# provides the following **built-in value types**, also known as simple types:
* Integral numeric types,
* Floating-point numeric types,
* bool that represents a Boolean value,
* char that represents a Unicode UTF-16 character.

## Reference type

Variables of reference types store references to their data (objects), while variables of value types directly contain their data. With reference types, two variables can reference the same object. Therefore, operations on one variable can affect the object referenced by the other variable. 

C# also provides the following **built-in reference types**:
* dynamic,
* object,
* **string**.
