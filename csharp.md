# C# Syntax Overview

## Variables and Data Types
```csharp
int number = 10;
float pi = 3.14f;
double largeNumber = 1.7976931348623157E+308;
bool isTrue = true;
char letter = 'A';
string message = "Hello, World!";
```

## Constants
```csharp
const double Pi = 3.14159;
```

## Operators
```csharp
int sum = 5 + 3;
int difference = 5 - 3;
int product = 5 * 3;
int quotient = 5 / 3;
int remainder = 5 % 3;
int increment = ++sum;
int decrement = --difference;
```

## Conditional Statements
```csharp
if (number > 0) {
    Console.WriteLine("Positive number");
} else if (number < 0) {
    Console.WriteLine("Negative number");
} else {
    Console.WriteLine("Zero");
}
```

## Switch Case
```csharp
switch (letter) {
    case 'A':
        Console.WriteLine("Letter is A");
        break;
    case 'B':
        Console.WriteLine("Letter is B");
        break;
    default:
        Console.WriteLine("Unknown letter");
        break;
}
```

## Loops

### For Loop
```csharp
for (int i = 0; i < 5; i++) {
    Console.WriteLine(i);
}
```

### While Loop
```csharp
int count = 0;
while (count < 5) {
    Console.WriteLine(count);
    count++;
}
```

### Do-While Loop
```csharp
int x = 0;
do {
    Console.WriteLine(x);
    x++;
} while (x < 5);
```

## Arrays
```csharp
int[] numbers = {1, 2, 3, 4, 5};
Console.WriteLine(numbers[0]);
```

## Lists
```csharp
using System.Collections.Generic;

List<int> numList = new List<int> {1, 2, 3};
numList.Add(4);
numList.Remove(2);
Console.WriteLine(numList.Count);
```

## Methods
```csharp
void PrintMessage() {
    Console.WriteLine("Hello from a method");
}

int Add(int a, int b) {
    return a + b;
}
```

## Classes and Objects
```csharp
class Car {
    public string Brand;
    public int Year;

    public Car(string brand, int year) {
        Brand = brand;
        Year = year;
    }

    public void DisplayInfo() {
        Console.WriteLine($"Brand: {Brand}, Year: {Year}");
    }
}

Car myCar = new Car("Toyota", 2022);
myCar.DisplayInfo();
```

## Inheritance
```csharp
class Animal {
    public void MakeSound() {
        Console.WriteLine("Animal makes a sound");
    }
}

class Dog : Animal {
    public void Bark() {
        Console.WriteLine("Dog barks");
    }
}

Dog myDog = new Dog();
myDog.MakeSound();
myDog.Bark();
```

## Interfaces
```csharp
interface IVehicle {
    void Drive();
}

class Car : IVehicle {
    public void Drive() {
        Console.WriteLine("Driving a car");
    }
}
```

## Exception Handling
```csharp
try {
    int result = 10 / 0;
} catch (DivideByZeroException e) {
    Console.WriteLine("Cannot divide by zero!");
} finally {
    Console.WriteLine("End of try-catch block");
}
```

## File Handling
```csharp
using System.IO;

File.WriteAllText("test.txt", "Hello, File!");
string content = File.ReadAllText("test.txt");
Console.WriteLine(content);
```

## Async and Await
```csharp
using System.Threading.Tasks;

async Task PrintMessageAsync() {
    await Task.Delay(1000);
    Console.WriteLine("Async Message");
}
