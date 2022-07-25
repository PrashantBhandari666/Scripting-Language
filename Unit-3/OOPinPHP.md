<div align="center">

[**_``Go Back``_**](../README.md)

# OOP in PHP

</div>

## Classes & Object

### **Classes**
A class is a user defined blueprint or prototype from which objects are created.  It represents the set of properties or methods that are common to all objects of one type. In general, class declarations can include these components, in order:

* **Modifiers:** A class can be public or has default access
.
* **``class`` keyword:** class keyword is used to create a class.

* **Class name:** The name should begin with an initial letter (capitalized by convention).

* **Superclass(if any):** The name of the class’s parent (superclass), if any, preceded by the keyword extends. A class can only extend (subclass) one parent.s

* **Interfaces(if any):** A comma-separated list of interfaces implemented by the class, if any, preceded by the keyword implements. A class can implement more than one interface.

* **Body:** The class body surrounded by braces, ``{ }``.

Syntax to declare a class:

```PHP
class <class_name>
{  
    field;  
    method;  
}  
```
Example:

```PHP
<?php
class Bicycle 
{
  // state or field
  public $gear = 5;
  // behavior or method
  public function braking() 
  {
    echo "Working of Braking";
  }
}
?>
```
### **Object**

An object is called an instance of a class. For example, suppose Bicycle is a class then MountainBicycle, SportsBicycle, TouringBicycle, etc can be considered as objects of the class.

An object has three characteristics:

* **State:** It is represented by attributes of an object. It also reflects the properties of an object.
* **Behavior:** It is represented by methods of an object. It also reflects the response of an object with other objects.
* **Identity:** It gives a unique name to an object and enables one object to interact with other objects.

Here is how we can create an object of a class.

Syntax:

```PHP
object = new className();
```

Example:

```PHP
$sportsBicycle = new Bicycle();
$touringBicycle = new Bicycle();
```
We have used the ``new`` keyword along with the constructor of the class to create an object.

Here, ``$sportsBicycle`` and ``$touringBicycle`` are the names of objects. We can use them to access fields and methods of the class.

As you can see, we have created two objects of the class. We can create multiple objects of a single class in ``PHP``.

## Defining & Using Properties & Methods

We can use the name of objects along with the ``->`` operator to access members of a ``class``. 

If a property is declared as ``public``, it is available to object with the help of ``->`` operator. If a property is defined with ``static`` keyword, its value is shared among all objects of the class and is accessed using scope resolution operator (``::``) and name of ``class``. For example,

```PHP
<?php
class Bicycle 
{
  // field of class
  public $gear = 5;
  // method of class
  public function braking() 
  {
      echo "Working of Braking";
  }
}

// create object
$sportsBicycle = new Bicycle();
// access field and method
echo $sportsBicycle->gear;
$sportsBicycle->braking();
?>
```
In the above example, we have created a class named ``Bicycle``. It includes a field named ``gear`` and a method named ``braking()``. Notice the statement,

```Java
$sportsBicycle = new Bicycle();
```

Here, we have created an object of ``Bicycle`` named ``$sportsBicycle``. We then use the object to access the field and method of the class.

* ``$sportsBicycle->gear`` - access the field ``gear``
* ``$sportsBicycle->braking()`` - access the method ``braking()``

## Constructors and Destructors

### **Constructor**

In ``Object Oriented Programming`` terminology, ``constructor`` is a method defined inside a class is called automatically at the time of creation of object. Purpose of a constructor method is to initialize the object. In PHP, a method of special name __construct acts as a constructor.

Syntax:

```PHP
function __construct()
{
    Statements;
}
```

Example:

```PHP
<?php
class myclass
{
   function __construct()
   {
      echo "object initialized";
   }
}
$obj = new myclass();
?>
```
Constructor types: 

- ``Default Constructor``:It has no parameters, but the values to the default constructor can be passed dynamically.
- ``Parameterized Constructor``: It takes the parameters, and also you can pass different values to the data members.
- ``Copy Constructor``: It accepts the address of the other objects as a parameter.

### **Destructor**

``Destructor`` is a method automatically as soon as garbage collector finds that a particular object has no more references. In PHP, destructor method is named as ``__destruct``. During shutdown sequence too, objects will be destroyed. Destructor method doesn't take any arguments, neither does it return any data type.

Syntax:

```PHP
function __destruct()
{
    Statements;
}
```

Example:

```PHP
<?php
class myclass
{
   function __construct()
   {
      echo "object is initialized\n";
   }
   function __destruct()
   {
      echo "object is destroyed\n";
   }
}
$obj = new myclass();
?>
```

## Method Overriding

In method overriding, both ``parent`` and ``child`` classes should have same function name with and number of arguments. It is used to replace parent method in child class. The purpose of overriding is to change the behavior of parent class method. The two methods with the same name and same parameter is called overriding.

**Example**
```PHP
<?php
class P 
{
    function printc() 
    {
        echo "Parent\n";
    }
}
class C extends P 
{     
    // Overriding printc method
    function printc() 
    {
        echo "Child\n";
    }
}
$p = new P();
$c= new C();
$p->printc();
$c->printc();
?>
```
**Output**

```
Parent
Child
```

## Encapsulation

``Encapsulation`` is defined as the wrapping up of data under a single unit. It is the mechanism that binds together code and the data it manipulates. Another way to think about encapsulation is, it is a protective shield that prevents the data from being accessed by the code outside this shield.

Advantages of Encapsulation:

- ``Data Hiding``: The user will have no idea about the inner implementation of the class. It will not be visible to the user how the class is storing values in the variables. The user will only know that we are passing the values to a setter method and variables are getting initialized with that value.

- ``Increased Flexibility``: We can make the variables of the class read-only or write-only depending on our requirement. If we wish to make the variables read-only then we have to omit the setter methods like ``setName()``, ``setAge()``, etc. or if we wish to make the variables as write-only then we have to omit the get methods like ``getName()``, ``getAge()``, etc.

- ``Reusability``: Encapsulation also improves the re-usability and is easy to change with new requirements.

- ``Testing code is easy``: Encapsulated code is easy to test for unit testing.

## Inheritance 

``Inheritance`` is an important pillar of OOP (Object-Oriented Programming) . It is the mechanism in java by which one class is allowed to inherit the features ``(fields and methods)`` of another class.

Types of Inheritance

- Single Inheritance
- Multilevel Inheritance
- Hierarchical Inheritance
- Multiple Inheritance
- Hybrid Inheritance

``extends`` is the keyword used to inherit the properties of a class. Following is the syntax of extends keyword :

Syntax:

```PHP
class <derived-class> extends <base-class>  
{  
   //methods and fields  
}  
```

## Polymorphism

The word ``polymorphism`` means having many forms.``Polymorphism`` is considered one of the important features of ``Object-Oriented Programming``. Polymorphism allows us to perform a single action in different ways. In other words, polymorphism allows you to define one interface and have multiple implementations. The word “poly” means many and “morphs” means forms, So it means many forms.

In Java polymorphism is mainly divided into two types:

- Compile time Polymorphism
- Runtime Polymorphism

### **Compiled time Polymorphism:**

It is also known as static polymorphism. This type of polymorphism is achieved by function overloading or operator overloading. But Java doesn’t support the Operator Overloading.

``Method Overloading``: When there are multiple functions with same name but different parameters then these functions are said to be overloaded. Functions can be overloaded by change in number of arguments or/and change in type of arguments.

### **Runtime Polymorphism**

It is a process in which a function call to the overridden method is resolved at Runtime. This type of polymorphism is achieved by ``Method Overriding``.

``Method overriding``, on the other hand, occurs when a derived class has a definition for one of the member functions of the base class. That base function is said to be overridden.

## Static Members

### **Static Properties**
Static properties can be called directly - without creating an instance of a class.

To access a static property use the class name, double colon (``::``), and the property name

```PHP
<?php
class pi 
{
  public static $value = 3.14159;
}

// Get static property
echo pi::$value;
?>
```

### **Static Method**

Static methods can be called directly - without creating an instance of the class.

They can be invoked directly outside the class by using scope resolution operator (``::``)

```PHP
<?php
class greeting 
{
  public static function welcome() 
  {
    echo "Hello World!";
  }
}

// Call static method
greeting::welcome();
?>
```

## Exception Handeling

Exception handling is used to change the normal flow of the code execution if a specified error (exceptional) condition occurs. This condition is called an exception.

PHP provides following specialized keywords for this purpose.

- ``try``: It represent block of code in which exception can arise.
- ``catch``: It represent block of code that will be executed when a particular exception has been thrown.
- ``throw``: It is used to throw an exception. It is also used to list the exceptions that a function throws, but doesn’t handle itself.
- ``finally``: It is used in place of catch block or after catch block basically it is put for cleanup activity in PHP code.

Example
```PHP
<?php
$num = 0
try 
{
  if($num == 0)
  {
     throw new Exception("Number is less than 0 \n"); 
  }
}
catch(Exception $e) 
{
  echo "Exception Caught" . $e->getMessage() . "\n";
}
finally
{
  echo " Here cleanup activity will be done \n";
}
?>
```


