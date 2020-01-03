# OCA

### Module 2: Java Basics
###### 1.Scope
```
for(int i=0;i<10;i++){
}
//x not in scope
```
###### 2.Structure of Java class
```
1.
package structure;
public class Structure{} - only one public class for a source file
class B {}

file name should be A.java

2.
package one;
import two;
public class A{
B b;
C c;
}
package one;
public class B{
A a;
two.C c;
}
package two;
public class C{
one.A a;
}
```

```
public abstract class AConcept{ //cannot create a subclass
 // if you subclass then you can make use of it

package sample;
public class NewStructure{

  public float getTemperature(){
     return temperature;
  }

  private float temperature;
  void NewStructure(){ // constructor
    temperature = 98.4F;
  }
  class AnInnerClass(){ // inner class
  }

  public void makeOne(){
    Aconcept ac = new AConcept();
  }
}
```

###### 3.Create exe
```
public static void main(String[] args)
//String... args -> replacement
$ java mypackage.MyProg today 99

```

###### 4.Import other java packages
```
import java.util.date
Date d = new Date();

package and sub-packages are different

```

### Module 3: Data types
###### 1.Declare and init
###### 2.Ref vs Primitive
###### 3.Read/write obj fields
###### 4.Obj Lifecycle
###### 5.Call Methods on Objects
###### 6.Stringbuilder
###### 7. Creating and manipulating strings

### Module 4: Operators and Decision
###### 1.Java operators
###### 2.Parenthesis
###### 3.Use == and equals()
###### 4.if else
###### 5.switch


### Module 5: Arrays
###### 1.Java operators
###### 2.Multi dimensional array
###### 3.Array List


### Module 6: Loop Constructs
###### 1.While
###### 2.Enhanced for loop
###### 3.Do while
###### 4.Compare loop
###### 5.Break and continue

### Module 7: Methods and Encapsulation
###### 1.Methods with args and return values
###### 2.Static keyword to method and fields
###### 3.Overloaded method
###### 4.Default and user defined constructors
###### 5.Create and overload constructors
###### 6.Access modifiers
###### 7.Apply encapsulation principle to class
###### 8.Effect of object references and primitive values

### Module 8: Inheritance
###### 1.Implement inheritance
###### 2.Polymorphism
###### 3.Diff type of reference and type of object
###### 4.Casting
###### 5.Super
###### 6.Abstract class and interfaces


### Module 9: Handling Exceptions
###### 1.Checked and run time exceptions
###### 2.Try-catch
###### 3.Exceptions
###### 4.Method that throws exception
###### 5.Common exception class and categories
