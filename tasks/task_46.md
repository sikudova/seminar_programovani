# Cvičení 46: geometrická kalkulačka

**Cíl:** procvičení tvorby a používání metod

Vytvoř program, který uživateli nabídne menu s výběrem tělesa pro výpočet jeho objemu a povrchu. Podle volby si vyžádá potřebné rozměry a pomocí samostatných metod spočítá a vypíše jeho objem a povrch.

```text
--- GEOMETRY CALCULATOR ---
Choose a solid figure (cube, cuboid, cylinder): cube
Enter a side of a cube: 5
Results for cube with side 5: volume = 125, surface = 150.
```

```text
--- GEOMETRY CALCULATOR ---
Choose a solid figure (cube, cuboid, cylinder): cuboid
Enter a first side of a cuboid: 2
Enter a second side of a cuboid: 3
Enter a third side of a cuboid: 5
Results for cube with sides 2, 3 and 5: volume = 30, surface = 62.
```

```text
--- GEOMETRY CALCULATOR ---
Choose a solid figure (cube, cuboid, cylinder): cylinder
Enter a radius of a cylinder: 4
Enter a height a cylinder: 10
Results for cylinder with radius 4 and height 10: volume = 502,6548245743669, surface = 351,85837720205683.
```

## Čtverec

Napiš metodu, pro výpočet obsahu čtverce.

```csharp
static double CalculateSquareArea(double side);
```

## Obdélník

Napiš metodu pro výpočet obsahu obdélníku.

```csharp
static double CalculateRectangleArea(double height, double width);
```

## Kruh

Napiš metodu pro výpočet obsahu kruhu.

```csharp
static double CalculateCircleArea(double radius);
```

## Krychle

Napiš metody pro výpočet povrchu a objemu krychle.

```csharp
static double CalculateCubeSurface(double side);
static double CalculateCubeVolume(double side);
```

## Kvádr

Napiš metody pro výpočet povrchu a objemu kvádru.

```csharp
static double CalculateCuboidSurface(double a, double b, double c);
static double CalculateCuboidVolume(double a, double b, double c);
```

## Válec

Napiš metody pro výpočet povrchu a objemu válce.

```csharp
static double CalculateCylinderSurface(double radius, double height);
static double CalculateCylinderVolume(double radius, double height);
```
