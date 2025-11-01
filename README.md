# Open-Closed-Principle
Цей приклад демонструє застосування OCP у C# на прикладі ієрархії зброї.

---
#Цей проєкт демонструє використання **абстрактного класу** та **поліморфізму** в мові C#.  
Базовий клас `Weapon` визначає спільний метод `Invoke()`, який реалізується у кожному виді зброї по-своєму.

`
abstract class Weapon
{
    public abstract void Invoke(); //Абстрактний клас Weapon визначає метод Invoke(), який має бути реалізований у всіх класах-нащадках.
}
`
`
class Gun : Weapon
{
    public override void Invoke()
    {
        Console.WriteLine("Piv");
    }
}
`
`
class Knife : Weapon
{
    public override void Invoke()
    {
        Console.WriteLine("Vjuh");
    }
}
`
`
class Rifle : Weapon
{
    public override void Invoke()
    {
        // Логіка стрільби
    }
}
`

