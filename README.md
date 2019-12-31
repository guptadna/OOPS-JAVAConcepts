OOPS & Java Concepts
=====

# Java Basic

## How Java works

![Alt text](/java_works_2.png?raw=true "Optional Title")

*Note - JRE contains JVM*. 

*A Java interpreter is a software that implements the Java virtual machine and runs Java applications. As the Java compiler compiles the source code into the Java bytecode, the same way the Java interpreter translates the Java bytecode into the code that can be understood by the Operating System*

![Alt text](/java_works_1.jpeg?raw=true "Optional Title")


## What is the difference between JDK, JRE, and JVM?

![Alt text](/JDK_JRE_JVM_0.jpg?raw=true "Optional Title")

![Alt text](/JDK_JRE_JVM_1.png?raw=true "Optional Title")

![Alt text](/JDK_JRE_JVM_2.png?raw=true "Optional Title")

##  What is the difference between Stack, Heap & Class(Method) Area?

![Alt text](/java_memory_3.jpg?raw=true "Optional Title")

![Alt text](/java_memory_2.jpg?raw=true "Optional Title")

## Where static variables are stored in memory in Java?

![Alt text](/java_memory_1.png?raw=true "Optional Title")

Class variables(Static variables) are stored as part of the Class object associated with that class.
It is stored in non heap area which is called Method Area


# OOPS Concepts

* Polymorphism
* Inheritance
* Encapsulation
* Abstraction
* Association
* Aggregation
* Composition


## Polymorphism 
Definition : Allows us to perform a single action in different ways.

Two types of Polymorphism

1) **Compile time** - This type of polymorphism is achieved by method overloading or operator overloading.
 
    a) Method Overloading - When there are multiple functions with same name but different parameters then these functions are said to be overloaded. 

    b) Operator Overloading: Java also provide option to overload operators. For example, we can make the operator (‘+’) for string class to concatenate two strings.

2) Runtime Polymorphism - It is a process in which a function call to the overridden method is resolved at Runtime. This type of polymorphism is achieved by Method Overriding.

      a) Method overriding, on the other hand, occurs when a derived class has a definition for one of the member functions of the base class. That base function is said to be overridden.


Polymorphism can be achieved by
1) Overloading
2) Overriding

**Example**

Real life example of polymorphism: A person at the same time can have different characteristic. Like a man at the same time is a father, a husband, an employee. So the same person posses different behaviour in different situations. This is called polymorphism.

**Advantages & Usages of Polymorphism**

1) Method overloading allows methods that perform similar or closely related functions to be accessed through a common name. For example, a program performs operations on an array of numbers which can be int, float, or double type. Method overloading allows you to define three methods with the same name and different types of parameters to handle the array of operations.

2) Method overloading can be implemented on constructors allowing different ways to initialize objects of a class. This enables you to define multiple constructors for handling different types of initializations.

3) Method overriding allows a sub class to use all the general definitions that a super class provides and add specialized definitions through overridden methods.

4) Method overriding works together with inheritance to enable code reuse of existing classes without the need for re-compilation.

****************************************************************************************************************************************
**Inheritance in Java**

Inheritance represents a IS-A relationship. This object is a type of that object.

definition

1) **Inheritance in Java is a mechanism in which one class acquires all the properties and behaviors of a parent class.**
2) The idea behind inheritance in Java is that you can create new classes that are built upon existing classes. When you inherit from an existing class, you can reuse methods and fields of the parent class. Moreover, you can add new methods and fields in your current class also.
3) Inheritance represents the IS-A relationship which is also known as a parent-child relationship.
4) It is the mechanism in java by which one class is allow to inherit the features(fields and methods) of another class.
5) Inheritance is a mechanism wherein a new class is derived from an existing class. In Java, classes may inherit or acquire the properties and methods of other classes. A class derived from another class is called a subclass, whereas the class from which a subclass is derived is called a superclass. A subclass can have only one superclass, whereas a superclass may have one or more subclasses.
6) The process by which one class acquires the properties(data members) and functionalities(methods) of another class is called inheritance. The aim of inheritance is to provide the reusability of code so that a class has to write only the unique features and rest of the common properties and functionalities can be extended from the another class.

**Why inheritance is used in Java**
1) For Method Overriding (so runtime polymorphism can be achieved).
2) For Code Reusability.

**Types of Inheritance in Java**

1) Single Inheritance
2) Multilevel Inheritance
3) Hierarchical Inheritance
4) **Multiple Inheritance  (Through Interfaces)** -  In Multiple inheritance ,one class can have more than one superclass and inherit features from all parent classes. 
Please note that **Java does not support multiple inheritance with classes**. In java, we can achieve multiple inheritance only through Interfaces.
5) Hybrid Inheritance(Through Interfaces) - only with Interfaces


**Super/Constructor keyword**
1) The keyword super can be used to access any data member or methods of the parent class.
2) Super keyword can be used at variable, method and constructor level.
3) Call to super() must be the first statement in subclass Class constructor.
4) If a constructor does not explicitly invoke a superclass constructor, the Java compiler automatically inserts a call to the no-argument constructor of the superclass. If the superclass does not have a no-argument constructor, you will get a compile-time error. Object does have such a constructor, so if Object is the only superclass, there is no problem.
5) If a subclass constructor invokes a constructor of its superclass, either explicitly or implicitly, you might think that a whole chain of constructors called, all the way back to the constructor of Object. This, in fact, is the case. It is called constructor chaining..

How it is achieved - using extends keyword

Java Object Creation of Inherited Class
1) One sub class object is only created
2) super.getClass().getName() return sub class name

https://www.geeksforgeeks.org/gfact-52-java-object-creation-of-inherited-classes/

**Why multiple inheritance is not supported in java?**
1) To reduce the complexity and simplify the language, multiple inheritance is not supported in java.
2) There will be ambiguity

**Class Vs object**
Class - It is a template or blueprint from which objects are created.

****************************************************************************************************************************************

## Encapsulation in Java
1)	Is a mechanism of wrapping the data (variables) and code acting on the data (methods) together as a single unit. 
2)	In encapsulation, the variables of a class will be hidden from other classes, and can be accessed only through the methods of their current class. Therefore, it is also known as data hiding.

**To achieve encapsulation in Java**

  a) Declare the variables of a class as private.

  b) Provide public setter and getter methods to modify and view the variables values.


**Advantage of Encapsulation in Java**

a) By providing only a setter or getter method, you can make the class read-only or write-only. In other words, you can skip the getter or setter methods.

b) It(Setters) provides you the control over the data. Suppose you want to set the value of id which should be greater than 100 only, you can write the logic inside the setter method. You can write the logic not to store the negative numbers in the setter methods.

c) It is a way to achieve data hiding in Java because other class will not be able to access the data through the private data members.


****************************************************************************************************************************************
## Abstraction in Java

Definition:

1) Abstraction is selecting data from a larger pool to show only the relevant details and hides the irrelevant details.
2) abstraction is a process of hiding the implementation details from the user, only the functionality will be provided to the user. In other words, the user will have the information on what the object does instead of how it does it.

**Why**

It helps to reduce programming complexity and effort.

How to achieve
1)	Abstract classes and 
2)	interfaces.

**Example**

a) Mobile or TV

b) A car is viewed as a car rather than its individual components. Data Abstraction may also be defined as the process of identifying only the required characteristics of an object ignoring the irrelevant details.


****************************************************************************************************************************************

**Abstraction vs. Encapsulation**

Often encapsulation is misunderstood with Abstraction. Lets study-

a) Encapsulation is more about "How" to achieve a functionality
b) Abstraction is more about "What" a class can do.

**Example**

A simple example to understand this difference is a mobile phone. Where the complex logic in the circuit board is encapsulated in a touch screen, and the interface is provided to abstract it out.

****************************************************************************************************************************************

## Aggregation in Java

https://beginnersbook.com/2013/05/association/

Aggregation represents Has-A relationship (Student Has-A Address).

Aggregation is a special form of association. It is a relationship between two classes like association, however its a directional association, which means it is strictly a one way association. It represents a HAS-A relationship.


**Example**

For example, consider two classes Student class and Address class. Every student has an address so the relationship between student and address is a Has-A relationship. But if you consider its vice versa then it would not make any sense as an Address doesn’t need to have a Student necessarily.

**Why we need Aggregation?**

To maintain code re-usability. To understand this lets take the same example again. Suppose there are two other classes College and Staff along with above two classes Student and Address. In order to maintain Student’s address, College Address and Staff’s address we don’t need to use the same code again and again. We just have to use the reference of Address class while defining each of these classes like:

Student Has-A Address (Has-a relationship between student and address)
College Has-A Address (Has-a relationship between college and address)
Staff Has-A Address (Has-a relationship between staff and address)
****************************************************************************************************************************************

## Association in java?

Association establishes relationship between two separate classes through their objects. The relationship can be one to one, One to many, many to one and many to many.

Both the classes represent two separate entities.
****************************************************************************************************************************************



## Casting

Converting one type of value to another is called as Type Casting.

Two type of casting:
1)	Up Casting
2)	Down Casting

You can cast an instance of a child class to its parent class. Casting an object of child class to a parent class is called upcasting.

Vehicle    v2 = new  TwoWheeler();
Casting an object of a parent class to its child class is called downcasting.

TwoWheeler v3 = (TwoWheeler) new  Vehicle();
If parent class has m1 & m2 method and child class has m1 and m3 method.
```
class Parent {
	int a = 10;
	int b = 30;

	void m1() {
		System.out.println("m1 from Prent");
	}

	void m2() {
		System.out.println("m2 from Prent");
	}
}

class Child extends Parent {
	int a = 20;
	int c = 40;

	void m1() {
		System.out.println("m1 from Child");
	}

	void m3() {
		System.out.println("m3 from Child");
	}
}

public class First {

	public static void main(String[] args) {

		Parent p = new Child();
		p.m1(); // Overriding is occurring - Child method m1 executes
		p.m2(); // inheritance
		// p.m3(); // INVALID statement
		((Child) p).m3(); // to wider the scope of parent reference type to access child method
		// There is no way of accessing parent m1 method if object is instantiated with
		// child.
		System.out.println(p.a); // 10
		System.out.println(((Child) p).a); // 20
		System.out.println(p.b);
		System.out.println(((Child) p).c);

	}

}
	
```





*************************************** START **************************************************

**java certificate note -1- Operator & Precedence**

![Alt text](/operatorPrecedence.png?raw=true "Optional Title")

```
& and | do not short circuit the expression but && and || do.

Bitwise operator 
Bitwise and (&) --> all bits are set, result is set
Bitwise or(|) --> any bit is set, result is set
Bitwise xor(^) --> one or more bit but not all bits is/are set, result will be set
Bitwise one Complement (~) -->
Bitwise left Shift (>>) -->  all the bits will be pushed to left, that removes left side bits and adds 0 at the right side
Bitwise Right Shift (<<) ( shows bigger number) -->  all the bits will be pushed to LEFT, that removes LEFT MOST bits and adds 0 at the RIGHT side

```
**Difference between Logical And ( && ) and Bitwise And (&)**

&& compares boolean only
```
int x = -10 --> (-) is unary operator
int x = 11-10 --> (-) is Arithmetic operator


int x = (-10)%(-3);  --> x is -1, not 1 --> % goes by numerator sign.
int x = (-10)%(3);  --> x is -1, not 1 --> % goes by numerator sign.
int x = (10)%(-3);  --> x is 1,  % goes by numerator sign.

```

Integer i ; i++ --> throws runtime exception as NullPointerException;
Integer i=10; i++ --> 11; */

*************************************** END **************************************************

*************************************** START **************************************************
**java certificate note -2- Exception**

![Alt text](/exceptionHandling.png?raw=true "Optional Title")


*************************************** END **************************************************

*************************************** START **************************************************

**java certificate note -3- Inheritance/ polymorphism / overloading/ overriding / interface / class - Completed**

**Inheritance**
```

1) method dynamic binding(runtime) works (if same name methods are defined in parent and child class)

2) dynamic binding does not work with static as static methods are tied to class.

3) static variables are copied from parent to child class so static variables declared in parent class can be accessed using child class name.

4) static methods are NOT copied from parent to child class so static methods declared in parent class can NOT be accessed using child class name. 

5) variable binding will be at compile time.6) final class cannot be extended 
```


**Static Variable in Inheritance**

**Static variable and method declared in Parent class can be accessed:**

```
staticVar;
Parent.staticVar;
Child.staticVar;
new Parent().staticVar;
new Child().staticVar;
```
**Instance variable and method declared in Parent class can be accessed:**
```
instanceVar;
new Parent().instanceVar;
new Child().instanceVar;
```

**Dynamic Binding**

When parent and child class have same method name and overriding exist - Dynamic biding happens and parent reference type has object of child class will access child method.

If parent method is throwing checked exception, child method is runtime or no exception, in case of overriding or dynamic binding, compilation error as parent object at compile time think about parent method which is having checked exception so should be handled.
```
 Parent ptoC = new Child();
 ptoC.commonM(); //dynamic binding concept - access child method
 ```
 
**Casting**

Parent reference type with child object, parent reference type can access only parent method, 
To enable access to child method, we need to use casting. 
```
Parent ptoC = new Child();
ptoC.parentM();
((Child) ptoC).childM();   // casting example
 ```
 
Parent class reference with child class object, to access child methods ( if not overriding ) requires CASTING otherwise compilation error.
 ```
 Child ctoP = (Child) new Parent(); INVALID CASTING
 ```
**Overriding**

The compiler performs the following checks when you override a nonprivate method:

The method from child class must have the same signature as the method in the parent class.

Access Identifier - Equal or Widening - The method from child class must be at least as accessible or more accessible than the method in the parent class.

The method from child class may not throw a checked exception that is new or broader than the class of any exception thrown from the parent class method.

If the method returns a value, it must be the same or a subclass of the method in the parent class.

Ex : parent method --> Object m(){}; Child method --> String m(){}; --> Correct

Java is not possible to override a private method in a parent class since the parent method is not accessible from the child class.

Java can redeclare a new method in the child class with the same or modified signature as the method in the parent class.

This method in the child class is a separate and independent method, unrelated to the parent version's method.

Override --> Final method cannot be overridden.

Override --> Private method cannot be overridden.

Override --> Static method cannot be overridden. Static method looks to overridden but it is hidden.

Override --> If a method cannot be inherited then it cannot be overridden.

*Exam Tip : If parent method is throwing checked exception, child method is runtime or no exception, in case of overriding or dynamic binding, compilation error as parent object at compile time think about parent method which is having checked exception so should be handled.*

 
**Exception with Overriding Rules**
When parent method has :

1) No Exception --> Overriding method can NOT throw checked exception.
2) Unchecked Exception--> Overriding method can Not throw checked exception.
3) Checked Exception --> Overriding method can NOT throw new or  broader checked exception

**Overloading**

Overloading --> In Overloading/polymorphism exception can differ. Access modifier can differ. 
Overloaded methods must have different method parameters from one another.
Overloaded methods may or may not define a different return type. 
Overloaded methods may or may not define different access modifiers. 


Using the same Method name but with different argument is called overloading.

Constructors can also be overloadedOverloaded Methods must have different argument set.

Overloaded Methods may have different return type.

Overloaded Methods may have different access modifier.

Overloaded Methods may throw different exception broader or narrowno restriction.

Methods from super class can also be overloaded in subclass.

Polymorphism applies to overriding not Overloading.

Determining which overloaded Method will be invoked is decided atcompile time on the basis of the reference type.

Overloaded methods can’t be defined by only changing their return type or access modifiers.
*************************************** END **************************************************

