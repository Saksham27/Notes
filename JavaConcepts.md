# Access Modifiers :
### public 
public Members (variables, methods, and constructors) declared public within a public class are visible to any class in the Java program, whether these classes are in the same package or in another package.
### protected 
The protected fields or methods, cannot be used for classes and Interfaces. Fields, methods and constructors declared protected in a super-class can be accessed only by sub-classes in other packages. Classes in the same package can also access protected fields, methods and constructors as well, even if they are not a subclass of the protected member’s class.
### Default (no value)
The default access level is declared by not writing any access modifier at all. Any class, field, method or constructor that has no declared access modifier is accessible only by classes in the same package.
### private
The private (most restrictive) modifiers can be used for members but cannot be used for classes and Interfaces. Fields, methods or constructors declared private are strictly controlled, which means they cannot be accessed by anywhere outside the enclosing class.
# Modifiers :
### static
static can be used for members of a class. The static members of the class can be accessed without creating an object of a class.
### final
This modifier applicable to class, method, and variables. This modifier tells the compiler not to change the value of a variable once assigned. If applied to class, it cannot be sub-classed. If applied to a method, the method cannot be overridden in sub-class.
### abstract
There are situations in which you will want to define a super-class that declares the structure of a given abstraction without providing a complete implementation of every method. This modifier is applicable to class and methods only.
| Modifier | class | constructor | method | Data/variables |
|--|--|--|--|--|
| *public*    | yes | yes | yes | yes |
| *protected* |     | yes | yes | yes |
| *default*   | yes | yes | yes | yes |
| *final*     |     | yes | yes | yes |
| *static*    |     |     | yes |     |
| *final*     | yes |     | yes |     |

# Packages :
```java
package com.sct.calculate;
public  class  MyCalculation  {
	//This method calculate interst
	public  int  calculateInterest(int amount,  int rate)  {
	int intrerstAmount = amount * rate/100;  
	return intrerstAmount;  
	}  
}
```

 1. Calling with fully qualified name.  ` // line no 6 below`
 2. package import and then directly calling the method `// line no 7 below`
 
```java
 package com.sct.account;
 import com.sct.calculate.*;
 public  class  SalesTax  {
   public  static  void  main  (String args[]) {
      int interestAmount =  new com.sct.calculate.MyCalculation().calculateInterest(1000,  8); // line 6
      System.out.println("Interest Amount = "+ interestAmount);
      int intAmount2 =  new  MyCalculation().calculateInterest(1000,8); // line 7
      System.out.println("Interest Amount2= "+ intAmount2);
      }
}
```

# varargs :
In JDK 5, Java has included a feature that simplifies the creation of methods that need to take a variable number of arguments. This feature is called varargs and it is short-form for variable-length arguments. A method that takes a variable number of arguments is a varargs method.
Prior to JDK 5, variable-length arguments could be handled two ways. One using overloaded method(one for each) and another put the arguments into an array, and then pass this array to the method.
```java
public static void fun(int ... a) 
{
   // method body
}
```
This syntax tells the compiler that fun( ) can be called with zero or more arguments.
[Varargs explained in detail - GeeksForGeeks](https://www.geeksforgeeks.org/variable-arguments-varargs-in-java/)

# Object Oriented Programming  ( OOP's ) :

 - A class is a blueprint with some properties/behaviours and methods.
 - An object is an instance of a Class.
 - Three main features of OOP's - 
	1. **Encapsulation**
	2. **Inheritance**
	3. **Polymorphism**
### Encapsulation :
Encapsulation means putting together all the variables (instance variables) and the methods into a single unit called Class. It also means hiding data and methods within an Object. Encapsulation provides the security that keeps data and methods safe from inadvertent changes. Programmers sometimes refer to encapsulation as using a “black box,” or a device that you can use without regard to the internal mechanisms. A programmer can access and use the methods and data contained in the black box but cannot change them.
```java
package oopsconcept;
public class Mobile {	
	private String manufacturer;
	private String operating_system;
	public String model;
	private int cost;
	//Constructor to set properties/characteristics of object
	Mobile(String man, String o,String m, int c){
		this.manufacturer = man;
		this.operating_system=o;
		this.model=m;
		this.cost=c;
	}
	//Method to get access Model property of Object
	public String getModel(){
		return this.model;
	}
	// We can add other method to get access to other properties
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA5OTEzMTMxNl19
-->