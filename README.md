# Function-Overloading-Constructor-Overloading-Copy-Constructor

1.
using System;

class Program
{
// Method overloading - different parameter types
static int MyFunc(int i)
{
return i;
}
static double MyFunc(double i)
{
return i;
}
static void Main(string[] args)
{
Console.WriteLine(MyFunc(10)); // Calls MyFunc(int i)

Console.WriteLine(MyFunc(5.4)); // Calls MyFunc(double i)
}

}

2.
Overloading Constructor Functions:

using System;

class Person

{

public string Name;

public int Age;

public Person() // Default constructor

{

Name = "Unknown";

Age = 0;

}

public Person(string name) // Constructor with one parameter

{

Name = name;

}

public Person(string name, int age) // Constructor with two parameters

{

Name = name;

Age = age;

}

public void Display()

{

Console.WriteLine($"Name: {Name}, Age: {Age}");

}

static void Main()

{

// Using different overloaded constructors

Person person1 = new Person();

// Default constructor

Person person2 = new Person(“ABC");

// Constructor with one parameter

Person person3 = new Person(“DEF", 20);

// Constructor with two parameters

person1.Display();

person2.Display();

person3.Display();

}

}

3.Shallow Copy Code Example (C#)
class BankAccount {

private string name;

private double balance;

// Property for Name with get and set

public string Name {

get { return name; }

set { name = value; }

}

// Property for Balance with get and set

public double Balance {

get { return balance; }

set { balance = value; }

}

// Parameterized Constructor

public BankAccount(string name, double balance) {

this.Name = name;

this.Balance = balance;

}

}

Shallow Copy Code Example (C#)

// Usage: Shallow Copy Example

class Program {

static void Main() {

// Create the first BankAccount object

BankAccount account1 = new BankAccount(“ABC”, 1000.00);

// Create a shallow copy of account1 by assignment (not using a copy constructor)

BankAccount account2 = account1; // Shallow copy: account2 references the same memory as account1

// Modify account2's Balance

account2.Balance = 500.00;

// Output the balances of both account1 and account2

Console.WriteLine("Account 1 Balance: " + account1.Balance); // Output: 500.00

Console.WriteLine("Account 2 Balance: " + account2.Balance); // Output: 500.00

}

}

