# Open-Closed-Principle
Цей приклад демонструє застосування OCP у C# на прикладі ієрархії зброї.

---
#Цей проєкт демонструє використання **абстрактного класу** та **поліморфізму** в мові C#.  
Базовий клас `Weapon` визначає спільний метод `Invoke()`, який реалізується у кожному виді зброї по-своєму.

```cs
//Абстрактний клас Weapon визначає метод Invoke(), який має бути реалізований у всіх класах-нащадках.
abstract class Weapon
{
    public abstract void Invoke(); 
}

//Наслідники Weapon які реалізовують Invoke();
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

/*Пркилад використання
Weapon gun = new Gun();
Weapon knife = new Knife();
Weapon rifle = new Rifle();

gun.Invoke();   // Piv
knife.Invoke(); // Vjuh
rifle.Invoke(); // (Логіка стрільби) 
*/


