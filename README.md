# Open-Closed-Principle
Цей приклад демонструє застосування OCP у C# на прикладі ієрархії зброї.

---
# Weapon System — Приклад SOLID (Open-Closed Principle)

Цей проєкт демонструє **принцип відкритості/закритості (OCP)** з SOLID у мові C#.

## Суть принципу OCP

> **Код має бути відкритим для розширення, але закритим для зміни.**

Це означає, що ми повинні мати можливість **додавати нову поведінку**, не змінюючи існуючі класи.

---

## Структура

Маємо абстрактний клас `Weapon`, який визначає метод `Invoke()`.  
Кожен конкретний вид зброї реалізує цей метод по-своєму.

```csharp

## Абстрактний клас Weapon визначає метод Invoke(), який має бути реалізований у всіх класах-нащадках.
abstract class Weapon
{
    public abstract void Invoke(); 
}

## Наслідники Weapon які реалізовують Invoke();
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

## Пркилад використання
Weapon gun = new Gun();
Weapon knife = new Knife();
Weapon rifle = new Rifle();

gun.Invoke();   // Piv
knife.Invoke(); // Vjuh
rifle.Invoke(); // (Логіка стрільби) 

## Таке рішення дозволяє розширити функціонал та змінити поведінку без зміни в існуючому класі Weapon

