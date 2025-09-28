# Open-Closed-Principle
Цей приклад демонструє застосування OCP у C# на прикладі ієрархії зброї.

---

code:

```csharp
abstract class Weapon
{
    public abstract void Invoke();
}

class Gun : Weapon
{
    public override void Invoke()
    {
        Console.WriteLine("Piv");
    }
}

class Knife : Weapon
{
    public override void Invoke()
    {
        Console.WriteLine("Vjuh");
    }
}

class Rifle : Weapon
{
    public override void Invoke()
    {
        // Логіка стрільби
    }
}
