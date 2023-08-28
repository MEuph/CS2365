# Procedural Programming

## Step 1
- ### A procedure
  - A set of programming language statements to perform a task
  - E.g., a function
  - Operates on data items separated from the procedure
    - E.g, Fortran, Cobol, C

#### An example of a procedure is:

```java
// This is an encapsulation
class Procedure {
    // This is a procedure
    int average(int a, int b) {
        return (a + b) / 2;
    }
}
```

### Step 2
- In Procedural Programming, the data items are passed from one procedure to another

### Step 3
- Data is global to the entire procedures or program
- Data formats might change, thus the procedures must change

# Object Oriented Programming

- OOP is centered on creating ***objects*** rather than procedures

### Think of it like this:

- A box is an object. It has dimensions, contents, etc.
- Procedures for the box could include `open`, `close`, `destroy`, and more

- An Object is a melding of data and procedures that manipulate that data

- For objects
  - data are called `attributes`
  - procedures are called `methods`

## The four pillars of OOP

- ### Abstraction
  - A process of hiding the fine details of the implementation, and showing only the functionality to the user.
  - For example, `printf` in C has a lot of complexity in its implementation, but all the user needs to do is specify the format string and the parameters to the function
  - Without abstraction
    - Have the following buttons
      - "boil water",
      - "add cold water to kettle",
      - "add 1 spoon of ground coffee to clean cup",
      - "clean any dirty cups",
      - "etc..."
  - But *with* abstraction, we can simply replace this whole process with a "make coffee" button
- ### Encapsulation
  - A mechanism binding data and procedures
  - Object (class) encapsulating data and procedures
  - Easier than abstraction. I.E., a class needn't hide its implementation details
  - Only an object's methods directly manipulate its procedures (for private variables)
  - Other objects indirectly manipulate an object's attributes via the object's methods
    - Known as an ***object (programming) interface***
- ### Inheritance
  - Process of acquiring the properties of another object
  - Supports the concept of hierarchical classification
    - E.g., grandparents, parents, and me
    - A child inherits its general attributes from its parents
  - Class hierarchy abstracted
    - Defer complex details to the next level of abstraction
- ### Polymorphism
  - Meaning "many forms" from Greek
  - Same method name, but different implementations

#### Example of polymorphism

```java
abstract class Animal {
  protected void makeSound();
}

class Dog extends Animal {
  public void makeSound() {
    System.out.println("Bark!");
  }
}

class Cat extends Animal {
  public void makeSound() {
    System.out.println("Meow!");
  }
}

public class Main {
    public static void main(String[] args) {
        Animal dog, cat;
        dog = new Dog();
        cat = new Cat();
        
        dog.makeSound(); // Bark!
        cat.makeSound(); // Meow!
    }
}
```

#### Java is a very good language for OOP because it has all four pillars of OOP

# History of Java
 - Created in 1991
   - By a team (led by James Gosling, named the Green Team)
   - made at Sun Microsystems (now owned by Oracle)
   - Java was initially named `OAK`
 - The intention for Java was to design programs that could run consumer applications from computers
 - A browser named HotJava, could display animation and interact with users

### Applications vs Applets
- Two types of programs can be made with Java: Applications and Applets
  - Application
    - A stand-alone program which runs on your computer
    - Example: A word processor, a spreadsheet
  - Applets
    - A small application design to be ***transmitted*** over the internet from a web server and run in the browser

# The Compiler and the JVM

- Java Source files have a `.java` extension
- ***Most*** compilers
  - Translate source code into *executable* files containing *machine* code
  - Java does ***not*** do this
- The Java compiler
  - Translates a Java source file into a file containing *byte code* instructions
- Byte Code is ***NOT*** machine code
- The JVM converts the Byte Code into machine code.
- This allows Java to run on systems differing from the one the program was developed on