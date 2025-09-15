# C#
```cs
if (obj is IEnumerable enum){

}

IEnumerable enum = obj as IEnumerable
if (enum is not null){}
```
cast the obj to IEnmerable

```cs
obj is string;
obj is null;
obj is IEnumerable;
```
data type check

```cs
int[][] jaggedArray = new int[][]
        {
            new int[] { 1, 2, 3 },       // Row 0 has 3 elements
            new int[] { 4, 5 },          // Row 1 has 2 elements
            new int[] { 6, 7, 8, 9 }     // Row 2 has 4 elements
        };

int[,] rectArray = new int[,]
{
    { 1, 2, 3 },   // Row 0
    { 4, 5, 6 },   // Row 1
    { 7, 8, 9 }    // Row 2
};

rectArray.Cast<int>()
```
Jagged 2d array with initial values
Rect 2d array with initial value
print rect array, react array is IEnumerable not T

```cs
dictionary1.OrderBy(kvp => kvp.Key)
           .SequenceEqual(dictionary2.OrderBy(kvp => kvp.Key))
```
compare if 2 dict has the same key value pairs


```cs
using System;
using System.Collections.Generic;

//////////////////////
// Base Class
//////////////////////
abstract class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    // Constructor
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Abstract method (must be implemented by derived classes)
    public abstract void DisplayRole();

    // Virtual method (can be overridden, but has a default behavior)
    public virtual void using System;
using System.Collections.Generic;

//////////////////////
// Base Class
//////////////////////
abstract class Person
{
    public string Name { get; set; }
    public int Age { get; set; }

    // Constructor
    public Person(string name, int age)
    {
        Name = name;
        Age = age;
    }

    // Abstract method (must be implemented by derived classes)
    public abstract void DisplayRole();

    // Virtual method (can be overridden, but has a default behavior)
    public virtual void Introduce()
    {
        Console.WriteLine($"Hi, my name is {Name} and I am {Age} years old.");
    }
}

//////////////////////
// Derived Class 1
//////////////////////
class Student : Person
{
    public int Grade { get; set; }

    // Constructor calls base constructor
    public Student(string name, int age, int grade) : base(name, age)
    {
        Grade = grade;
    }

    // Must implement abstract method
    public override void DisplayRole()
    {
        Console.WriteLine("I am a student.");
    }

    // Override virtual method
    public override void Introduce()
    {
        base.Introduce();  // call base method
        Console.WriteLine($"I study in grade {Grade}.");
    }

    public void Study()
    {
        Console.WriteLine($"{Name} is studying.");
    }
}

//////////////////////
// Derived Class 2
//////////////////////
class Teacher : Person
{
    public string Subject { get; set; }

    public Teacher(string name, int age, string subject) : base(name, age)
    {
        Subject = subject;
    }

    public override void DisplayRole()
    {
        Console.WriteLine("I am a teacher.");
    }

    public override void Introduce()
    {
        base.Introduce();
        Console.WriteLine($"I teach {Subject}.");
    }

    public void Teach()
    {
        Console.WriteLine($"{Name} is teaching {Subject}.");
    }
}

//////////////////////
// Program Entry
//////////////////////
class Program
{
    static void Main()
    {
        // Using polymorphism: store different Person types in one list
        List<Person> people = new List<Person>
        {
            new Student("Alice", 15, 10),
            new Teacher("Mr. Smith", 40, "Mathematics")
        };

        foreach (var person in people)
        {
            person.DisplayRole();  // Calls the correct implementation depending on type
            person.Introduce();    // Calls overridden version if exists
            Console.WriteLine();
        }

        // Directly call subclass-specific methods
        Student s = new Student("Bob", 16, 11);
        s.Study();

        Teacher t = new Teacher("Mrs. Johnson", 35, "Physics");
        t.Teach();
    }
}

    {
        Console.WriteLine($"Hi, my name is {Name} and I am {Age} years old.");
    }
}

//////////////////////
// Derived Class 1
//////////////////////
class Student : Person
{
    public int Grade { get; set; }

    // Constructor calls base constructor
    public Student(string name, int age, int grade) : base(name, age)
    {
        Grade = grade;
    }

    // Must implement abstract method
    public override void DisplayRole()
    {
        Console.WriteLine("I am a student.");
    }

    // Override virtual method
    public override void Introduce()
    {
        base.Introduce();  // call base method
        Console.WriteLine($"I study in grade {Grade}.");
    }

    public void Study()
    {
        Console.WriteLine($"{Name} is studying.");
    }
}

//////////////////////
// Derived Class 2
//////////////////////
class Teacher : Person
{
    public string Subject { get; set; }

    public Teacher(string name, int age, string subject) : base(name, age)
    {
        Subject = subject;
    }

    public override void DisplayRole()
    {
        Console.WriteLine("I am a teacher.");
    }

    public override void Introduce()
    {
        base.Introduce();
        Console.WriteLine($"I teach {Subject}.");
    }

    public void Teach()
    {
        Console.WriteLine($"{Name} is teaching {Subject}.");
    }
}

//////////////////////
// Program Entry
//////////////////////
class Program
{
    static void Main()
    {
        // Using polymorphism: store different Person types in one list
        List<Person> people = new List<Person>
        {
            new Student("Alice", 15, 10),
            new Teacher("Mr. Smith", 40, "Mathematics")
        };

        foreach (var person in people)
        {
            person.DisplayRole();  // Calls the correct implementation depending on type
            person.Introduce();    // Calls overridden version if exists
            Console.WriteLine();
        }

        // Directly call subclass-specific methods
        Student s = new Student("Bob", 16, 11);
        s.Study();

        Teacher t = new Teacher("Mrs. Johnson", 35, "Physics");
        t.Teach();
    }
}
```
example of inheritance
