Here’s a comprehensive list of topics for **Core Java** and **Spring Boot**:

### **Core Java Concepts**
1. **Basic Concepts**
   - Variables and Data Types
   - Operators
   - Control Statements (if, switch)
   - Loops (for, while, do-while)

2. **Object-Oriented Programming (OOP)**
   - Classes and Objects
   - Constructors
   - Inheritance
   - Polymorphism (Method Overloading, Method Overriding)
   - Abstraction (Abstract Class, Interface)
   - Encapsulation
   - Static and Final Keywords
   - Nested Classes

3. **Exception Handling**
   - try-catch
   - throw and throws
   - finally
   - Custom Exceptions

4. **Collections Framework**
   - List, Set, Map Interfaces
   - ArrayList, LinkedList, HashSet, TreeSet, HashMap, LinkedHashMap, TreeMap
   - Iterator and ListIterator
   - Comparable and Comparator

5. **Multithreading and Concurrency**
   - Thread Lifecycle
   - Creating Threads (Thread Class, Runnable Interface)
   - Synchronization
   - Executor Framework
   - Concurrency Utilities (CountDownLatch, Semaphore, CyclicBarrier)
   - Deadlock, Race Conditions

6. **Java I/O**
   - File Handling (FileReader, FileWriter, BufferedReader, BufferedWriter)
   - Byte Streams vs Character Streams
   - Serialization and Deserialization

7. **Java 8 Features**
   - Lambda Expressions
   - Stream API
   - Optional Class
   - Functional Interfaces (Predicate, Consumer, Supplier, Function)
   - Method References
   - Default and Static Methods in Interfaces

8. **Generics**
   - Generic Classes
   - Bounded Types
   - Wildcards

9. **Java Memory Management**
   - Stack vs Heap Memory
   - Garbage Collection
   - JVM, JDK, JRE

10. **Annotations**
    - Built-in Annotations
    - Custom Annotations

11. **Reflection API**
    - Accessing Methods and Fields at Runtime

12. **Networking in Java**
    - Sockets (TCP, UDP)
    - URL and HttpURLConnection

13. **JDBC (Java Database Connectivity)**
    - Establishing Connection
    - CRUD Operations
    - PreparedStatement vs Statement
    - Transactions

---

# 1. Basic Concepts

### Variables and Data Types in Java

#### **1. Variables in Java:**

A variable is a container that holds data during the execution of a Java program. Each variable in Java must have a **data type** that defines the kind of value it can hold, such as integers, floating-point numbers, or strings.

##### **Types of Variables in Java:**
- **Local Variables:** Declared inside methods, constructors, or blocks. They are created when the method is called and destroyed once the method finishes executing.
- **Instance Variables:** Declared inside a class but outside any method. They are associated with instances of a class (object-level).
- **Static Variables (Class Variables):** Declared with the `static` keyword inside a class, but outside methods. These variables belong to the class rather than an instance of the class.

#### **2. Data Types in Java:**

Data types specify the size and type of values that can be stored in variables. Java has two categories of data types:

##### **a) Primitive Data Types:**
1. **byte** (1 byte) - Stores whole numbers from -128 to 127
2. **short** (2 bytes) - Stores whole numbers from -32,768 to 32,767
3. **int** (4 bytes) - Stores whole numbers from -2^31 to 2^31-1
4. **long** (8 bytes) - Stores whole numbers from -2^63 to 2^63-1
5. **float** (4 bytes) - Stores fractional numbers up to 7 decimal digits
6. **double** (8 bytes) - Stores fractional numbers up to 15 decimal digits
7. **char** (2 bytes) - Stores single characters using Unicode (e.g., 'a', 'A', '1', etc.)
8. **boolean** (1 bit) - Stores true or false values

##### **b) Non-Primitive Data Types (Reference Types):**
1. **String**
2. **Arrays**
3. **Classes**
4. **Interfaces**
5. **Enums**

#### **Syntax for Declaring a Variable:**
```java
data_type variable_name = value;
```
- `data_type`: The type of the variable (e.g., int, double, String).
- `variable_name`: The name of the variable.
- `value`: The value assigned to the variable.

### **Example:**
```java
public class VariablesDemo {

    // Instance variable
    int instanceVariable = 20;

    // Static variable (Class variable)
    static String staticVariable = "Hello, World!";

    public static void main(String[] args) {
        
        // Local variables
        int localVariable = 10;
        double decimalNumber = 10.5;
        char grade = 'A';
        boolean isPassed = true;

        // Displaying local variables
        System.out.println("Integer: " + localVariable);
        System.out.println("Decimal Number: " + decimalNumber);
        System.out.println("Grade: " + grade);
        System.out.println("Passed: " + isPassed);

        // Accessing static variable
        System.out.println("Static Variable: " + staticVariable);

        // Creating an object to access instance variable
        VariablesDemo demo = new VariablesDemo();
        System.out.println("Instance Variable: " + demo.instanceVariable);
    }
}
```

### **Explanation:**
- **Local Variables:** `localVariable`, `decimalNumber`, `grade`, and `isPassed` are declared inside the `main()` method and only exist within that method.
- **Instance Variable:** `instanceVariable` is declared inside the class and can be accessed using an object of the class.
- **Static Variable:** `staticVariable` is shared across all instances of the class and can be accessed directly using the class name or inside a static method like `main()`.

### **Output:**
```
Integer: 10
Decimal Number: 10.5
Grade: A
Passed: true
Static Variable: Hello, World!
Instance Variable: 20
```

This example demonstrates the use of various types of variables in Java, including their scopes and how they are initialized and accessed.

---
---
---

### Operators in Java

Operators in Java are symbols that perform operations on variables and values. They are used to perform tasks like arithmetic calculations, comparisons, logical operations, etc. Java has several types of operators, each serving different purposes.

#### **Types of Operators in Java:**

1. **Arithmetic Operators**
2. **Assignment Operators**
3. **Relational (Comparison) Operators**
4. **Logical Operators**
5. **Unary Operators**
6. **Bitwise Operators**
7. **Ternary Operator**
8. **Shift Operators**

---

### **1. Arithmetic Operators:**
These operators are used to perform basic arithmetic operations like addition, subtraction, multiplication, etc.

| Operator | Description     | Example      |
|----------|-----------------|--------------|
| `+`      | Addition        | `a + b`      |
| `-`      | Subtraction     | `a - b`      |
| `*`      | Multiplication  | `a * b`      |
| `/`      | Division        | `a / b`      |
| `%`      | Modulus (Remainder) | `a % b`  |

#### **Example:**
```java
int a = 10;
int b = 3;

System.out.println("Addition: " + (a + b));      // Output: 13
System.out.println("Subtraction: " + (a - b));   // Output: 7
System.out.println("Multiplication: " + (a * b));// Output: 30
System.out.println("Division: " + (a / b));      // Output: 3
System.out.println("Modulus: " + (a % b));       // Output: 1
```

---

### **2. Assignment Operators:**
These operators are used to assign values to variables.

| Operator | Description               | Example  |
|----------|---------------------------|----------|
| `=`      | Assign value               | `a = 10` |
| `+=`     | Add and assign             | `a += 5` |
| `-=`     | Subtract and assign        | `a -= 5` |
| `*=`     | Multiply and assign        | `a *= 5` |
| `/=`     | Divide and assign          | `a /= 5` |
| `%=`     | Modulus and assign         | `a %= 5` |

#### **Example:**
```java
int x = 5;
x += 3;  // x = x + 3; x is now 8
x -= 2;  // x = x - 2; x is now 6
System.out.println("Value of x: " + x);  // Output: 6
```

---

### **3. Relational (Comparison) Operators:**
These operators are used to compare two values or variables. They return a boolean result (`true` or `false`).

| Operator | Description              | Example    |
|----------|--------------------------|------------|
| `==`     | Equal to                 | `a == b`   |
| `!=`     | Not equal to             | `a != b`   |
| `>`      | Greater than             | `a > b`    |
| `<`      | Less than                | `a < b`    |
| `>=`     | Greater than or equal to | `a >= b`   |
| `<=`     | Less than or equal to    | `a <= b`   |

#### **Example:**
```java
int a = 10;
int b = 20;

System.out.println(a == b);  // false
System.out.println(a != b);  // true
System.out.println(a > b);   // false
System.out.println(a < b);   // true
```

---

### **4. Logical Operators:**
Logical operators are used to combine multiple conditions or perform logical operations. They return a boolean result.

| Operator | Description           | Example     |
|----------|-----------------------|-------------|
| `&&`     | Logical AND            | `a && b`    |
| `||`     | Logical OR             | `a || b`    |
| `!`      | Logical NOT            | `!a`        |

#### **Example:**
```java
boolean x = true;
boolean y = false;

System.out.println(x && y);  // false (AND)
System.out.println(x || y);  // true (OR)
System.out.println(!x);      // false (NOT)
```

---

### **5. Unary Operators:**
Unary operators operate on a single operand. They are commonly used for incrementing, decrementing, negating, etc.

| Operator | Description              | Example     |
|----------|--------------------------|-------------|
| `++`     | Increment by 1           | `a++` or `++a` |
| `--`     | Decrement by 1           | `a--` or `--a` |
| `+`      | Unary plus               | `+a`        |
| `-`      | Unary minus              | `-a`        |
| `!`      | Logical NOT              | `!a`        |

#### **Example:**
```java
int a = 10;
System.out.println(++a);  // Pre-increment: Output is 11
System.out.println(a++);  // Post-increment: Output is 11, then a becomes 12
System.out.println(--a);  // Pre-decrement: Output is 11
```

---

### **6. Bitwise Operators:**
These operators work on bits and perform bit-by-bit operations.

| Operator | Description          | Example  |
|----------|----------------------|----------|
| `&`      | Bitwise AND          | `a & b`  |
| `|`      | Bitwise OR           | `a | b`  |
| `^`      | Bitwise XOR          | `a ^ b`  |
| `~`      | Bitwise Complement   | `~a`     |

#### **Example:**
```java
int a = 5;  // In binary: 101
int b = 3;  // In binary: 011

System.out.println(a & b);  // Output: 1 (001)
System.out.println(a | b);  // Output: 7 (111)
System.out.println(a ^ b);  // Output: 6 (110)
System.out.println(~a);     // Output: -6 (Inverts the bits)
```

---

### **7. Ternary Operator:**
The ternary operator (`? :`) is a shorthand for `if-else` statements. It evaluates a boolean expression and returns one of two values based on whether the condition is true or false.

#### **Syntax:**
```java
condition ? value_if_true : value_if_false;
```

#### **Example:**
```java
int a = 10;
int b = 20;
int max = (a > b) ? a : b;
System.out.println("Max value is: " + max);  // Output: Max value is 20
```

---

### **8. Shift Operators:**
Shift operators are used to shift bits of a number left or right, effectively multiplying or dividing the number by powers of two.

| Operator | Description         | Example  |
|----------|---------------------|----------|
| `<<`     | Left shift          | `a << 2` |
| `>>`     | Right shift         | `a >> 2` |
| `>>>`    | Unsigned right shift | `a >>> 2`|

#### **Example:**
```java
int a = 8;  // Binary: 1000

System.out.println(a << 2);  // Output: 32 (Left shift by 2, equivalent to multiplying by 4)
System.out.println(a >> 2);  // Output: 2 (Right shift by 2, equivalent to dividing by 4)
```

---

### **Example Code Using Multiple Operators:**
```java
public class OperatorsDemo {
    public static void main(String[] args) {
        int a = 10, b = 5, c = 15;

        // Arithmetic Operators
        System.out.println("Addition: " + (a + b));
        System.out.println("Multiplication: " + (a * b));

        // Assignment Operator
        a += b;
        System.out.println("a after += : " + a);

        // Relational Operator
        System.out.println("Is a > b? " + (a > b));

        // Logical Operators
        boolean result = (a > b) && (c > a);
        System.out.println("Logical AND: " + result);

        // Ternary Operator
        int max = (a > b) ? a : b;
        System.out.println("Maximum value: " + max);

        // Bitwise Operator
        System.out.println("Bitwise AND: " + (a & b));
    }
}
```

### **Output:**
```
Addition: 15
Multiplication: 50
a after += : 15
Is a > b? true
Logical AND: true
Maximum value: 15
Bitwise AND: 0
```

This example demonstrates the use of various operators such as arithmetic, assignment, relational, logical, ternary, and bitwise operators.

---
---
---

### Control Statements in Java

Control statements are used to control the flow of execution in a program, based on certain conditions. They help make decisions (conditional execution) or execute code repetitively (loops). Here, we will focus on **decision-making** control statements: `if` and `switch`.

#### **Types of Control Statements:**
1. **if Statements**
2. **switch Statements**

---

### **1. if Statements:**

The `if` statement allows a block of code to be executed based on a condition. If the condition is true, the block of code inside the `if` statement will run; otherwise, it will be skipped.

#### **Syntax:**
```java
if (condition) {
    // Code to execute if condition is true
}
```

#### **Types of `if` Statements:**
1. **Simple `if` statement**
2. **if-else statement**
3. **if-else-if ladder**
4. **Nested `if` statement**

---

### **1.1. Simple `if` Statement:**

This executes a block of code if the condition is true.

#### **Example:**
```java
int number = 10;
if (number > 5) {
    System.out.println("Number is greater than 5.");
}
// Output: Number is greater than 5.
```

---

### **1.2. if-else Statement:**

This executes one block of code if the condition is true, and another block if the condition is false.

#### **Syntax:**
```java
if (condition) {
    // Code to execute if condition is true
} else {
    // Code to execute if condition is false
}
```

#### **Example:**
```java
int number = 3;
if (number > 5) {
    System.out.println("Number is greater than 5.");
} else {
    System.out.println("Number is less than or equal to 5.");
}
// Output: Number is less than or equal to 5.
```

---

### **1.3. if-else-if Ladder:**

This is used when multiple conditions need to be checked in sequence. The first block whose condition is true gets executed, and the rest are skipped.

#### **Syntax:**
```java
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition2 is true
} else {
    // Code to execute if none of the above conditions are true
}
```

#### **Example:**
```java
int number = 20;

if (number > 0 && number <= 10) {
    System.out.println("Number is between 1 and 10.");
} else if (number > 10 && number <= 20) {
    System.out.println("Number is between 11 and 20.");
} else {
    System.out.println("Number is greater than 20.");
}
// Output: Number is between 11 and 20.
```

---

### **1.4. Nested `if` Statement:**

An `if` statement inside another `if` statement is called nested `if`. It is useful when one condition depends on another.

#### **Syntax:**
```java
if (condition1) {
    if (condition2) {
        // Code to execute if both conditions are true
    }
}
```

#### **Example:**
```java
int number = 15;

if (number > 0) {
    if (number < 20) {
        System.out.println("Number is positive and less than 20.");
    }
}
// Output: Number is positive and less than 20.
```

---

### **2. switch Statement:**

The `switch` statement is used to execute one block of code among multiple options based on the value of a variable. It is an alternative to the `if-else-if` ladder, typically used when a variable needs to be compared with multiple constant values.

#### **Syntax:**
```java
switch (expression) {
    case value1:
        // Code to execute if expression equals value1
        break;
    case value2:
        // Code to execute if expression equals value2
        break;
    // Add more cases as needed
    default:
        // Code to execute if none of the above cases match
}
```

#### **Key Points:**
- Each `case` must end with a `break;` statement to prevent fall-through (executing subsequent cases).
- The `default` case is optional but is executed if no case matches the expression.

---

### **2.1. Example of a `switch` Statement:**
```java
int day = 3;

switch (day) {
    case 1:
        System.out.println("Sunday");
        break;
    case 2:
        System.out.println("Monday");
        break;
    case 3:
        System.out.println("Tuesday");
        break;
    case 4:
        System.out.println("Wednesday");
        break;
    case 5:
        System.out.println("Thursday");
        break;
    case 6:
        System.out.println("Friday");
        break;
    case 7:
        System.out.println("Saturday");
        break;
    default:
        System.out.println("Invalid day");
}
// Output: Tuesday
```

---

### **2.2. Using `switch` with Strings (Java 7 and above):**
In Java 7, `switch` was enhanced to allow String comparisons.

#### **Example:**
```java
String color = "Red";

switch (color) {
    case "Red":
        System.out.println("You chose Red.");
        break;
    case "Blue":
        System.out.println("You chose Blue.");
        break;
    default:
        System.out.println("Color not recognized.");
}
// Output: You chose Red.
```

---

### **2.3. `switch` with Enums:**
Enums (enumerated types) can also be used in `switch` statements.

#### **Example:**
```java
enum Day { SUNDAY, MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY }

Day day = Day.MONDAY;

switch (day) {
    case SUNDAY:
        System.out.println("Sunday");
        break;
    case MONDAY:
        System.out.println("Monday");
        break;
    // Add other cases here
    default:
        System.out.println("Invalid day");
}
// Output: Monday
```

---

### **Complete Example Using Both `if` and `switch`:**
```java
public class ControlStatementsDemo {
    public static void main(String[] args) {
        // Example of if-else
        int number = 15;
        if (number > 0) {
            System.out.println("Number is positive.");
        } else {
            System.out.println("Number is negative or zero.");
        }

        // Example of switch
        int month = 4;
        switch (month) {
            case 1:
                System.out.println("January");
                break;
            case 2:
                System.out.println("February");
                break;
            case 3:
                System.out.println("March");
                break;
            case 4:
                System.out.println("April");
                break;
            default:
                System.out.println("Invalid month");
        }
    }
}
```

### **Output:**
```
Number is positive.
April
```

---

### Summary of Control Statements:

- **if statement**: Executes code based on a condition.
- **if-else statement**: Chooses between two blocks of code based on a condition.
- **if-else-if ladder**: Used for multiple conditions in a sequence.
- **switch statement**: Selects and executes one block of code based on a variable's value. It is generally more readable than an `if-else-if` ladder when there are many constant comparisons.

---
---
---

### Loops in Java

Loops allow a block of code to be executed repeatedly based on a condition. The loop will keep executing the block until the specified condition evaluates to false. Java provides three main types of loops:

1. **for loop**
2. **while loop**
3. **do-while loop**

---

### **1. for Loop:**

The `for` loop is used when you know in advance how many times you want to iterate over a block of code. It is the most commonly used loop for definite iterations.

#### **Syntax:**
```java
for (initialization; condition; update) {
    // Code to execute in each iteration
}
```

- **initialization**: Initializes a loop counter or a control variable, executed only once.
- **condition**: Checks the condition before every iteration. If true, the loop body is executed; if false, the loop terminates.
- **update**: Increments or decrements the loop counter after every iteration.

#### **Example:**
```java
for (int i = 1; i <= 5; i++) {
    System.out.println("Iteration: " + i);
}
// Output:
// Iteration: 1
// Iteration: 2
// Iteration: 3
// Iteration: 4
// Iteration: 5
```

---

### **1.1. Enhanced for Loop (for-each):**

This loop is mainly used to iterate over collections such as arrays or lists.

#### **Syntax:**
```java
for (dataType variable : collection) {
    // Code to execute for each item in the collection
}
```

#### **Example:**
```java
int[] numbers = {10, 20, 30, 40, 50};
for (int num : numbers) {
    System.out.println("Number: " + num);
}
// Output:
// Number: 10
// Number: 20
// Number: 30
// Number: 40
// Number: 50
```

---

### **2. while Loop:**

The `while` loop is used when you want to repeat a block of code as long as a condition is true. It checks the condition before executing the loop body.

#### **Syntax:**
```java
while (condition) {
    // Code to execute as long as condition is true
}
```

- **condition**: The condition is checked before entering the loop. If it's true, the loop continues to execute.

#### **Example:**
```java
int i = 1;
while (i <= 5) {
    System.out.println("Iteration: " + i);
    i++;  // Increment the counter
}
// Output:
// Iteration: 1
// Iteration: 2
// Iteration: 3
// Iteration: 4
// Iteration: 5
```

---

### **3. do-while Loop:**

The `do-while` loop is similar to the `while` loop, but with one key difference: it will execute the loop body **at least once** before checking the condition. This means the block of code runs first, and the condition is checked afterward.

#### **Syntax:**
```java
do {
    // Code to execute at least once
} while (condition);
```

- **condition**: After executing the loop body, the condition is checked. If it's true, the loop continues; if false, the loop stops.

#### **Example:**
```java
int i = 1;
do {
    System.out.println("Iteration: " + i);
    i++;  // Increment the counter
} while (i <= 5);
// Output:
// Iteration: 1
// Iteration: 2
// Iteration: 3
// Iteration: 4
// Iteration: 5
```

---

### **Comparison of Loops:**

| Loop Type      | Condition Check | Use Case |
|----------------|-----------------|----------|
| `for` loop     | Before each iteration | When the number of iterations is known |
| `while` loop   | Before each iteration | When the number of iterations is unknown, but condition is needed first |
| `do-while` loop| After each iteration  | When the loop must execute at least once |

---

### **Complete Example of All Loops:**

```java
public class LoopExamples {
    public static void main(String[] args) {
        
        // for loop example
        System.out.println("for loop:");
        for (int i = 1; i <= 5; i++) {
            System.out.println("Iteration: " + i);
        }
        
        // while loop example
        System.out.println("\nwhile loop:");
        int j = 1;
        while (j <= 5) {
            System.out.println("Iteration: " + j);
            j++;
        }
        
        // do-while loop example
        System.out.println("\ndo-while loop:");
        int k = 1;
        do {
            System.out.println("Iteration: " + k);
            k++;
        } while (k <= 5);
    }
}
```

#### **Output:**
```
for loop:
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4
Iteration: 5

while loop:
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4
Iteration: 5

do-while loop:
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4
Iteration: 5
```

---

### Summary:

- **`for` loop**: Best for iterating a known number of times.
- **`while` loop**: Best for iterating until a condition becomes false.
- **`do-while` loop**: Ensures the block runs at least once, regardless of the condition.

These loops are essential for controlling the flow of execution when repetitive tasks are involved.

---
---
---

# 2. Object-Oriented Programming (OOP)

### Classes and Objects in Java

Java is an **object-oriented programming (OOP)** language, and the concepts of **classes** and **objects** are fundamental to its design. They allow you to model real-world entities and behaviors within your programs.

---

### **1. Class:**

A **class** in Java is a blueprint or template that defines properties (fields) and behaviors (methods) for objects. It represents a group of objects with common characteristics. A class provides a structure for creating objects.

#### **Syntax:**
```java
class ClassName {
    // Fields (attributes)
    dataType fieldName;

    // Methods (behaviors)
    returnType methodName(parameters) {
        // Method body
    }
}
```

#### **Example:**
```java
class Car {
    // Fields (properties)
    String make;
    String model;
    int year;

    // Method (behavior)
    void displayDetails() {
        System.out.println("Car Make: " + make);
        System.out.println("Car Model: " + model);
        System.out.println("Year: " + year);
    }
}
```

Here, `Car` is a class that defines three fields (`make`, `model`, and `year`) and one method (`displayDetails`) to display the car’s information.

---

### **2. Object:**

An **object** is an instance of a class. It represents a specific entity in memory that has attributes (values of fields) and behaviors (methods). Each object created from a class has its own set of properties.

#### **Creating an Object:**

To create an object, we use the `new` keyword along with the class constructor (a special method to initialize objects).

#### **Syntax:**
```java
ClassName objectName = new ClassName();
```

#### **Example:**
```java
public class Main {
    public static void main(String[] args) {
        // Creating an object of class Car
        Car myCar = new Car();
        
        // Setting properties
        myCar.make = "Toyota";
        myCar.model = "Corolla";
        myCar.year = 2020;
        
        // Calling a method on the object
        myCar.displayDetails();
    }
}
```

#### **Output:**
```
Car Make: Toyota
Car Model: Corolla
Year: 2020
```

In this example:
- `Car myCar = new Car();` creates an object of the `Car` class called `myCar`.
- The object's properties are set individually.
- The `displayDetails()` method is called to print the car's information.

---

### **3. Key Concepts in Classes and Objects:**

- **Fields (Instance Variables)**: These are attributes or properties that belong to the class. Each object of the class can have different values for these fields.
- **Methods**: These define the behavior of objects. Methods are functions inside a class that can manipulate the object’s properties or perform actions.
- **Constructor**: A special method used to initialize objects. It has the same name as the class and does not return any value.
  
  #### Example of a Constructor:
  ```java
  class Car {
      String make;
      String model;
      int year;

      // Constructor
      Car(String carMake, String carModel, int carYear) {
          make = carMake;
          model = carModel;
          year = carYear;
      }

      void displayDetails() {
          System.out.println("Car Make: " + make);
          System.out.println("Car Model: " + model);
          System.out.println("Year: " + year);
      }
  }

  public class Main {
      public static void main(String[] args) {
          // Creating an object using the constructor
          Car myCar = new Car("Honda", "Civic", 2019);
          myCar.displayDetails();
      }
  }
  ```

  #### **Output:**
  ```
  Car Make: Honda
  Car Model: Civic
  Year: 2019
  ```

- **Access Modifiers**: They define the visibility of classes, fields, and methods. Examples include `public`, `private`, `protected`, and default (no modifier).
  
  - **`public`**: Accessible from anywhere.
  - **`private`**: Accessible only within the class.
  - **`protected`**: Accessible within the same package or subclasses.

---

### **4. Important OOP Concepts Related to Classes and Objects:**

- **Encapsulation**: Bundling the data (fields) and methods that operate on the data into a single unit (class). It often involves restricting direct access to some of the object's components using access modifiers like `private`.

- **Inheritance**: A mechanism where a class (subclass) inherits properties and behaviors from another class (superclass). This allows for code reuse and polymorphic behavior.

- **Polymorphism**: The ability to process objects differently based on their data type or class. It allows objects of different types to be treated as objects of a common super class.

- **Abstraction**: Hiding the implementation details and showing only the functionality to the user.

---

### **Complete Example (Classes, Objects, Methods, and Constructor):**

```java
class Person {
    // Fields
    String name;
    int age;

    // Constructor
    Person(String personName, int personAge) {
        name = personName;
        age = personAge;
    }

    // Method to display details
    void displayPersonDetails() {
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating objects using the constructor
        Person person1 = new Person("Alice", 30);
        Person person2 = new Person("Bob", 25);

        // Calling methods on objects
        person1.displayPersonDetails();
        person2.displayPersonDetails();
    }
}
```

#### **Output:**
```
Name: Alice
Age: 30
Name: Bob
Age: 25
```

---

### **Summary:**

- A **class** is a blueprint that defines properties and behaviors.
- An **object** is an instance of a class, representing a specific entity in memory.
- Fields store data, and methods define behavior.
- Objects are created using constructors, and methods can be used to interact with objects.
  
By using classes and objects, Java enables the development of scalable, modular, and reusable code that models real-world entities effectively.

---
---
---

### Constructors in Java

A **constructor** is a special method in a class that is called when an object of the class is instantiated. Its primary purpose is to initialize the object’s properties (fields) and allocate memory for the object. Unlike regular methods, constructors have the same name as the class and do not have a return type.

---

### **Key Characteristics of Constructors:**

1. **Same Name as Class**: The constructor must have the same name as the class it belongs to.
2. **No Return Type**: Constructors do not have a return type, not even `void`.
3. **Called Automatically**: When you create an object using the `new` keyword, the constructor is called automatically.
4. **Overloading**: You can have multiple constructors in a class (constructor overloading) with different parameter lists.

---

### **Types of Constructors:**

1. **Default Constructor**: A constructor that does not take any parameters. If you do not define any constructor in a class, Java automatically provides a default constructor.

2. **Parameterized Constructor**: A constructor that takes parameters to initialize the object's fields with specific values when the object is created.

---

### **1. Default Constructor**

A **default constructor** is automatically provided by the Java compiler if no constructor is explicitly defined in the class. It initializes the object with default values (e.g., `0` for integers, `null` for objects).

#### **Example:**
```java
class Dog {
    String name;

    // Default constructor
    Dog() {
        name = "Unknown"; // Initializing the name with a default value
    }

    void display() {
        System.out.println("Dog's name: " + name);
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog1 = new Dog(); // Default constructor is called
        dog1.display(); // Output: Dog's name: Unknown
    }
}
```

---

### **2. Parameterized Constructor**

A **parameterized constructor** allows you to pass values to the object during its creation. This helps initialize the object with specific values provided by the user.

#### **Example:**
```java
class Car {
    String make;
    String model;
    int year;

    // Parameterized constructor
    Car(String carMake, String carModel, int carYear) {
        make = carMake;
        model = carModel;
        year = carYear; // Initializing fields with parameters
    }

    void displayDetails() {
        System.out.println("Car Make: " + make);
        System.out.println("Car Model: " + model);
        System.out.println("Year: " + year);
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating objects with parameterized constructor
        Car car1 = new Car("Toyota", "Camry", 2020);
        Car car2 = new Car("Honda", "Civic", 2019);

        // Calling methods on the objects
        car1.displayDetails();
        car2.displayDetails();
    }
}
```

#### **Output:**
```
Car Make: Toyota
Car Model: Camry
Year: 2020
Car Make: Honda
Car Model: Civic
Year: 2019
```

---

### **Constructor Overloading**

You can create multiple constructors in a class with different parameter lists. This is called **constructor overloading**. It allows objects to be initialized in different ways based on the arguments passed.

#### **Example:**
```java
class Book {
    String title;
    String author;
    double price;

    // Constructor with one parameter
    Book(String bookTitle) {
        title = bookTitle;
        author = "Unknown"; // Default value
        price = 0.0; // Default value
    }

    // Constructor with two parameters
    Book(String bookTitle, String bookAuthor) {
        title = bookTitle;
        author = bookAuthor;
        price = 0.0; // Default value
    }

    // Constructor with three parameters
    Book(String bookTitle, String bookAuthor, double bookPrice) {
        title = bookTitle;
        author = bookAuthor;
        price = bookPrice;
    }

    void displayDetails() {
        System.out.println("Title: " + title);
        System.out.println("Author: " + author);
        System.out.println("Price: " + price);
        System.out.println();
    }
}

public class Main {
    public static void main(String[] args) {
        Book book1 = new Book("Java Programming");
        Book book2 = new Book("Python Programming", "John Doe");
        Book book3 = new Book("C++ Programming", "Jane Doe", 29.99);

        book1.displayDetails();
        book2.displayDetails();
        book3.displayDetails();
    }
}
```

#### **Output:**
```
Title: Java Programming
Author: Unknown
Price: 0.0

Title: Python Programming
Author: John Doe
Price: 0.0

Title: C++ Programming
Author: Jane Doe
Price: 29.99
```

---

### **Summary:**

- **Constructors** are special methods used to initialize objects in Java.
- **Default constructors** are provided by Java if no constructors are defined, while **parameterized constructors** allow you to initialize objects with specific values.
- **Constructor overloading** allows a class to have multiple constructors with different parameter lists, enabling flexibility in object creation.

Understanding constructors is crucial for effective object-oriented programming in Java, as they lay the foundation for creating and initializing objects that encapsulate data and behavior.

---
---
---

### Inheritance in Java

**Inheritance** is a fundamental concept in object-oriented programming (OOP) that allows a new class (subclass or derived class) to inherit properties and behaviors (fields and methods) from an existing class (superclass or base class). This promotes code reusability and establishes a relationship between classes.

---

### **Key Features of Inheritance:**

1. **Code Reusability**: By inheriting from a superclass, a subclass can reuse existing code, which reduces redundancy and promotes maintainability.
2. **Method Overriding**: Subclasses can provide specific implementations of methods defined in the superclass, allowing for dynamic behavior.
3. **Hierarchical Relationships**: Inheritance enables a natural hierarchy between classes, representing "is-a" relationships. For example, a `Dog` is a type of `Animal`.
4. **Single Inheritance**: Java supports single inheritance, meaning a class can inherit from only one superclass, but it can implement multiple interfaces.

---

### **Types of Inheritance:**

1. **Single Inheritance**: A class inherits from one superclass.
2. **Multilevel Inheritance**: A class inherits from another class, which in turn inherits from another class, forming a chain.
3. **Hierarchical Inheritance**: Multiple subclasses inherit from a single superclass.
4. **Multiple Inheritance (through Interfaces)**: Java does not support multiple inheritance directly with classes to avoid ambiguity but allows it through interfaces.

---

### **1. Single Inheritance**

In single inheritance, one class extends another class.

#### **Example:**
```java
// Superclass (Base class)
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Subclass (Derived class)
class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat(); // Inherited method from Animal
        dog.bark(); // Method from Dog class
    }
}
```

#### **Output:**
```
This animal eats food.
The dog barks.
```

In this example, `Dog` is a subclass that inherits the `eat()` method from the `Animal` superclass.

---

### **2. Multilevel Inheritance**

In multilevel inheritance, a class is derived from another class, forming a chain of inheritance.

#### **Example:**
```java
// Superclass
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Intermediate subclass
class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

// Derived subclass
class Puppy extends Dog {
    void weep() {
        System.out.println("The puppy weeps.");
    }
}

public class Main {
    public static void main(String[] args) {
        Puppy puppy = new Puppy();
        puppy.eat(); // Inherited from Animal
        puppy.bark(); // Inherited from Dog
        puppy.weep(); // Method from Puppy class
    }
}
```

#### **Output:**
```
This animal eats food.
The dog barks.
The puppy weeps.
```

Here, `Puppy` inherits from `Dog`, which in turn inherits from `Animal`, allowing it to access methods from both classes.

---

### **3. Hierarchical Inheritance**

In hierarchical inheritance, multiple subclasses inherit from a single superclass.

#### **Example:**
```java
// Superclass
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

// Subclass 1
class Dog extends Animal {
    void bark() {
        System.out.println("The dog barks.");
    }
}

// Subclass 2
class Cat extends Animal {
    void meow() {
        System.out.println("The cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog();
        Cat cat = new Cat();

        dog.eat(); // Inherited from Animal
        dog.bark(); // Method from Dog class

        cat.eat(); // Inherited from Animal
        cat.meow(); // Method from Cat class
    }
}
```

#### **Output:**
```
This animal eats food.
The dog barks.
This animal eats food.
The cat meows.
```

Both `Dog` and `Cat` inherit from the `Animal` superclass, allowing them to access the `eat()` method.

---

### **Method Overriding**

When a subclass provides a specific implementation for a method that is already defined in its superclass, it is called **method overriding**. This allows the subclass to modify or enhance the behavior of the inherited method.

#### **Example:**
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound.");
    }
}

class Dog extends Animal {
    @Override // Annotation to indicate method overriding
    void sound() {
        System.out.println("Dog barks.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal = new Dog(); // Upcasting
        myAnimal.sound(); // Calls the overridden method in Dog
    }
}
```

#### **Output:**
```
Dog barks.
```

In this example, the `sound()` method in `Dog` overrides the method in `Animal`, providing a specific implementation.

---

### **Constructor in Inheritance**

When a subclass is created, the constructor of the superclass is called first (implicitly or explicitly) before the subclass constructor.

#### **Example:**
```java
class Animal {
    Animal() {
        System.out.println("Animal Constructor");
    }
}

class Dog extends Animal {
    Dog() {
        System.out.println("Dog Constructor");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog dog = new Dog(); // Creates a Dog object
    }
}
```

#### **Output:**
```
Animal Constructor
Dog Constructor
```

Here, when a `Dog` object is created, the constructor of the `Animal` class is called first, followed by the constructor of the `Dog` class.

---

### **Summary:**

- **Inheritance** allows a new class to inherit properties and behaviors from an existing class, promoting code reusability and establishing a natural hierarchy.
- It supports various types of inheritance, including single, multilevel, and hierarchical inheritance.
- **Method overriding** allows subclasses to provide specific implementations of methods defined in superclasses, enhancing or modifying inherited behavior.
- The constructor of the superclass is called when an object of the subclass is created, ensuring proper initialization.

Inheritance is a powerful feature that enhances the flexibility and maintainability of Java applications, allowing developers to create a structured and organized codebase.

---
---
---

### Polymorphism in Java

**Polymorphism** is a core concept in object-oriented programming (OOP) that allows objects to be treated as instances of their parent class. It provides a way to perform a single action in different forms. In Java, polymorphism is primarily divided into two types: **method overloading** and **method overriding**.

---

### **1. Method Overloading**

**Method Overloading** occurs when multiple methods in the same class have the same name but different parameter lists (different type, number, or both). It allows a class to have more than one method with the same name, making it easier to read and use.

#### **Key Features of Method Overloading:**

- **Same Method Name**: The method name must be the same.
- **Different Parameters**: The parameter list must differ (type, number, or order of parameters).
- **Return Type**: The return type can be the same or different, but it cannot be used alone to distinguish the overloaded methods.

#### **Example of Method Overloading:**
```java
class MathOperations {
    
    // Method to add two integers
    int add(int a, int b) {
        return a + b;
    }
    
    // Method to add three integers
    int add(int a, int b, int c) {
        return a + b + c;
    }
    
    // Method to add two double values
    double add(double a, double b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        MathOperations math = new MathOperations();
        
        System.out.println("Sum of two integers: " + math.add(5, 10)); // Calls first add method
        System.out.println("Sum of three integers: " + math.add(5, 10, 15)); // Calls second add method
        System.out.println("Sum of two doubles: " + math.add(5.5, 10.5)); // Calls third add method
    }
}
```

#### **Output:**
```
Sum of two integers: 15
Sum of three integers: 30
Sum of two doubles: 16.0
```

In this example, the `add` method is overloaded to handle different types and numbers of parameters, demonstrating method overloading.

---

### **2. Method Overriding**

**Method Overriding** occurs when a subclass provides a specific implementation for a method that is already defined in its superclass. It allows a subclass to define a behavior that is specific to the subclass, providing dynamic method dispatch.

#### **Key Features of Method Overriding:**

- **Same Method Name**: The method name must be the same as in the superclass.
- **Same Parameters**: The parameter list must be identical.
- **Return Type**: The return type must be the same or a subtype (covariant return type).
- **Inheritance Required**: Overriding can only happen in a subclass.

#### **Example of Method Overriding:**
```java
class Animal {
    void sound() {
        System.out.println("Animal makes a sound.");
    }
}

class Dog extends Animal {
    @Override // Annotation to indicate method overriding
    void sound() {
        System.out.println("Dog barks.");
    }
}

class Cat extends Animal {
    @Override // Annotation to indicate method overriding
    void sound() {
        System.out.println("Cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myAnimal; // Declare an Animal reference
        
        // Assign Dog object to Animal reference
        myAnimal = new Dog();
        myAnimal.sound(); // Calls Dog's sound() method
        
        // Assign Cat object to Animal reference
        myAnimal = new Cat();
        myAnimal.sound(); // Calls Cat's sound() method
    }
}
```

#### **Output:**
```
Dog barks.
Cat meows.
```

In this example, both `Dog` and `Cat` classes override the `sound` method of the `Animal` class. The method called depends on the actual object type (not the reference type), demonstrating polymorphism through method overriding.

---

### **Dynamic Method Dispatch**

Java supports dynamic method dispatch, which allows the method to be determined at runtime based on the object type rather than the reference type. This is a key feature of polymorphism in Java.

#### **Example:**
```java
class Vehicle {
    void start() {
        System.out.println("Vehicle is starting.");
    }
}

class Car extends Vehicle {
    @Override
    void start() {
        System.out.println("Car is starting.");
    }
}

class Bike extends Vehicle {
    @Override
    void start() {
        System.out.println("Bike is starting.");
    }
}

public class Main {
    public static void main(String[] args) {
        Vehicle myVehicle; // Declare a Vehicle reference
        
        myVehicle = new Car(); // Upcasting to Vehicle reference
        myVehicle.start(); // Calls Car's start() method
        
        myVehicle = new Bike(); // Upcasting to Vehicle reference
        myVehicle.start(); // Calls Bike's start() method
    }
}
```

#### **Output:**
```
Car is starting.
Bike is starting.
```

Here, the `start` method is determined at runtime based on the actual object type (either `Car` or `Bike`), showcasing the dynamic nature of polymorphism.

---

### **Summary:**

- **Polymorphism** allows objects to be treated as instances of their parent class and can take many forms, primarily through method overloading and method overriding.
- **Method Overloading** enables multiple methods with the same name but different parameter lists within the same class, enhancing code readability and usability.
- **Method Overriding** allows subclasses to provide specific implementations of methods defined in their superclasses, supporting dynamic method dispatch.
- **Dynamic Method Dispatch** ensures that the correct method is called based on the actual object type at runtime, rather than the reference type.

Polymorphism is a powerful feature that enhances the flexibility and extensibility of Java applications, allowing developers to create code that is more modular and easier to maintain.

---
---
---

### Abstraction in Java

**Abstraction** is a core principle of object-oriented programming (OOP) that focuses on exposing only the essential features of an object while hiding the unnecessary details. In Java, abstraction can be achieved using **abstract classes** and **interfaces**.

---

### **1. Abstract Class**

An **abstract class** is a class that cannot be instantiated on its own and is intended to be subclassed. It can contain both abstract methods (without a body) and concrete methods (with a body). Abstract classes are useful when you want to provide a common base class for a group of related classes while allowing for specific implementations in the subclasses.

#### **Key Features of Abstract Classes:**

- Can have both abstract and concrete methods.
- Can have instance variables and constructors.
- Can define non-static and static methods.
- Can provide default behavior through concrete methods.
- Use the `abstract` keyword in the class definition.

#### **Example of an Abstract Class:**
```java
abstract class Animal {
    // Abstract method (no body)
    abstract void sound();

    // Concrete method
    void eat() {
        System.out.println("Animal eats food.");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks.");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myDog = new Dog();
        myDog.sound(); // Calls Dog's sound() method
        myDog.eat();   // Calls Animal's eat() method

        Animal myCat = new Cat();
        myCat.sound(); // Calls Cat's sound() method
        myCat.eat();   // Calls Animal's eat() method
    }
}
```

#### **Output:**
```
Dog barks.
Animal eats food.
Cat meows.
Animal eats food.
```

In this example, `Animal` is an abstract class with an abstract method `sound()` and a concrete method `eat()`. The `Dog` and `Cat` classes extend `Animal` and provide their implementations of the `sound()` method.

---

### **2. Interface**

An **interface** in Java is a reference type similar to a class that can only contain abstract methods, static methods, default methods, and final variables (constants). Interfaces provide a way to achieve full abstraction and multiple inheritance in Java. A class can implement multiple interfaces, allowing for greater flexibility in designing the system.

#### **Key Features of Interfaces:**

- All methods in an interface are abstract by default (prior to Java 8).
- Can contain default and static methods (from Java 8 onwards).
- Cannot have instance variables (only constants).
- A class can implement multiple interfaces.
- Use the `interface` keyword in the definition.

#### **Example of an Interface:**
```java
interface Animal {
    // Abstract method (no body)
    void sound();

    // Default method
    default void eat() {
        System.out.println("Animal eats food.");
    }
}

class Dog implements Animal {
    @Override
    public void sound() {
        System.out.println("Dog barks.");
    }
}

class Cat implements Animal {
    @Override
    public void sound() {
        System.out.println("Cat meows.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal myDog = new Dog();
        myDog.sound(); // Calls Dog's sound() method
        myDog.eat();   // Calls default eat() method

        Animal myCat = new Cat();
        myCat.sound(); // Calls Cat's sound() method
        myCat.eat();   // Calls default eat() method
    }
}
```

#### **Output:**
```
Dog barks.
Animal eats food.
Cat meows.
Animal eats food.
```

In this example, `Animal` is an interface with an abstract method `sound()` and a default method `eat()`. The `Dog` and `Cat` classes implement the `Animal` interface and provide their implementations of the `sound()` method.

---

### **Differences Between Abstract Class and Interface**

| Feature                 | Abstract Class                              | Interface                                   |
|-------------------------|--------------------------------------------|---------------------------------------------|
| Instantiation           | Cannot be instantiated                     | Cannot be instantiated                      |
| Abstract Methods        | Can have both abstract and concrete methods| Can have only abstract methods (until Java 8) |
| Constructors            | Can have constructors                       | Cannot have constructors                    |
| Variables               | Can have instance variables                | Can only have static final variables       |
| Method Implementation    | Can provide default implementation          | Can provide default and static methods (from Java 8) |
| Inheritance             | Supports single inheritance                | Supports multiple inheritance               |

---

### **Summary:**

- **Abstraction** is an OOP principle that focuses on hiding the complex implementation details and showing only the essential features of an object.
- **Abstract classes** provide a base for subclasses and can contain both abstract and concrete methods, allowing for partial implementation.
- **Interfaces** define a contract that classes must adhere to and can provide default implementations for methods, supporting full abstraction.
- Using **abstract classes** and **interfaces** promotes code reusability and flexibility, making it easier to manage and extend applications.

---
---
---

### Encapsulation in Java

**Encapsulation** is one of the fundamental principles of object-oriented programming (OOP) that involves bundling the data (attributes) and methods (functions) that operate on that data into a single unit, typically called a class. It restricts direct access to some of the object's components and can prevent the accidental modification of data. Encapsulation is achieved through the use of **access modifiers** and the **getter** and **setter** methods.

---

### **Key Features of Encapsulation:**

1. **Data Hiding**: Encapsulation helps hide the internal state of an object from the outside world. The attributes of a class are typically made private, which restricts their direct access.

2. **Controlled Access**: Access to the attributes is provided through public methods (getters and setters). This allows you to control how the data is accessed and modified.

3. **Improved Code Maintenance**: Encapsulation makes it easier to maintain and modify code, as changes to the internal implementation can be made without affecting the outside code that uses the class.

4. **Enhanced Security**: By restricting access to certain methods and variables, encapsulation enhances the security of the application.

---

### **Example of Encapsulation:**

```java
class BankAccount {
    // Private attributes (data hiding)
    private String accountNumber;
    private double balance;

    // Constructor to initialize the account
    public BankAccount(String accountNumber, double initialBalance) {
        this.accountNumber = accountNumber;
        this.balance = initialBalance;
    }

    // Getter for accountNumber
    public String getAccountNumber() {
        return accountNumber;
    }

    // Getter for balance
    public double getBalance() {
        return balance;
    }

    // Method to deposit money
    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: $" + amount);
        } else {
            System.out.println("Invalid deposit amount.");
        }
    }

    // Method to withdraw money
    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrew: $" + amount);
        } else {
            System.out.println("Invalid withdraw amount or insufficient funds.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Create a BankAccount object
        BankAccount myAccount = new BankAccount("123456", 1000.0);
        
        // Accessing account details through public methods
        System.out.println("Account Number: " + myAccount.getAccountNumber());
        System.out.println("Initial Balance: $" + myAccount.getBalance());

        // Performing deposit and withdrawal
        myAccount.deposit(500.0);
        System.out.println("New Balance: $" + myAccount.getBalance());

        myAccount.withdraw(300.0);
        System.out.println("New Balance: $" + myAccount.getBalance());

        myAccount.withdraw(1500.0); // Invalid withdraw
    }
}
```

#### **Output:**
```
Account Number: 123456
Initial Balance: $1000.0
Deposited: $500.0
New Balance: $1500.0
Withdrew: $300.0
New Balance: $1200.0
Invalid withdraw amount or insufficient funds.
```

### **Explanation of the Example:**

1. **Private Attributes**: The attributes `accountNumber` and `balance` are marked as private, meaning they cannot be accessed directly from outside the `BankAccount` class.

2. **Getters and Setters**: The class provides public methods (`getAccountNumber()` and `getBalance()`) that allow controlled access to these attributes. There are no setters for `balance` or `accountNumber`, preventing external modification of these fields.

3. **Methods for Operations**: The `deposit` and `withdraw` methods manage the `balance` and include validation to ensure that the operations are valid.

4. **Encapsulation in Action**: In the `main` method, we create a `BankAccount` object and interact with it using the public methods, demonstrating how encapsulation allows for controlled access to the account's data.

---

### **Benefits of Encapsulation:**

- **Improved Code Organization**: Encapsulation helps organize code into logical units, making it easier to understand and maintain.
- **Increased Flexibility**: Changes to the internal implementation can be made without affecting the code that uses the class, providing greater flexibility in code management.
- **Security**: Sensitive data is protected from unauthorized access and modification, enhancing the overall security of the application.

---

### **Summary:**

Encapsulation is a key principle of object-oriented programming that promotes data hiding, controlled access to class attributes, and improved code organization. By using private variables and public methods (getters and setters), encapsulation helps create secure and maintainable code, allowing for better management of complex systems.

---
---
---

### Static and Final Keywords in Java

In Java, the `static` and `final` keywords are used to define specific behaviors for classes, methods, and variables. Understanding how to use these keywords is crucial for efficient Java programming.

---

### **1. Static Keyword**

The `static` keyword is used to indicate that a particular member (variable or method) belongs to the class itself rather than to any specific instance of the class. This means that static members can be accessed without creating an instance of the class.

#### **Key Features of Static:**

- **Static Variables**: A variable declared as static is shared among all instances of the class. It is initialized only once at the start of the execution.
  
- **Static Methods**: A static method can be called without an instance of the class. Static methods can only access static variables and call static methods.

- **Static Blocks**: Static blocks can be used for static initialization of a class.

#### **Example of Static:**
```java
class Counter {
    // Static variable
    static int count = 0;

    // Constructor
    Counter() {
        count++; // Incrementing count for each instance created
    }

    // Static method to get the count
    static int getCount() {
        return count;
    }
}

public class Main {
    public static void main(String[] args) {
        new Counter();
        new Counter();
        new Counter();

        // Accessing static method and variable
        System.out.println("Total objects created: " + Counter.getCount()); // Outputs: 3
    }
}
```

#### **Output:**
```
Total objects created: 3
```

In this example, the static variable `count` keeps track of how many instances of the `Counter` class have been created. The static method `getCount()` returns the current value of `count`.

---

### **2. Final Keyword**

The `final` keyword is used to define constants in Java. Once a variable, method, or class is declared as final, its value cannot be changed, the method cannot be overridden, and the class cannot be subclassed.

#### **Key Features of Final:**

- **Final Variables**: A variable declared as final cannot be reassigned once it is initialized. It acts as a constant.

- **Final Methods**: A final method cannot be overridden in subclasses.

- **Final Classes**: A final class cannot be subclassed (i.e., you cannot extend it).

#### **Example of Final:**
```java
final class Constants {
    // Final variable
    public static final double PI = 3.14159;

    // Final method
    public final void display() {
        System.out.println("This is a final method.");
    }
}

// Attempting to subclass a final class will cause a compile-time error
// class MoreConstants extends Constants {} // This line will cause an error

public class Main {
    public static void main(String[] args) {
        // Accessing final variable
        System.out.println("Value of PI: " + Constants.PI);

        // Creating an instance of Constants and calling a final method
        Constants constants = new Constants();
        constants.display();
    }
}
```

#### **Output:**
```
Value of PI: 3.14159
This is a final method.
```

In this example, `PI` is a final variable, meaning its value cannot be changed. The class `Constants` is marked as final, so it cannot be subclassed. The method `display()` is also final, preventing it from being overridden in any subclass.

---

### **Differences Between Static and Final:**

| Feature               | Static                                   | Final                                    |
|-----------------------|------------------------------------------|------------------------------------------|
| Purpose               | Belongs to the class, not instances      | Used to define constants and prevent modification |
| Usage                 | Variables, methods, blocks               | Variables, methods, classes              |
| Initialization        | Initialized once, shared among instances | Initialized once, cannot be changed      |
| Accessibility         | Can be accessed without an instance      | Once assigned, cannot be modified        |
| Overriding            | Static methods can be overridden         | Final methods cannot be overridden       |
| Inheritance           | Static members can be inherited          | Final classes cannot be subclassed       |

---

### **Summary:**

- The **static** keyword is used to create class-level members that can be accessed without instantiation. It allows for shared data among all instances of a class.
- The **final** keyword is used to define constants and prevent changes to variables, methods, or classes. It helps enforce immutability and maintain a clear structure in your code.

Using `static` and `final` effectively can lead to more organized, maintainable, and efficient code in Java applications.

---
---
---

### Nested Classes in Java

**Nested classes** are classes defined within another class in Java. They are a way to logically group classes that are only used in one place, which increases the encapsulation of the code and helps with organization. There are several types of nested classes in Java:

1. **Static Nested Classes**
2. **Non-static Nested Classes (Inner Classes)**
3. **Method-local Inner Classes**
4. **Anonymous Inner Classes**

---

### **1. Static Nested Classes**

A **static nested class** is defined with the `static` keyword and can access the static members (variables and methods) of the outer class. However, it cannot access non-static members directly.

#### **Example of Static Nested Class:**
```java
class OuterClass {
    private static String outerStaticVariable = "Outer static variable";

    static class StaticNestedClass {
        void display() {
            System.out.println("Accessing from static nested class: " + outerStaticVariable);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        // Creating an instance of the static nested class
        OuterClass.StaticNestedClass nestedObject = new OuterClass.StaticNestedClass();
        nestedObject.display();
    }
}
```

#### **Output:**
```
Accessing from static nested class: Outer static variable
```

---

### **2. Non-static Nested Classes (Inner Classes)**

An **inner class** is a nested class that does not have the `static` modifier. It can access all members (both static and non-static) of the outer class.

#### **Example of Inner Class:**
```java
class OuterClass {
    private String outerVariable = "Outer variable";

    class InnerClass {
        void display() {
            System.out.println("Accessing from inner class: " + outerVariable);
        }
    }
}

public class Main {
    public static void main(String[] args) {
        OuterClass outerObject = new OuterClass();
        OuterClass.InnerClass innerObject = outerObject.new InnerClass();
        innerObject.display();
    }
}
```

#### **Output:**
```
Accessing from inner class: Outer variable
```

---

### **3. Method-local Inner Classes**

A **method-local inner class** is defined within a method and is only accessible within that method. It can access local variables and parameters of the method (if they are final or effectively final).

#### **Example of Method-local Inner Class:**
```java
class OuterClass {
    void outerMethod() {
        final String localVariable = "Local variable";

        class MethodLocalInnerClass {
            void display() {
                System.out.println("Accessing from method-local inner class: " + localVariable);
            }
        }

        MethodLocalInnerClass localInner = new MethodLocalInnerClass();
        localInner.display();
    }
}

public class Main {
    public static void main(String[] args) {
        OuterClass outerObject = new OuterClass();
        outerObject.outerMethod();
    }
}
```

#### **Output:**
```
Accessing from method-local inner class: Local variable
```

---

### **4. Anonymous Inner Classes**

An **anonymous inner class** is a type of inner class without a name. It is defined and instantiated in a single statement. This type is often used to create objects with specific behavior (for example, implementing interfaces or extending classes) without having to create a separate named class.

#### **Example of Anonymous Inner Class:**
```java
abstract class AbstractClass {
    abstract void display();
}

public class Main {
    public static void main(String[] args) {
        // Anonymous inner class
        AbstractClass obj = new AbstractClass() {
            void display() {
                System.out.println("Accessing from anonymous inner class");
            }
        };

        obj.display();
    }
}
```

#### **Output:**
```
Accessing from anonymous inner class
```

---

### **Benefits of Nested Classes:**

1. **Logical Grouping**: Nested classes help logically group classes that are only used in one place, improving code readability and maintainability.

2. **Access to Outer Class Members**: Inner classes have access to the members of the outer class, which can simplify the code when closely related classes are working together.

3. **Encapsulation**: Nested classes can be kept private to the outer class, which enhances encapsulation and hides implementation details from the outside world.

4. **Code Organization**: Nested classes allow for better organization of classes that serve a specific purpose within the context of another class.

---

### **Summary:**

- **Static Nested Classes** are associated with the class itself rather than instances and can only access static members of the outer class.
- **Inner Classes** can access all members of the outer class and require an instance of the outer class to be created.
- **Method-local Inner Classes** are defined within a method and can access local variables of that method if they are effectively final.
- **Anonymous Inner Classes** provide a way to instantiate a class or implement an interface in a concise manner without formally naming the class.

Nested classes can enhance code organization, maintainability, and encapsulation, making them a valuable feature in Java programming.

---
---
---

# 3. Exception Handling

### try-catch in Java

In Java, the **try-catch** block is used for exception handling. It allows you to write code that may throw an exception while providing a way to handle that exception gracefully, ensuring that the program can continue to execute or terminate in a controlled manner.

---

### **Key Components of try-catch**

1. **try Block**: This block contains the code that may potentially throw an exception. If an exception occurs within this block, the flow of control is transferred to the corresponding catch block.

2. **catch Block**: This block is used to handle the exception thrown by the try block. You can have multiple catch blocks to handle different types of exceptions.

3. **finally Block (Optional)**: This block can be used after the try-catch blocks. The code within the finally block always executes, regardless of whether an exception occurred or not. It is typically used for cleanup activities, such as closing resources (files, database connections, etc.).

---

### **Basic Syntax**

```java
try {
    // Code that may throw an exception
} catch (ExceptionType e) {
    // Code to handle the exception
} finally {
    // Code that always executes (optional)
}
```

---

### **Example of try-catch**

Here’s a simple example that demonstrates the usage of try-catch for handling exceptions:

```java
public class Main {
    public static void main(String[] args) {
        try {
            // Code that may throw an exception
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // This will throw ArrayIndexOutOfBoundsException
        } catch (ArrayIndexOutOfBoundsException e) {
            // Handling the exception
            System.out.println("Error: " + e.getMessage());
        } finally {
            // This block will execute regardless of whether an exception occurred
            System.out.println("Execution completed.");
        }
    }
}
```

#### **Output:**
```
Error: Index 5 out of bounds for length 3
Execution completed.
```

---

### **Explanation of the Example:**

1. **try Block**: The code attempts to access an index that is out of bounds for the `numbers` array, which triggers an `ArrayIndexOutOfBoundsException`.

2. **catch Block**: When the exception is thrown, control is passed to the catch block. The catch block catches the `ArrayIndexOutOfBoundsException` and prints an error message. You can use the `getMessage()` method to retrieve a detailed message about the exception.

3. **finally Block**: The finally block executes after the try and catch blocks, regardless of whether an exception occurred or not. In this case, it prints "Execution completed."

---

### **Multiple catch Blocks**

You can have multiple catch blocks to handle different types of exceptions separately:

```java
public class Main {
    public static void main(String[] args) {
        try {
            int result = 10 / 0; // This will throw ArithmeticException
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // This will throw ArrayIndexOutOfBoundsException
        } catch (ArithmeticException e) {
            System.out.println("Arithmetic error: " + e.getMessage());
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array error: " + e.getMessage());
        } finally {
            System.out.println("Execution completed.");
        }
    }
}
```

#### **Output:**
```
Arithmetic error: / by zero
Execution completed.
```

In this case, since the `ArithmeticException` occurs first, the corresponding catch block handles it. The `ArrayIndexOutOfBoundsException` will not be executed since the program exits the try block at the first exception.

---

### **Catching Multiple Exceptions**

You can also catch multiple exceptions in a single catch block by using the pipe `|` operator:

```java
public class Main {
    public static void main(String[] args) {
        try {
            int result = 10 / 0; // This will throw ArithmeticException
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // This will throw ArrayIndexOutOfBoundsException
        } catch (ArithmeticException | ArrayIndexOutOfBoundsException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            System.out.println("Execution completed.");
        }
    }
}
```

#### **Output:**
```
Error: / by zero
Execution completed.
```

---

### **Best Practices for Using try-catch:**

1. **Catch Specific Exceptions**: Always catch specific exceptions before more general ones to avoid unexpected behavior.

2. **Avoid Empty Catch Blocks**: Do not leave catch blocks empty; always handle exceptions appropriately.

3. **Use Finally for Cleanup**: Use the finally block for cleanup code, like closing resources.

4. **Limit Scope of try Block**: Keep the code in the try block minimal to reduce the risk of unexpected exceptions.

5. **Log Exceptions**: Consider logging exceptions for debugging and monitoring purposes.

---

### **Summary**

The **try-catch** block is a powerful mechanism in Java for handling exceptions. It allows you to separate error-handling code from regular code, enhancing the robustness and readability of your programs. Properly using try-catch blocks can help you create more resilient applications that can handle errors gracefully without crashing.

---
---
---

### `throw` and `throws` in Java

In Java, both `throw` and `throws` are used for exception handling, but they serve different purposes. Understanding the distinction between them is crucial for effectively managing exceptions in your programs.

---

### **1. `throw` Statement**

The `throw` statement is used to explicitly throw an exception from a method or any block of code. When you throw an exception, you can either create a new instance of an exception class or rethrow an existing exception.

#### **Key Points about `throw`:**
- It is followed by an instance of the exception.
- It is used within the body of a method, constructor, or block.
- When an exception is thrown using `throw`, the normal flow of execution is interrupted, and control is transferred to the nearest catch block.

#### **Example of `throw`:**
```java
public class Main {
    // Method that throws an exception
    public static void checkAge(int age) {
        if (age < 18) {
            throw new IllegalArgumentException("Age must be 18 or older.");
        } else {
            System.out.println("Access granted.");
        }
    }

    public static void main(String[] args) {
        try {
            checkAge(15); // This will throw an exception
        } catch (IllegalArgumentException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

#### **Output:**
```
Error: Age must be 18 or older.
```

In this example, the `checkAge` method throws an `IllegalArgumentException` when the age is less than 18. The exception is caught in the `main` method, where we handle it appropriately.

---

### **2. `throws` Keyword**

The `throws` keyword is used in the method signature to indicate that a method can throw one or more exceptions. It is a way of signaling that the calling method must handle these exceptions, either by catching them or declaring them further up the call stack.

#### **Key Points about `throws`:**
- It is used in the method declaration.
- It indicates that the method may throw certain exceptions.
- The method can declare multiple exceptions, separated by commas.
- It is mainly used for checked exceptions, which must be either caught or declared.

#### **Example of `throws`:**
```java
public class Main {
    // Method that declares that it throws an exception
    public static void checkAge(int age) throws IllegalArgumentException {
        if (age < 18) {
            throw new IllegalArgumentException("Age must be 18 or older.");
        } else {
            System.out.println("Access granted.");
        }
    }

    public static void main(String[] args) {
        try {
            checkAge(15); // This will throw an exception
        } catch (IllegalArgumentException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

#### **Output:**
```
Error: Age must be 18 or older.
```

In this example, the `checkAge` method declares that it throws an `IllegalArgumentException`. The calling method (`main`) handles the exception using a try-catch block.

---

### **Differences Between `throw` and `throws`**

| Aspect                  | `throw`                                 | `throws`                             |
|-------------------------|-----------------------------------------|--------------------------------------|
| **Purpose**             | Used to explicitly throw an exception.  | Used to declare that a method can throw exceptions. |
| **Location**            | Used inside method bodies.              | Used in method declarations.         |
| **Usage**               | Follows an instance of an exception.    | Followed by one or more exception types. |
| **Control Flow**        | Interrupts the normal flow of execution. | Indicates that exceptions need to be handled by the caller. |

---

### **Summary**

- **`throw`** is used to throw an exception explicitly, while **`throws`** is used in the method signature to declare that the method can throw exceptions.
- Use `throw` when you want to generate an exception and pass control to the nearest catch block.
- Use `throws` to inform the caller of the method about potential exceptions, ensuring they are handled appropriately.

Together, `throw` and `throws` are essential for effective exception handling in Java, allowing developers to create robust applications that can gracefully handle error conditions.

---
---
---

### `finally` Block in Java

In Java, the `finally` block is used to execute a set of statements after a try-catch block, regardless of whether an exception was thrown or caught. It is typically used for cleanup operations, such as closing resources (like files or database connections) or executing important code that must run irrespective of the outcome of the try block.

---

### **Key Points about the `finally` Block:**

1. **Always Executes**: The code within the `finally` block always executes after the try block and any catch blocks, whether or not an exception occurred. The only exception is if the program exits abruptly, such as through a call to `System.exit()` or if the thread executing the code is interrupted.

2. **Resource Management**: It is commonly used for resource management, ensuring that resources are released properly even when exceptions occur.

3. **Can Be Used Without catch**: While it is typically used with a try-catch block, a `finally` block can also follow a try block without a catch block.

---

### **Basic Syntax**

```java
try {
    // Code that may throw an exception
} catch (ExceptionType e) {
    // Code to handle the exception
} finally {
    // Code that always executes
}
```

---

### **Example of `finally` Block**

Here’s an example that demonstrates the use of a `finally` block in Java:

```java
import java.io.File;
import java.io.FileReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) {
        FileReader reader = null;
        try {
            File file = new File("example.txt");
            reader = new FileReader(file);
            // Code that may throw an exception
            int data = reader.read();
            while (data != -1) {
                System.out.print((char) data);
                data = reader.read();
            }
        } catch (IOException e) {
            // Handling the exception
            System.out.println("Error reading file: " + e.getMessage());
        } finally {
            // Cleanup code
            try {
                if (reader != null) {
                    reader.close(); // Closing the FileReader
                }
            } catch (IOException e) {
                System.out.println("Error closing file: " + e.getMessage());
            }
            System.out.println("\nCleanup completed.");
        }
    }
}
```

#### **Output (If the file exists):**
```
[Contents of the file example.txt]
Cleanup completed.
```

#### **Output (If the file does not exist):**
```
Error reading file: example.txt (No such file or directory)
Cleanup completed.
```

---

### **Explanation of the Example:**

1. **try Block**: The code attempts to read data from a file. If the file is not found or cannot be read, an `IOException` may be thrown.

2. **catch Block**: If an `IOException` occurs, it is caught in the catch block, where we handle the error by printing an appropriate message.

3. **finally Block**: Regardless of whether an exception was thrown or caught, the finally block executes. Here, we check if the `reader` object is not null, and if so, we close it to free up system resources. Any exceptions thrown while closing the reader are caught in a nested try-catch block.

---

### **Use Case for `finally`**

The `finally` block is particularly useful in scenarios involving:
- **File Handling**: Ensuring files are closed after operations.
- **Network Connections**: Closing network connections after use.
- **Database Connections**: Closing database connections to avoid memory leaks.

---

### **Multiple try-catch-finally Blocks**

You can have multiple try-catch-finally blocks in a program. Each try block can have its own catch and finally blocks.

```java
public class Main {
    public static void main(String[] args) {
        try {
            System.out.println("Try block 1");
            int result = 10 / 0; // This will throw ArithmeticException
        } catch (ArithmeticException e) {
            System.out.println("Caught exception: " + e.getMessage());
        } finally {
            System.out.println("Finally block 1 executed.");
        }

        try {
            System.out.println("Try block 2");
            int[] numbers = {1, 2, 3};
            System.out.println(numbers[5]); // This will throw ArrayIndexOutOfBoundsException
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Caught exception: " + e.getMessage());
        } finally {
            System.out.println("Finally block 2 executed.");
        }
    }
}
```

#### **Output:**
```
Try block 1
Caught exception: / by zero
Finally block 1 executed.
Try block 2
Caught exception: Index 5 out of bounds for length 3
Finally block 2 executed.
```

In this example, both try blocks are executed independently, and their respective finally blocks are also executed, regardless of the exceptions caught.

---

### **Summary**

- The **`finally` block** is an essential part of exception handling in Java, ensuring that specific cleanup code runs regardless of the outcome of the try-catch blocks.
- It is particularly useful for resource management, such as closing files, database connections, or network sockets.
- Proper use of finally can help avoid resource leaks and ensure that applications run smoothly even in the face of exceptions.


---
---
---


### Custom Exceptions in Java

In Java, custom exceptions allow you to define your own exception classes to handle specific error conditions in your application. Custom exceptions can make your code more readable and maintainable by providing clearer error messages and handling unique situations that built-in exceptions may not cover.

---

### **Creating Custom Exceptions**

To create a custom exception, you typically extend the `Exception` class (for checked exceptions) or `RuntimeException` class (for unchecked exceptions). By doing so, you can create an exception that reflects the specific needs of your application.

### **Key Steps to Create a Custom Exception:**

1. **Define a Custom Exception Class**: Extend the `Exception` or `RuntimeException` class.
2. **Add Constructors**: Provide constructors that can pass error messages and/or cause exceptions.
3. **Use the Custom Exception**: Throw the custom exception in your code when a specific error condition occurs.

---

### **Example of Custom Exception**

Here’s a simple example that demonstrates how to create and use a custom exception:

#### **Step 1: Create a Custom Exception Class**

```java
// Custom exception class
public class InvalidAgeException extends Exception {
    // Constructor that accepts a message
    public InvalidAgeException(String message) {
        super(message); // Call the constructor of the parent class (Exception)
    }
}
```

#### **Step 2: Use the Custom Exception**

Now, let's use the custom exception in a method:

```java
public class Main {
    // Method that throws the custom exception
    public static void checkAge(int age) throws InvalidAgeException {
        if (age < 18) {
            throw new InvalidAgeException("Age must be 18 or older.");
        } else {
            System.out.println("Access granted.");
        }
    }

    public static void main(String[] args) {
        try {
            checkAge(15); // This will throw InvalidAgeException
        } catch (InvalidAgeException e) {
            System.out.println("Error: " + e.getMessage());
        }
    }
}
```

#### **Output:**
```
Error: Age must be 18 or older.
```

---

### **Explanation of the Example:**

1. **Custom Exception Class**: 
   - The `InvalidAgeException` class extends `Exception`. It has a constructor that accepts a string message, which is passed to the parent `Exception` class constructor using `super(message)`.

2. **checkAge Method**: 
   - This method checks if the provided age is less than 18. If it is, it throws an `InvalidAgeException`, providing a specific error message.

3. **Main Method**: 
   - In the `main` method, we call `checkAge(15)`, which results in throwing the custom exception. We catch the exception in the catch block and print the error message.

---

### **Advantages of Custom Exceptions**

- **Clarity**: Custom exceptions can provide clearer meaning for specific error conditions in your application.
- **Specificity**: They allow you to handle different types of errors in a more granular way, enabling better error management.
- **Maintainability**: Custom exceptions can make your code more readable and easier to maintain by organizing error handling around application-specific logic.

---

### **Best Practices for Custom Exceptions**

1. **Meaningful Names**: Name your custom exceptions clearly to reflect their purpose.
2. **Extend the Appropriate Class**: Extend `Exception` for checked exceptions and `RuntimeException` for unchecked exceptions based on your needs.
3. **Add Constructors**: Provide constructors that allow setting detailed error messages and, if necessary, chaining exceptions.
4. **Document Your Exceptions**: Document your custom exceptions to help other developers understand when and why they should be used.

---

### **Summary**

Custom exceptions in Java provide a way to handle specific error conditions unique to your application. By creating custom exception classes, you can improve the readability and maintainability of your code while providing more meaningful error handling. They are a powerful tool in creating robust applications that can effectively manage various error scenarios.

---
---
---

# 4. Collections Framework

### List, Set, and Map Interfaces in Java

In Java, the Collections Framework provides a set of interfaces and classes to store and manipulate groups of objects. The three most commonly used interfaces are **List**, **Set**, and **Map**. Each of these interfaces has its own characteristics and is used for different purposes.

---

## 1. **List Interface**

### **Description**
- The `List` interface represents an ordered collection (also known as a sequence) that allows duplicate elements. Lists can contain elements of any type and provide positional access to elements.

### **Key Features**
- **Ordered**: Elements are maintained in the order they are inserted.
- **Duplicates Allowed**: The same element can appear multiple times.
- **Access by Index**: Provides methods to access elements based on their position.

### **Common Implementations**
- **ArrayList**: Resizable array implementation of the `List` interface.
- **LinkedList**: Doubly linked list implementation of the `List` interface.

### **Example**
```java
import java.util.ArrayList;
import java.util.List;

public class ListExample {
    public static void main(String[] args) {
        List<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");
        fruits.add("Apple"); // Duplicates allowed

        System.out.println("Fruits List: " + fruits);
        System.out.println("First Fruit: " + fruits.get(0)); // Access by index
    }
}
```

#### **Output:**
```
Fruits List: [Apple, Banana, Orange, Apple]
First Fruit: Apple
```

---

## 2. **Set Interface**

### **Description**
- The `Set` interface represents a collection that does not allow duplicate elements. Sets are unordered and do not maintain any specific order for their elements.

### **Key Features**
- **No Duplicates**: Each element must be unique; duplicates are not allowed.
- **Unordered**: The elements are not stored in any particular order.
  
### **Common Implementations**
- **HashSet**: Uses a hash table to store elements, offering constant time performance for basic operations.
- **LinkedHashSet**: Maintains a linked list of entries to preserve the insertion order.
- **TreeSet**: Implements the `SortedSet` interface and stores elements in a sorted order.

### **Example**
```java
import java.util.HashSet;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        Set<String> colors = new HashSet<>();
        colors.add("Red");
        colors.add("Green");
        colors.add("Blue");
        colors.add("Red"); // Duplicates are ignored

        System.out.println("Colors Set: " + colors);
    }
}
```

#### **Output:**
```
Colors Set: [Red, Green, Blue]
```

---

## 3. **Map Interface**

### **Description**
- The `Map` interface represents a collection of key-value pairs. Each key is unique, and each key maps to exactly one value. Maps are not considered collections in the strict sense but are a part of the Collections Framework.

### **Key Features**
- **Key-Value Pair**: Each entry in a map consists of a key and a corresponding value.
- **Unique Keys**: Each key in a map must be unique, but values can be duplicated.
- **No Ordering**: Maps do not guarantee any specific order of elements.

### **Common Implementations**
- **HashMap**: Uses a hash table for storing the map, providing constant-time performance for most operations.
- **LinkedHashMap**: Maintains a linked list of entries to preserve insertion order.
- **TreeMap**: Implements the `NavigableMap` interface and stores entries in sorted order based on the keys.

### **Example**
```java
import java.util.HashMap;
import java.util.Map;

public class MapExample {
    public static void main(String[] args) {
        Map<String, Integer> studentScores = new HashMap<>();
        studentScores.put("Alice", 90);
        studentScores.put("Bob", 85);
        studentScores.put("Charlie", 95);
        studentScores.put("Alice", 92); // Updates the score for Alice

        System.out.println("Student Scores: " + studentScores);
        System.out.println("Bob's Score: " + studentScores.get("Bob")); // Access value by key
    }
}
```

#### **Output:**
```
Student Scores: {Alice=92, Bob=85, Charlie=95}
Bob's Score: 85
```

---

### Summary of Differences

| Feature        | List                 | Set                  | Map                   |
|----------------|----------------------|----------------------|-----------------------|
| Allows Duplicates | Yes                  | No                   | Yes (for values only) |
| Order          | Maintains insertion order | No specific order    | No specific order      |
| Access Method  | Index-based          | Not applicable       | Key-based             |
| Common Implementations | ArrayList, LinkedList | HashSet, LinkedHashSet, TreeSet | HashMap, LinkedHashMap, TreeMap |

---

### Conclusion

The `List`, `Set`, and `Map` interfaces are fundamental parts of the Java Collections Framework. They provide a way to store and manipulate groups of objects with specific behaviors and characteristics. By understanding these interfaces and their implementations, you can choose the right data structure for your needs in Java programming.

---
---
---

### ArrayList, LinkedList, HashSet, TreeSet, HashMap, LinkedHashMap, and TreeMap in Java

The Java Collections Framework includes various classes that implement the core collection interfaces like `List`, `Set`, and `Map`. Each of these classes has its own characteristics and use cases. Below is a detailed explanation of each of these classes, including their features, implementations, and examples.

---

## 1. **ArrayList**

### **Description**
- `ArrayList` is a resizable array implementation of the `List` interface. It allows for dynamic arrays that can grow as needed.

### **Key Features**
- **Dynamic Size**: Automatically resizes itself as elements are added or removed.
- **Indexed Access**: Provides fast random access to elements using an index.
- **Allows Duplicates**: Can store duplicate elements.
  
### **Performance**
- **Access Time**: Constant time for accessing elements (O(1)).
- **Insertion/Deletion Time**: Linear time (O(n)) in the worst case, as elements may need to be shifted.

### **Example**
```java
import java.util.ArrayList;

public class ArrayListExample {
    public static void main(String[] args) {
        ArrayList<String> names = new ArrayList<>();
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");
        
        System.out.println("ArrayList: " + names);
        names.remove("Bob");
        System.out.println("After removal: " + names);
    }
}
```

#### **Output:**
```
ArrayList: [Alice, Bob, Charlie]
After removal: [Alice, Charlie]
```

---

## 2. **LinkedList**

### **Description**
- `LinkedList` is a doubly linked list implementation of the `List` and `Deque` interfaces. It provides better performance when adding or removing elements compared to `ArrayList`.

### **Key Features**
- **Dynamic Size**: Grows and shrinks dynamically.
- **Node-Based Structure**: Each element (node) contains references to the next and previous nodes.
- **Allows Duplicates**: Can store duplicate elements.

### **Performance**
- **Access Time**: Linear time (O(n)) to access elements by index.
- **Insertion/Deletion Time**: Constant time (O(1)) for adding/removing elements at the beginning or end.

### **Example**
```java
import java.util.LinkedList;

public class LinkedListExample {
    public static void main(String[] args) {
        LinkedList<String> fruits = new LinkedList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.addFirst("Mango");
        
        System.out.println("LinkedList: " + fruits);
        fruits.removeLast();
        System.out.println("After removal: " + fruits);
    }
}
```

#### **Output:**
```
LinkedList: [Mango, Apple, Banana]
After removal: [Mango, Apple]
```

---

## 3. **HashSet**

### **Description**
- `HashSet` is a collection that implements the `Set` interface using a hash table. It does not allow duplicate elements and does not maintain any order.

### **Key Features**
- **No Duplicates**: Each element must be unique.
- **Unordered**: Does not maintain any specific order of elements.
- **Performance**: Offers constant time performance for basic operations (add, remove, contains).

### **Example**
```java
import java.util.HashSet;

public class HashSetExample {
    public static void main(String[] args) {
        HashSet<String> colors = new HashSet<>();
        colors.add("Red");
        colors.add("Green");
        colors.add("Blue");
        colors.add("Red"); // Duplicate will be ignored

        System.out.println("HashSet: " + colors);
    }
}
```

#### **Output:**
```
HashSet: [Red, Green, Blue]
```

---

## 4. **TreeSet**

### **Description**
- `TreeSet` is a collection that implements the `Set` interface using a red-black tree. It maintains a sorted order of elements.

### **Key Features**
- **No Duplicates**: Each element must be unique.
- **Sorted Order**: Automatically sorts elements in their natural order or by a specified comparator.
- **Performance**: Offers log(n) time cost for basic operations (add, remove, contains).

### **Example**
```java
import java.util.TreeSet;

public class TreeSetExample {
    public static void main(String[] args) {
        TreeSet<Integer> numbers = new TreeSet<>();
        numbers.add(5);
        numbers.add(3);
        numbers.add(8);
        numbers.add(1); // Duplicates will be ignored

        System.out.println("TreeSet: " + numbers);
    }
}
```

#### **Output:**
```
TreeSet: [1, 3, 5, 8]
```

---

## 5. **HashMap**

### **Description**
- `HashMap` is a collection that implements the `Map` interface using a hash table. It allows key-value pairs and does not maintain any order.

### **Key Features**
- **Key-Value Pairs**: Each key is unique and maps to one value.
- **No Specific Order**: The order of elements is not guaranteed.
- **Performance**: Offers constant time performance for basic operations (put, get, remove).

### **Example**
```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        HashMap<String, Integer> scores = new HashMap<>();
        scores.put("Alice", 90);
        scores.put("Bob", 85);
        scores.put("Charlie", 95);

        System.out.println("HashMap: " + scores);
        System.out.println("Bob's Score: " + scores.get("Bob"));
    }
}
```

#### **Output:**
```
HashMap: {Alice=90, Bob=85, Charlie=95}
Bob's Score: 85
```

---

## 6. **LinkedHashMap**

### **Description**
- `LinkedHashMap` is a collection that combines the features of `HashMap` and `LinkedList`. It maintains a linked list of entries to preserve the order of insertion.

### **Key Features**
- **Key-Value Pairs**: Each key is unique and maps to one value.
- **Insertion Order**: Maintains the order of elements based on insertion.
- **Performance**: Offers constant time performance for basic operations.

### **Example**
```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> employeeIds = new LinkedHashMap<>();
        employeeIds.put("Alice", 1001);
        employeeIds.put("Bob", 1002);
        employeeIds.put("Charlie", 1003);

        System.out.println("LinkedHashMap: " + employeeIds);
    }
}
```

#### **Output:**
```
LinkedHashMap: {Alice=1001, Bob=1002, Charlie=1003}
```

---

## 7. **TreeMap**

### **Description**
- `TreeMap` is a collection that implements the `NavigableMap` interface using a red-black tree. It maintains a sorted order of keys.

### **Key Features**
- **Key-Value Pairs**: Each key is unique and maps to one value.
- **Sorted Order**: Automatically sorts the keys based on their natural order or by a specified comparator.
- **Performance**: Offers log(n) time cost for basic operations.

### **Example**
```java
import java.util.TreeMap;

public class TreeMapExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> productPrices = new TreeMap<>();
        productPrices.put("Laptop", 1000);
        productPrices.put("Smartphone", 500);
        productPrices.put("Tablet", 300);

        System.out.println("TreeMap: " + productPrices);
    }
}
```

#### **Output:**
```
TreeMap: {Laptop=1000, Smartphone=500, Tablet=300}
```

---

### Summary of Characteristics

| Class               | Type          | Allows Duplicates | Order Maintained | Key-Value Pairs | Time Complexity (Basic Operations) |
|---------------------|---------------|--------------------|------------------|------------------|-------------------------------------|
| `ArrayList`         | List          | Yes                | Insertion order   | No                | O(1) (get), O(n) (add/remove)      |
| `LinkedList`        | List          | Yes                | Insertion order   | No                | O(1) (add/remove), O(n) (get)      |
| `HashSet`           | Set           | No                 | No specific order | No                | O(1) (add/remove/contains)         |
| `TreeSet`           | Set           | No                 | Sorted order      | No                | O(log n) (add/remove/contains)     |
| `HashMap`           | Map           | No (for keys)      | No specific order | Yes               | O(1) (put/get/remove)              |
| `LinkedHashMap`     | Map           | No (for keys)      | Insertion order    | Yes               | O(1) (put/get/remove)              |
| `TreeMap`           | Map           | No (for keys)      | Sorted order      | Yes               | O(log n) (put/get/remove)          |

---

### Conclusion

Each of these classes has its own unique properties, making them suitable for

---
---
---

### Iterator and ListIterator in Java

The Java Collections Framework provides `Iterator` and `ListIterator` interfaces to traverse through collections like lists and sets. These iterators are designed to provide a way to access elements sequentially without exposing the underlying structure of the collection.

---

## 1. **Iterator**

### **Description**
- The `Iterator` interface is used to iterate over a collection (such as `Collection`, `Set`, or `List`) in a forward direction. It provides methods to check if there are more elements and to access those elements.

### **Key Features**
- **Unidirectional**: It can only traverse the collection in one direction (forward).
- **Remove Support**: Allows removing elements from the collection during iteration.

### **Methods**
- `boolean hasNext()`: Returns `true` if there are more elements to iterate.
- `E next()`: Returns the next element in the iteration.
- `void remove()`: Removes the last element returned by the iterator.

### **Example**
```java
import java.util.ArrayList;
import java.util.Iterator;

public class IteratorExample {
    public static void main(String[] args) {
        ArrayList<String> names = new ArrayList<>();
        names.add("Alice");
        names.add("Bob");
        names.add("Charlie");

        Iterator<String> iterator = names.iterator();
        
        while (iterator.hasNext()) {
            String name = iterator.next();
            System.out.println("Name: " + name);
            if (name.equals("Bob")) {
                iterator.remove(); // Removing Bob from the list
            }
        }
        
        System.out.println("After removal: " + names);
    }
}
```

#### **Output:**
```
Name: Alice
Name: Bob
Name: Charlie
After removal: [Alice, Charlie]
```

---

## 2. **ListIterator**

### **Description**
- The `ListIterator` interface is a subinterface of `Iterator` and is specifically designed for lists. It allows bidirectional traversal of the list and provides additional methods for modifying the list.

### **Key Features**
- **Bidirectional**: Can traverse the list in both forward and backward directions.
- **Modify List**: Supports operations to add, remove, and replace elements in the list.

### **Methods**
- `boolean hasNext()`: Returns `true` if there are more elements when traversing forward.
- `boolean hasPrevious()`: Returns `true` if there are more elements when traversing backward.
- `E next()`: Returns the next element in the iteration.
- `E previous()`: Returns the previous element in the iteration.
- `int nextIndex()`: Returns the index of the element that would be returned by the next call to `next()`.
- `int previousIndex()`: Returns the index of the element that would be returned by the previous call to `previous()`.
- `void add(E e)`: Inserts the specified element into the list.
- `void set(E e)`: Replaces the last element returned by the iterator with the specified element.
- `void remove()`: Removes the last element returned by the iterator.

### **Example**
```java
import java.util.ArrayList;
import java.util.ListIterator;

public class ListIteratorExample {
    public static void main(String[] args) {
        ArrayList<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");

        ListIterator<String> listIterator = fruits.listIterator();
        
        System.out.println("Traversing forward:");
        while (listIterator.hasNext()) {
            String fruit = listIterator.next();
            System.out.println("Fruit: " + fruit);
            if (fruit.equals("Banana")) {
                listIterator.set("Blueberry"); // Replacing Banana with Blueberry
            }
        }

        System.out.println("After forward traversal: " + fruits);
        
        System.out.println("Traversing backward:");
        while (listIterator.hasPrevious()) {
            String fruit = listIterator.previous();
            System.out.println("Fruit: " + fruit);
        }
    }
}
```

#### **Output:**
```
Traversing forward:
Fruit: Apple
Fruit: Banana
Fruit: Cherry
After forward traversal: [Apple, Blueberry, Cherry]
Traversing backward:
Fruit: Cherry
Fruit: Blueberry
Fruit: Apple
```

---

### Summary of Differences

| Feature                   | Iterator                | ListIterator            |
|---------------------------|-------------------------|--------------------------|
| Direction                  | Unidirectional (forward) | Bidirectional (forward and backward) |
| Applicable Collections      | `Collection`, `Set`, `List` | `List`                   |
| Additional Methods         | None                    | `hasPrevious()`, `previous()`, `add()`, `set()` |
| Modifying the Collection   | Yes (via `remove()`)   | Yes (via `add()`, `set()`, `remove()`) |

---

### Conclusion

Both `Iterator` and `ListIterator` provide convenient ways to traverse collections. `Iterator` is suitable for general collections, while `ListIterator` offers more capabilities specifically for lists, allowing for more flexible manipulation of list elements.

---
---
---

### Comparable and Comparator in Java

In Java, `Comparable` and `Comparator` are two interfaces that are used to define the order of objects. They provide a way to sort objects based on specified criteria. Understanding the differences and use cases for these interfaces is essential for effective object sorting and comparison.

---

## 1. **Comparable Interface**

### **Description**
- The `Comparable` interface is used to define the natural ordering of objects of a class. A class that implements the `Comparable` interface must define the `compareTo()` method, which compares the current object with another object of the same class.

### **Key Features**
- **Single Sorting Logic**: The class itself defines how its objects should be sorted.
- **Default Sorting**: If a class implements `Comparable`, it can be sorted using methods like `Collections.sort()` or `Arrays.sort()` without any additional logic.

### **Methods**
- `int compareTo(T o)`: Compares the current object with the specified object for order.

### **Example**
```java
import java.util.ArrayList;
import java.util.Collections;

class Student implements Comparable<Student> {
    String name;
    int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public int compareTo(Student other) {
        return this.age - other.age; // Sorting by age in ascending order
    }

    @Override
    public String toString() {
        return name + " (" + age + ")";
    }
}

public class ComparableExample {
    public static void main(String[] args) {
        ArrayList<Student> students = new ArrayList<>();
        students.add(new Student("Alice", 22));
        students.add(new Student("Bob", 20));
        students.add(new Student("Charlie", 21));

        Collections.sort(students); // Sorts students based on age
        System.out.println("Students sorted by age: " + students);
    }
}
```

#### **Output:**
```
Students sorted by age: [Bob (20), Charlie (21), Alice (22)]
```

---

## 2. **Comparator Interface**

### **Description**
- The `Comparator` interface is used to define an external comparison logic for objects of a class. This is useful when you want to sort objects in multiple ways or when you do not have control over the class definition (i.e., you cannot modify the class to implement `Comparable`).

### **Key Features**
- **Multiple Sorting Criteria**: Allows different comparison methods to be defined externally without modifying the class.
- **Flexibility**: You can create multiple comparators for the same class.

### **Methods**
- `int compare(T o1, T o2)`: Compares two objects for order.
- `boolean equals(Object obj)`: (Optional) Indicates whether some other object is "equal to" this comparator.

### **Example**
```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.Comparator;

class Student {
    String name;
    int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return name + " (" + age + ")";
    }
}

class AgeComparator implements Comparator<Student> {
    @Override
    public int compare(Student s1, Student s2) {
        return s1.age - s2.age; // Sorting by age in ascending order
    }
}

class NameComparator implements Comparator<Student> {
    @Override
    public int compare(Student s1, Student s2) {
        return s1.name.compareTo(s2.name); // Sorting by name in alphabetical order
    }
}

public class ComparatorExample {
    public static void main(String[] args) {
        ArrayList<Student> students = new ArrayList<>();
        students.add(new Student("Alice", 22));
        students.add(new Student("Bob", 20));
        students.add(new Student("Charlie", 21));

        Collections.sort(students, new AgeComparator()); // Sorts by age
        System.out.println("Students sorted by age: " + students);

        Collections.sort(students, new NameComparator()); // Sorts by name
        System.out.println("Students sorted by name: " + students);
    }
}
```

#### **Output:**
```
Students sorted by age: [Bob (20), Charlie (21), Alice (22)]
Students sorted by name: [Alice (22), Bob (20), Charlie (21)]
```

---

### Summary of Differences

| Feature                   | Comparable                         | Comparator                             |
|---------------------------|------------------------------------|----------------------------------------|
| Definition                 | Natural ordering of objects        | Custom ordering logic                  |
| Implementation Location     | Inside the class                   | External to the class                  |
| Method                      | `compareTo()`                     | `compare()`                            |
| Use Case                   | Single sorting logic               | Multiple sorting criteria              |
| Flexibility                | Less flexible                      | More flexible                          |

---

### Conclusion

- **`Comparable`** is used for defining a default sort order for a class. It is more straightforward and is typically used when there is a single, logical way to sort the objects.
- **`Comparator`** provides a way to define multiple sorting mechanisms externally, allowing for greater flexibility when sorting objects. This is particularly useful when sorting objects of classes that you cannot modify or when different sorting orders are needed for the same class.

---
---
---

# 5. Multithreading and Concurrency

### Thread Lifecycle in Java

In Java, a thread is an independent path of execution in a program. Understanding the thread lifecycle is essential for effectively managing threads and ensuring that your application performs optimally. A thread goes through various states from its creation to its termination. These states are defined in the Java Thread API.

---

### Thread States

The lifecycle of a thread can be categorized into the following states:

1. **New (Born)**
2. **Runnable (Ready)**
3. **Blocked**
4. **Waiting**
5. **Timed Waiting**
6. **Terminated (Dead)**

---

### 1. **New (Born) State**
- **Description**: When a thread is created using the `Thread` class or implementing the `Runnable` interface, it enters the New state. In this state, the thread is not yet running.
- **Transition**: The thread transitions to the Runnable state when the `start()` method is invoked.

### Example
```java
Thread thread = new Thread(new MyRunnable()); // New state
```

---

### 2. **Runnable (Ready) State**
- **Description**: In this state, the thread is ready to run and waiting for CPU time to execute. A thread can be in this state even when it is not executing, as the operating system can decide to run another thread.
- **Transition**: The thread moves to the Running state when the CPU scheduler allocates CPU time to it.

---

### 3. **Running State**
- **Description**: When a thread is executing its task, it is in the Running state. The thread's run method is being executed at this point.
- **Transition**: The thread can move back to the Runnable state if the thread scheduler preempts it or if it yields control. It can also go to Blocked, Waiting, or Terminated states based on different conditions.

---

### 4. **Blocked State**
- **Description**: A thread enters the Blocked state when it is waiting to acquire a lock for an object that another thread holds. This state occurs primarily when the thread tries to access synchronized resources.
- **Transition**: Once the thread acquires the lock, it returns to the Runnable state.

### Example
```java
synchronized (object) {
    // Blocked if another thread holds the lock on 'object'
}
```

---

### 5. **Waiting State**
- **Description**: A thread enters the Waiting state when it is waiting indefinitely for another thread to perform a particular action (like notify or notifyAll). This can happen when a thread calls methods like `Object.wait()`, `Thread.join()`, or `LockSupport.park()`.
- **Transition**: The thread moves back to the Runnable state when it is notified or interrupted.

### Example
```java
synchronized (object) {
    object.wait(); // Waiting indefinitely
}
```

---

### 6. **Timed Waiting State**
- **Description**: A thread enters the Timed Waiting state when it waits for another thread to perform an action for a specified waiting time. This occurs when a thread calls methods like `Thread.sleep(milliseconds)`, `Object.wait(milliseconds)`, or `Thread.join(milliseconds)`.
- **Transition**: The thread returns to the Runnable state either after the specified time elapses or when it is notified.

### Example
```java
Thread.sleep(1000); // Timed waiting for 1 second
```

---

### 7. **Terminated (Dead) State**
- **Description**: A thread enters the Terminated state when it has completed its execution (either normally or due to an exception). Once a thread is in this state, it cannot be restarted.
- **Transition**: A thread terminates when the `run()` method completes, either by returning normally or throwing an uncaught exception.

### Example
```java
public void run() {
    // Thread logic
    // Automatically enters terminated state when this method completes
}
```

---

### Summary of Thread Lifecycle Transitions

- **New** → **Runnable**: When `start()` is called.
- **Runnable** → **Running**: When the thread scheduler allocates CPU time.
- **Running** → **Runnable**: When the thread is preempted, or it yields control.
- **Running** → **Blocked**: When waiting for a lock.
- **Running** → **Waiting**: When `wait()`, `join()`, or `LockSupport.park()` is called.
- **Running** → **Timed Waiting**: When `sleep()`, `wait(milliseconds)`, or `join(milliseconds)` is called.
- **Waiting/Blocked** → **Runnable**: When notified, interrupted, or the lock is acquired.
- **Running** → **Terminated**: When the `run()` method completes.

---

### Visual Representation

Here's a simple visual representation of the thread lifecycle:

```
New
  |
  v
Runnable <-------------------
  |                        |  |
  v                        |  |
Running  ------------------>  |
  |                        |  |
  |                        |  |
  v                        v  v
Blocked <----> Waiting <----> Timed Waiting
  |                        |
  |                        |
  v                        v
Terminated
```

---

### Conclusion

Understanding the thread lifecycle in Java is crucial for effective multithreading. It helps developers manage thread behavior, optimize performance, and avoid common pitfalls like deadlocks and resource contention. By knowing how threads transition between states, you can create more robust and efficient applications.

---
---
---

### Creating Threads in Java

In Java, threads can be created in two primary ways: by extending the `Thread` class or by implementing the `Runnable` interface. Both approaches have their own advantages, and understanding these methods is essential for effective multithreading in Java applications.

---

## 1. **Creating Threads by Extending the Thread Class**

### **Description**
When you create a thread by extending the `Thread` class, you are creating a new class that inherits from `Thread`. You override the `run()` method to define the code that should be executed when the thread is started.

### **Key Steps**
1. Extend the `Thread` class.
2. Override the `run()` method with the code to be executed.
3. Create an instance of the new class.
4. Call the `start()` method to initiate the thread.

### **Example**
```java
class MyThread extends Thread {
    @Override
    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Thread " + Thread.currentThread().getName() + " - Count: " + i);
            try {
                Thread.sleep(500); // Sleep for 500 milliseconds
            } catch (InterruptedException e) {
                System.out.println("Thread interrupted");
            }
        }
    }
}

public class ThreadExample {
    public static void main(String[] args) {
        MyThread thread1 = new MyThread(); // Create a new thread
        MyThread thread2 = new MyThread(); // Create another thread

        thread1.start(); // Start thread1
        thread2.start(); // Start thread2
    }
}
```

#### **Output:**
```
Thread Thread-0 - Count: 1
Thread Thread-1 - Count: 1
Thread Thread-0 - Count: 2
Thread Thread-1 - Count: 2
...
```

---

## 2. **Creating Threads by Implementing the Runnable Interface**

### **Description**
When you create a thread by implementing the `Runnable` interface, you define a separate class that implements `Runnable`. This approach is preferred when your class already extends another class since Java does not support multiple inheritance.

### **Key Steps**
1. Implement the `Runnable` interface.
2. Override the `run()` method with the code to be executed.
3. Create an instance of the `Thread` class, passing the `Runnable` instance to its constructor.
4. Call the `start()` method on the `Thread` instance to initiate the thread.

### **Example**
```java
class MyRunnable implements Runnable {
    @Override
    public void run() {
        for (int i = 1; i <= 5; i++) {
            System.out.println("Runnable " + Thread.currentThread().getName() + " - Count: " + i);
            try {
                Thread.sleep(500); // Sleep for 500 milliseconds
            } catch (InterruptedException e) {
                System.out.println("Thread interrupted");
            }
        }
    }
}

public class RunnableExample {
    public static void main(String[] args) {
        MyRunnable myRunnable = new MyRunnable(); // Create an instance of the runnable
        Thread thread1 = new Thread(myRunnable); // Create a new thread with the runnable
        Thread thread2 = new Thread(myRunnable); // Create another thread with the same runnable

        thread1.start(); // Start thread1
        thread2.start(); // Start thread2
    }
}
```

#### **Output:**
```
Runnable Thread-0 - Count: 1
Runnable Thread-1 - Count: 1
Runnable Thread-0 - Count: 2
Runnable Thread-1 - Count: 2
...
```

---

### Comparison of Both Approaches

| Feature                         | Extending `Thread` Class          | Implementing `Runnable` Interface   |
|---------------------------------|-----------------------------------|-------------------------------------|
| Inheritance                     | Can't inherit from another class   | Can inherit from another class      |
| Flexibility                     | Less flexible due to single inheritance | More flexible, can implement multiple interfaces |
| Thread Management               | Thread management is in the thread class | Thread management is handled in the `Runnable` class |
| Resource Sharing                | Difficult to share resources      | Easier to share resources among multiple threads |

---

### Conclusion

Creating threads in Java can be done through two primary approaches: extending the `Thread` class or implementing the `Runnable` interface. The choice between these methods depends on your specific use case, such as class inheritance and resource sharing requirements. Understanding both approaches allows developers to design efficient multithreaded applications tailored to their needs.

---
---
---


### Synchronization in Java

Synchronization is a fundamental concept in Java multithreading that ensures that shared resources are accessed by only one thread at a time. It is essential to prevent data inconsistency and ensure thread safety when multiple threads attempt to read or write shared data simultaneously.

---

## Key Concepts of Synchronization

1. **Shared Resources**: These are variables or objects that multiple threads access and modify. Without proper synchronization, these resources can lead to inconsistent states or data corruption.

2. **Critical Section**: This is a block of code that accesses shared resources. Only one thread can execute the critical section at any given time to ensure data integrity.

3. **Locking Mechanism**: Java uses locks to manage access to shared resources. When a thread enters a synchronized block or method, it acquires a lock for that object, preventing other threads from entering the synchronized section until the lock is released.

---

## Types of Synchronization

1. **Method-level Synchronization**
2. **Block-level Synchronization**
3. **Static Synchronization**

### 1. **Method-level Synchronization**

In method-level synchronization, a method is declared as `synchronized`. This means that only one thread can execute that method on a given object at a time.

#### **Example**
```java
class Counter {
    private int count = 0;

    // Synchronized method
    public synchronized void increment() {
        count++;
    }

    public int getCount() {
        return count;
    }
}

public class SyncMethodExample {
    public static void main(String[] args) {
        Counter counter = new Counter();

        // Create multiple threads
        Thread thread1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread thread2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        // Start threads
        thread1.start();
        thread2.start();

        // Wait for threads to finish
        try {
            thread1.join();
            thread2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        // Display the count
        System.out.println("Final Count: " + counter.getCount());
    }
}
```

#### **Output**
```
Final Count: 2000
```

---

### 2. **Block-level Synchronization**

Block-level synchronization allows you to synchronize a specific block of code instead of the entire method. This is useful when you want to minimize the synchronized code area to reduce contention among threads.

#### **Example**
```java
class Counter {
    private int count = 0;

    public void increment() {
        // Synchronized block
        synchronized (this) {
            count++;
        }
    }

    public int getCount() {
        return count;
    }
}

public class SyncBlockExample {
    public static void main(String[] args) {
        Counter counter = new Counter();

        // Create multiple threads
        Thread thread1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread thread2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        // Start threads
        thread1.start();
        thread2.start();

        // Wait for threads to finish
        try {
            thread1.join();
            thread2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        // Display the count
        System.out.println("Final Count: " + counter.getCount());
    }
}
```

#### **Output**
```
Final Count: 2000
```

---

### 3. **Static Synchronization**

Static synchronization is applied to static methods. When a static synchronized method is invoked, the lock is acquired on the class object instead of the instance object.

#### **Example**
```java
class Counter {
    private static int count = 0;

    // Synchronized static method
    public static synchronized void increment() {
        count++;
    }

    public static int getCount() {
        return count;
    }
}

public class SyncStaticExample {
    public static void main(String[] args) {
        // Create multiple threads
        Thread thread1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                Counter.increment();
            }
        });

        Thread thread2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                Counter.increment();
            }
        });

        // Start threads
        thread1.start();
        thread2.start();

        // Wait for threads to finish
        try {
            thread1.join();
            thread2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        // Display the count
        System.out.println("Final Count: " + Counter.getCount());
    }
}
```

#### **Output**
```
Final Count: 2000
```

---

## Conclusion

Synchronization in Java is essential for managing access to shared resources in a multithreaded environment. It prevents data inconsistency and ensures thread safety by allowing only one thread to execute a synchronized method or block at a time. Proper synchronization techniques—method-level, block-level, and static synchronization—help developers build robust and reliable applications that handle concurrent operations effectively.

---
---
---

### Executor Framework in Java

The Executor Framework is a part of the `java.util.concurrent` package introduced in Java 5. It provides a high-level mechanism for managing and controlling thread execution, allowing developers to easily work with concurrent programming without directly handling thread creation and management. The framework separates task submission from the mechanics of how each task will be run.

---

## Key Components of the Executor Framework

1. **Executor Interface**
2. **ExecutorService Interface**
3. **ThreadPoolExecutor Class**
4. **ScheduledExecutorService Interface**
5. **Callable and Future**

---

### 1. **Executor Interface**

The `Executor` interface is the simplest interface in the Executor Framework. It defines a single method, `execute()`, which accepts a `Runnable` task.

#### **Example**
```java
import java.util.concurrent.Executor;

public class SimpleExecutorExample {
    public static void main(String[] args) {
        Executor executor = new java.util.concurrent.Executor() {
            @Override
            public void execute(Runnable command) {
                new Thread(command).start(); // Execute the task in a new thread
            }
        };

        executor.execute(() -> System.out.println("Task executed by: " + Thread.currentThread().getName()));
    }
}
```

---

### 2. **ExecutorService Interface**

The `ExecutorService` interface extends the `Executor` interface and provides methods to manage the lifecycle of tasks and the thread pool. It includes methods for submitting tasks, shutting down the service, and more.

#### **Key Methods:**
- `submit()`: Accepts a `Callable` or `Runnable` and returns a `Future`.
- `shutdown()`: Initiates an orderly shutdown in which previously submitted tasks are executed, but no new tasks will be accepted.
- `shutdownNow()`: Attempts to stop all actively executing tasks and halts the processing of waiting tasks.

#### **Example**
```java
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;

public class ExecutorServiceExample {
    public static void main(String[] args) {
        ExecutorService executorService = Executors.newFixedThreadPool(2); // Create a thread pool with 2 threads

        for (int i = 0; i < 5; i++) {
            final int taskId = i;
            executorService.submit(() -> {
                System.out.println("Task " + taskId + " is executed by " + Thread.currentThread().getName());
            });
        }

        executorService.shutdown(); // Shutdown the executor service
    }
}
```

#### **Output:**
```
Task 0 is executed by pool-1-thread-1
Task 1 is executed by pool-1-thread-2
Task 2 is executed by pool-1-thread-1
Task 3 is executed by pool-1-thread-2
Task 4 is executed by pool-1-thread-1
```

---

### 3. **ThreadPoolExecutor Class**

`ThreadPoolExecutor` is a flexible and powerful implementation of the `ExecutorService` interface. It allows you to customize the thread pool, including the number of threads, the queue used for holding tasks, and more.

#### **Key Parameters:**
- **corePoolSize**: The number of threads to keep in the pool, even if they are idle.
- **maximumPoolSize**: The maximum number of threads allowed in the pool.
- **keepAliveTime**: The time for which idle threads will wait for new tasks before terminating.
- **workQueue**: The queue used to hold tasks before they are executed.

#### **Example**
```java
import java.util.concurrent.LinkedBlockingQueue;
import java.util.concurrent.ThreadPoolExecutor;
import java.util.concurrent.TimeUnit;

public class ThreadPoolExecutorExample {
    public static void main(String[] args) {
        ThreadPoolExecutor executor = new ThreadPoolExecutor(
                2, // corePoolSize
                4, // maximumPoolSize
                60, // keepAliveTime
                TimeUnit.SECONDS, // time unit for keepAliveTime
                new LinkedBlockingQueue<>()); // work queue

        for (int i = 0; i < 10; i++) {
            final int taskId = i;
            executor.execute(() -> {
                System.out.println("Task " + taskId + " is executed by " + Thread.currentThread().getName());
            });
        }

        executor.shutdown(); // Shutdown the executor
    }
}
```

---

### 4. **ScheduledExecutorService Interface**

The `ScheduledExecutorService` interface extends `ExecutorService` and provides methods to schedule tasks to run after a given delay or periodically.

#### **Key Methods:**
- `schedule()`: Schedules a task to be executed after a specified delay.
- `scheduleAtFixedRate()`: Schedules a task to be executed repeatedly at fixed intervals.
- `scheduleWithFixedDelay()`: Schedules a task to be executed with a fixed delay between the end of one execution and the start of the next.

#### **Example**
```java
import java.util.concurrent.Executors;
import java.util.concurrent.ScheduledExecutorService;
import java.util.concurrent.TimeUnit;

public class ScheduledExecutorServiceExample {
    public static void main(String[] args) {
        ScheduledExecutorService scheduler = Executors.newScheduledThreadPool(1);

        scheduler.scheduleAtFixedRate(() -> {
            System.out.println("Task executed at: " + System.currentTimeMillis());
        }, 0, 2, TimeUnit.SECONDS); // Initial delay of 0 seconds, repeat every 2 seconds

        // To stop the scheduler after some time (for demonstration purposes)
        try {
            Thread.sleep(10000); // Let it run for 10 seconds
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        scheduler.shutdown(); // Shutdown the scheduler
    }
}
```

---

### 5. **Callable and Future**

- **Callable**: Similar to `Runnable`, but it can return a result and can throw checked exceptions. It is typically used with `ExecutorService` to submit tasks.

- **Future**: Represents the result of an asynchronous computation. You can use it to retrieve the result of a task or check if it is complete.

#### **Example**
```java
import java.util.concurrent.Callable;
import java.util.concurrent.ExecutionException;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
import java.util.concurrent.Future;

public class CallableFutureExample {
    public static void main(String[] args) {
        ExecutorService executor = Executors.newFixedThreadPool(1);

        Callable<Integer> task = () -> {
            Thread.sleep(2000); // Simulate a long-running task
            return 123; // Return some result
        };

        Future<Integer> future = executor.submit(task); // Submit the callable task

        try {
            Integer result = future.get(); // Get the result (blocking call)
            System.out.println("Task result: " + result);
        } catch (InterruptedException | ExecutionException e) {
            e.printStackTrace();
        } finally {
            executor.shutdown(); // Shutdown the executor
        }
    }
}
```

#### **Output**
```
Task result: 123
```

---

## Conclusion

The Executor Framework in Java provides a robust and flexible approach to managing threads and executing tasks asynchronously. By abstracting thread management and providing various interfaces and classes, it simplifies the development of concurrent applications, allowing developers to focus on defining tasks rather than handling thread lifecycle and synchronization details. Understanding how to leverage the Executor Framework effectively is essential for building high-performance, scalable Java applications.

---
---
---

### Concurrency Utilities in Java

Java provides several high-level concurrency utilities in the `java.util.concurrent` package to help manage complex threading and synchronization tasks. Three commonly used utilities are `CountDownLatch`, `Semaphore`, and `CyclicBarrier`. Each serves a specific purpose in coordinating thread execution.

---

## 1. CountDownLatch

`CountDownLatch` is a synchronization aid that allows one or more threads to wait until a set of operations being performed in other threads completes. It maintains a count that is decremented each time a thread calls the `countDown()` method. Once the count reaches zero, all waiting threads are released.

### Key Methods
- **Constructor**: `CountDownLatch(int count)`: Initializes the latch with a given count.
- **countDown()**: Decrements the count.
- **await()**: Causes the current thread to wait until the count reaches zero.

### Example
```java
import java.util.concurrent.CountDownLatch;

public class CountDownLatchExample {
    public static void main(String[] args) throws InterruptedException {
        int numWorkers = 3;
        CountDownLatch latch = new CountDownLatch(numWorkers);

        for (int i = 0; i < numWorkers; i++) {
            final int workerId = i;
            new Thread(() -> {
                try {
                    // Simulating some work
                    Thread.sleep(1000);
                    System.out.println("Worker " + workerId + " has completed work.");
                } catch (InterruptedException e) {
                    e.printStackTrace();
                } finally {
                    latch.countDown(); // Decrement the count
                }
            }).start();
        }

        latch.await(); // Wait until count reaches zero
        System.out.println("All workers have completed their tasks.");
    }
}
```

### Output
```
Worker 0 has completed work.
Worker 1 has completed work.
Worker 2 has completed work.
All workers have completed their tasks.
```

---

## 2. Semaphore

`Semaphore` is a counting semaphore that can be used to control access to a shared resource by multiple threads. It maintains a set number of permits; threads can acquire a permit before accessing the resource and release it afterward. If no permits are available, the requesting thread will block until a permit is released.

### Key Methods
- **acquire()**: Decrements the count of available permits, blocking if none are available.
- **release()**: Increments the count of available permits.

### Example
```java
import java.util.concurrent.Semaphore;

public class SemaphoreExample {
    public static void main(String[] args) {
        Semaphore semaphore = new Semaphore(2); // Two permits available

        for (int i = 0; i < 5; i++) {
            final int threadId = i;
            new Thread(() -> {
                try {
                    semaphore.acquire(); // Acquire a permit
                    System.out.println("Thread " + threadId + " is using the resource.");
                    Thread.sleep(2000); // Simulating resource usage
                } catch (InterruptedException e) {
                    e.printStackTrace();
                } finally {
                    System.out.println("Thread " + threadId + " has released the resource.");
                    semaphore.release(); // Release the permit
                }
            }).start();
        }
    }
}
```

### Output
```
Thread 0 is using the resource.
Thread 1 is using the resource.
Thread 2 has released the resource.
Thread 0 has released the resource.
Thread 3 is using the resource.
Thread 4 is using the resource.
```

---

## 3. CyclicBarrier

`CyclicBarrier` is a synchronization aid that allows a set of threads to all wait for each other to reach a common barrier point. Once all threads have reached the barrier, they can continue execution. It is called "cyclic" because it can be reused after the waiting threads are released.

### Key Methods
- **await()**: Causes the current thread to wait until all parties have invoked await().
- **Constructor**: `CyclicBarrier(int parties)`: Initializes with a specified number of parties that must invoke await().

### Example
```java
import java.util.concurrent.CyclicBarrier;

public class CyclicBarrierExample {
    public static void main(String[] args) {
        int numThreads = 3;
        CyclicBarrier barrier = new CyclicBarrier(numThreads, () -> {
            System.out.println("All threads have reached the barrier, proceeding...");
        });

        for (int i = 0; i < numThreads; i++) {
            final int threadId = i;
            new Thread(() -> {
                try {
                    Thread.sleep(1000 * (threadId + 1)); // Simulating work
                    System.out.println("Thread " + threadId + " has reached the barrier.");
                    barrier.await(); // Wait at the barrier
                } catch (Exception e) {
                    e.printStackTrace();
                }
            }).start();
        }
    }
}
```

### Output
```
Thread 0 has reached the barrier.
Thread 1 has reached the barrier.
Thread 2 has reached the barrier.
All threads have reached the barrier, proceeding...
```

---

## Conclusion

The concurrency utilities `CountDownLatch`, `Semaphore`, and `CyclicBarrier` provide powerful mechanisms for coordinating multiple threads in Java. They help manage complex thread interactions, improve application performance, and ensure thread safety. Understanding these utilities is essential for effective concurrent programming in Java.

---
---
---

### Concurrency Issues in Java

In concurrent programming, two common issues that developers face are **Deadlock** and **Race Conditions**. Understanding these issues is crucial for writing safe and efficient multi-threaded applications.

---

## 1. Deadlock

**Deadlock** occurs when two or more threads are blocked forever, each waiting on the other to release a resource. This situation can happen in a multi-threaded environment when the following conditions are met:

1. **Mutual Exclusion**: At least one resource is held in a non-shareable mode.
2. **Hold and Wait**: A thread holding at least one resource is waiting to acquire additional resources.
3. **No Preemption**: Resources cannot be forcibly taken from a thread holding them.
4. **Circular Wait**: There exists a set of threads where each thread is waiting for a resource held by the next thread in the set.

### Example of Deadlock
Here's a simple example illustrating a deadlock situation:

```java
class Resource {
    public synchronized void methodA(Resource other) {
        System.out.println(Thread.currentThread().getName() + " is in methodA");
        try {
            Thread.sleep(100);
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        other.methodB(); // Calling method of another resource
    }

    public synchronized void methodB() {
        System.out.println(Thread.currentThread().getName() + " is in methodB");
    }
}

public class DeadlockExample {
    public static void main(String[] args) {
        final Resource resource1 = new Resource();
        final Resource resource2 = new Resource();

        Thread thread1 = new Thread(() -> resource1.methodA(resource2), "Thread 1");
        Thread thread2 = new Thread(() -> resource2.methodA(resource1), "Thread 2");

        thread1.start();
        thread2.start();
    }
}
```

### Output
```
Thread 1 is in methodA
Thread 2 is in methodA
```

In this example, `Thread 1` holds a lock on `resource1` and is trying to access `resource2`, while `Thread 2` holds a lock on `resource2` and is trying to access `resource1`. This creates a deadlock where neither thread can proceed.

### Preventing Deadlock
To prevent deadlocks, consider the following strategies:
- **Avoid Nested Locks**: Try to avoid acquiring multiple locks at once.
- **Lock Ordering**: Always acquire locks in a consistent global order.
- **Use Timeout**: Implement a timeout mechanism to avoid indefinite waiting.
- **Deadlock Detection**: Use algorithms to detect and resolve deadlocks if they occur.

---

## 2. Race Conditions

A **Race Condition** occurs when two or more threads access shared data and try to change it at the same time. If the threads do not use proper synchronization techniques, the final outcome depends on the timing of the threads' execution, which can lead to inconsistent or erroneous results.

### Example of Race Condition
Here’s an example demonstrating a race condition:

```java
class Counter {
    private int count = 0;

    public void increment() {
        count++; // Non-atomic operation
    }

    public int getCount() {
        return count;
    }
}

public class RaceConditionExample {
    public static void main(String[] args) {
        Counter counter = new Counter();
        Thread thread1 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        Thread thread2 = new Thread(() -> {
            for (int i = 0; i < 1000; i++) {
                counter.increment();
            }
        });

        thread1.start();
        thread2.start();

        try {
            thread1.join();
            thread2.join();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }

        // The expected output is 2000, but due to race condition, it may be less
        System.out.println("Final Count: " + counter.getCount());
    }
}
```

### Output
```
Final Count: 1987
```

In this example, both `thread1` and `thread2` increment the shared `count` variable without any synchronization. Due to the race condition, the final count can be less than the expected value (2000) because multiple threads may read and write the `count` variable simultaneously.

### Preventing Race Conditions
To prevent race conditions, consider the following techniques:
- **Synchronization**: Use synchronized blocks or methods to control access to shared resources.
- **Atomic Variables**: Use classes from the `java.util.concurrent.atomic` package, like `AtomicInteger`, which provide atomic operations.
- **Locks**: Use explicit locks from the `java.util.concurrent.locks` package for more granular control over synchronization.

### Example Using Synchronization
Here's how you can modify the `Counter` class to use synchronization:

```java
class Counter {
    private int count = 0;

    public synchronized void increment() {
        count++; // Synchronized to prevent race condition
    }

    public int getCount() {
        return count;
    }
}
```

---

## Conclusion

Understanding and managing deadlocks and race conditions is crucial for developing robust and reliable multi-threaded applications in Java. Implementing proper synchronization techniques can help you avoid these concurrency issues, leading to more predictable and stable software.

---
---
---

# 6. Java I/O

### File Handling in Java

File handling in Java allows you to create, read, write, and manipulate files stored on the file system. Java provides several classes for handling files and performing input/output operations, including `FileReader`, `FileWriter`, `BufferedReader`, and `BufferedWriter`. Below is an overview of each class along with examples.

---

## 1. FileReader

`FileReader` is a class used for reading character files. It makes it possible to read the contents of a file as a stream of characters.

### Key Features
- Reads data in character format.
- Suitable for reading text files.

### Example
```java
import java.io.FileReader;
import java.io.IOException;

public class FileReaderExample {
    public static void main(String[] args) {
        try (FileReader fileReader = new FileReader("example.txt")) {
            int character;
            while ((character = fileReader.read()) != -1) {
                System.out.print((char) character); // Print each character
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
```
Contents of example.txt
```

---

## 2. FileWriter

`FileWriter` is used for writing character files. It allows you to write data to a file in character format.

### Key Features
- Writes data in character format.
- If the file already exists, it can overwrite the existing data or append to it based on the constructor used.

### Example
```java
import java.io.FileWriter;
import java.io.IOException;

public class FileWriterExample {
    public static void main(String[] args) {
        try (FileWriter fileWriter = new FileWriter("output.txt")) {
            fileWriter.write("Hello, World!\n");
            fileWriter.write("Writing to a file using FileWriter.");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
The file `output.txt` will contain:
```
Hello, World!
Writing to a file using FileWriter.
```

---

## 3. BufferedReader

`BufferedReader` is a class used for reading text from a character input stream efficiently. It reads large chunks of data at once, improving performance when reading files.

### Key Features
- Buffered input for faster reading.
- Allows reading lines of text using `readLine()`.

### Example
```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class BufferedReaderExample {
    public static void main(String[] args) {
        try (BufferedReader bufferedReader = new BufferedReader(new FileReader("example.txt"))) {
            String line;
            while ((line = bufferedReader.readLine()) != null) {
                System.out.println(line); // Print each line
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
```
First line of example.txt
Second line of example.txt
...
```

---

## 4. BufferedWriter

`BufferedWriter` is used for writing text to a character output stream efficiently. It buffers the output, which can enhance performance when writing files.

### Key Features
- Buffered output for faster writing.
- Allows writing strings and characters, and can write lines of text using `newLine()`.

### Example
```java
import java.io.BufferedWriter;
import java.io.FileWriter;
import java.io.IOException;

public class BufferedWriterExample {
    public static void main(String[] args) {
        try (BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter("outputBuffered.txt"))) {
            bufferedWriter.write("Hello, World!");
            bufferedWriter.newLine(); // New line
            bufferedWriter.write("Writing to a file using BufferedWriter.");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
The file `outputBuffered.txt` will contain:
```
Hello, World!
Writing to a file using BufferedWriter.
```

---

## Conclusion

File handling in Java is essential for managing data stored in files. The `FileReader` and `FileWriter` classes provide basic methods for reading and writing character files, while `BufferedReader` and `BufferedWriter` improve performance through buffering. These classes enable efficient file operations and form the basis for handling file I/O in Java applications.

---
---
---

### Byte Streams vs Character Streams in Java

In Java, input and output operations are divided into two categories: **Byte Streams** and **Character Streams**. Understanding the difference between these two types of streams is essential for efficiently reading and writing data.

---

## Byte Streams

**Byte Streams** are designed for handling binary data. They work with raw bytes and are used to read and write binary files, such as images, audio files, and other non-text files. Java provides the following main classes for byte stream operations:

### Key Features of Byte Streams
- Operate on raw binary data (8 bits).
- Suitable for all types of files, including text files (but text files will be read as binary).
- Use `InputStream` and `OutputStream` as their parent classes.

### Common Byte Stream Classes
- **FileInputStream**: To read bytes from a file.
- **FileOutputStream**: To write bytes to a file.

### Example of Byte Streams
```java
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class ByteStreamExample {
    public static void main(String[] args) {
        // Writing to a file using FileOutputStream
        try (FileOutputStream fos = new FileOutputStream("output.dat")) {
            fos.write(65); // Writes the byte for 'A'
            fos.write(66); // Writes the byte for 'B'
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Reading from a file using FileInputStream
        try (FileInputStream fis = new FileInputStream("output.dat")) {
            int byteRead;
            while ((byteRead = fis.read()) != -1) {
                System.out.print((char) byteRead); // Convert byte to character
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
```
AB
```

---

## Character Streams

**Character Streams** are designed for handling character data (text). They work with 16-bit Unicode characters and are specifically designed for reading and writing text files. Java provides the following main classes for character stream operations:

### Key Features of Character Streams
- Operate on characters (16 bits), which allows them to handle international text.
- Automatically handle character encoding and decoding.
- Use `Reader` and `Writer` as their parent classes.

### Common Character Stream Classes
- **FileReader**: To read characters from a file.
- **FileWriter**: To write characters to a file.

### Example of Character Streams
```java
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;

public class CharacterStreamExample {
    public static void main(String[] args) {
        // Writing to a file using FileWriter
        try (FileWriter writer = new FileWriter("output.txt")) {
            writer.write("Hello, World!");
        } catch (IOException e) {
            e.printStackTrace();
        }

        // Reading from a file using FileReader
        try (FileReader reader = new FileReader("output.txt")) {
            int character;
            while ((character = reader.read()) != -1) {
                System.out.print((char) character); // Print each character
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
```
Hello, World!
```

---

## Comparison of Byte Streams and Character Streams

| Feature               | Byte Streams                     | Character Streams                |
|-----------------------|----------------------------------|----------------------------------|
| Data Type             | Operate on raw bytes (8 bits)    | Operate on characters (16 bits)   |
| Encoding               | No encoding; suitable for binary files | Automatically handle character encoding |
| Classes                | Use `InputStream` and `OutputStream` | Use `Reader` and `Writer`         |
| Common Classes         | `FileInputStream`, `FileOutputStream` | `FileReader`, `FileWriter`        |
| Usage                  | Used for all file types (binary and text) | Used primarily for text files     |
| Performance            | Generally faster for binary data | More overhead due to encoding/decoding |

---

## Conclusion

In summary, **byte streams** are suited for binary data and can handle all types of files, while **character streams** are specifically designed for text data and automatically manage character encoding. Choosing the appropriate stream type is crucial for efficient file operations in Java.

---
---
---


### Serialization and Deserialization in Java

Serialization and deserialization are processes that allow Java objects to be converted into a byte stream for storage or transmission and then reconstructed back into their original form. This is particularly useful for saving the state of an object, sending objects over a network, or storing objects in a file.

---

## Serialization

**Serialization** is the process of converting an object into a byte stream. This byte stream can then be saved to a file, sent over a network, or stored in memory. Serialization allows you to persist the state of an object so that it can be recreated later.

### Key Features of Serialization
- Converts objects into a byte stream.
- Enables object persistence (saving the state).
- Can be used for communication between different components in distributed applications.

### How to Serialize an Object
To make a Java object serializable, the class must implement the `Serializable` interface, which is a marker interface (it does not contain any methods). Here's how you can serialize an object:

### Example of Serialization
```java
import java.io.FileOutputStream;
import java.io.IOException;
import java.io.ObjectOutputStream;
import java.io.Serializable;

// Class to be serialized
class Student implements Serializable {
    private String name;
    private int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}

public class SerializationExample {
    public static void main(String[] args) {
        Student student = new Student("Alice", 22);

        // Serialize the student object
        try (FileOutputStream fileOutputStream = new FileOutputStream("student.ser");
             ObjectOutputStream objectOutputStream = new ObjectOutputStream(fileOutputStream)) {
            objectOutputStream.writeObject(student);
            System.out.println("Serialization successful: " + student);
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
```
Serialization successful: Student{name='Alice', age=22}
```

---

## Deserialization

**Deserialization** is the process of converting a byte stream back into a Java object. This is the reverse operation of serialization, allowing you to recreate the original object and its state.

### Key Features of Deserialization
- Converts a byte stream back into an object.
- Restores the state of the object from the serialized data.
- Allows for object retrieval from files, network connections, etc.

### How to Deserialize an Object
To deserialize an object, you need to use the `ObjectInputStream` class. Here's how you can deserialize an object:

### Example of Deserialization
```java
import java.io.FileInputStream;
import java.io.IOException;
import java.io.ObjectInputStream;

public class DeserializationExample {
    public static void main(String[] args) {
        Student student = null;

        // Deserialize the student object
        try (FileInputStream fileInputStream = new FileInputStream("student.ser");
             ObjectInputStream objectInputStream = new ObjectInputStream(fileInputStream)) {
            student = (Student) objectInputStream.readObject();
            System.out.println("Deserialization successful: " + student);
        } catch (IOException | ClassNotFoundException e) {
            e.printStackTrace();
        }
    }
}
```

### Output
```
Deserialization successful: Student{name='Alice', age=22}
```

---

## Important Considerations

- **serialVersionUID**: It is a good practice to declare a `serialVersionUID` field in your serializable class. This ID helps in version control of the serialized class and is used during deserialization to ensure that a loaded class corresponds to a serialized object.

    ```java
    private static final long serialVersionUID = 1L;
    ```

- **Transient Keyword**: If you want to skip serialization for a specific field (e.g., sensitive data), you can declare that field as `transient`. This means it won't be serialized and will be initialized to its default value during deserialization.

    ```java
    private transient String password;
    ```

---

## Conclusion

Serialization and deserialization in Java provide a powerful mechanism for converting objects to a byte stream and vice versa. This capability is crucial for saving object states, network communication, and storing objects in files. Understanding how to implement serialization and deserialization allows you to efficiently manage object persistence in your applications.

---
---
---

# 7 Java 8 Features

### Lambda Expressions in Java

Lambda expressions are a feature introduced in Java 8 that allow you to create anonymous functions (or implementations of functional interfaces) in a more concise and expressive manner. They enable you to treat functionality as a method argument or to create a more streamlined way of writing code, especially when working with collections and streams.

---

## Key Features of Lambda Expressions

1. **Concise Syntax**: Lambda expressions reduce the verbosity of anonymous class implementations.
2. **Functional Programming**: They support a functional programming style, making code easier to read and maintain.
3. **Targeting Functional Interfaces**: Lambda expressions can be used wherever a functional interface is expected (an interface with a single abstract method).

### Syntax of Lambda Expressions

The general syntax of a lambda expression is as follows:

```
(parameters) -> expression
```

or

```
(parameters) -> { statements; }
```

### Example of a Lambda Expression

1. **Without Parameters**: If the functional interface does not require parameters, you can omit them.

```java
Runnable runnable = () -> System.out.println("Hello, World!");
```

2. **With Parameters**: If the functional interface has parameters, define them in parentheses.

```java
// Using a functional interface with a single method
@FunctionalInterface
interface Greeting {
    void greet(String name);
}

// Implementing the functional interface with a lambda expression
Greeting greeting = (name) -> System.out.println("Hello, " + name + "!");
```

### Using Lambda Expressions with Collections

Lambda expressions are often used with Java's collection framework, especially with the `forEach`, `filter`, and `map` methods in the Stream API.

#### Example: Using Lambda with Collections
```java
import java.util.Arrays;
import java.util.List;

public class LambdaExample {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David");

        // Using a lambda expression to print each name
        names.forEach(name -> System.out.println(name));

        // Using a lambda expression to filter names that start with 'C'
        names.stream()
             .filter(name -> name.startsWith("C"))
             .forEach(name -> System.out.println("Filtered Name: " + name));
    }
}
```

### Output
```
Alice
Bob
Charlie
David
Filtered Name: Charlie
```

---

## Functional Interfaces

Functional interfaces are interfaces with a single abstract method. They can have multiple default or static methods but must have exactly one abstract method. You can use lambda expressions to provide implementations for functional interfaces.

### Common Functional Interfaces

Java 8 introduced several built-in functional interfaces in the `java.util.function` package, including:

- **Predicate<T>**: Represents a boolean-valued function (i.e., it takes an argument and returns a boolean).
- **Consumer<T>**: Represents an operation that takes a single argument and returns no result.
- **Supplier<T>**: Represents a supplier of results (no input).
- **Function<T, R>**: Represents a function that takes an argument and produces a result.
- **BinaryOperator<T>**: Represents an operation on two operands of the same type.

### Example of Built-in Functional Interfaces
```java
import java.util.function.Predicate;

public class FunctionalInterfaceExample {
    public static void main(String[] args) {
        // Using Predicate to check if a number is even
        Predicate<Integer> isEven = number -> number % 2 == 0;

        System.out.println(isEven.test(10)); // Output: true
        System.out.println(isEven.test(7));  // Output: false
    }
}
```

### Output
```
true
false
```

---

## Conclusion

Lambda expressions in Java provide a powerful and expressive way to implement functional programming concepts. They allow you to write cleaner and more concise code, especially when dealing with collections and functional interfaces. By reducing boilerplate code associated with anonymous classes, lambda expressions improve code readability and maintainability, making them an essential feature for modern Java development.

---
---
---

### Stream API in Java

The Stream API, introduced in Java 8, provides a powerful way to process sequences of elements (such as collections) in a functional style. It allows developers to express complex data processing queries concisely and efficiently, leveraging the benefits of functional programming.

---

## Key Features of Stream API

1. **Declarative Approach**: Stream API allows you to express computations in a high-level, declarative manner, making code more readable.
2. **Pipeline Processing**: Streams support a sequence of operations (transformations) that can be executed in a pipeline, enabling efficient data manipulation.
3. **Lazy Evaluation**: Intermediate operations on streams are lazy, meaning they are not executed until a terminal operation is invoked. This allows for optimization and reduced overhead.
4. **Parallel Processing**: Stream API allows easy parallel execution of operations on collections, improving performance on multi-core processors.

### Creating Streams

Streams can be created from various data sources, including collections, arrays, or I/O channels. Here are some common ways to create a stream:

1. **From a Collection**:
   ```java
   List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David");
   Stream<String> streamFromCollection = names.stream();
   ```

2. **From an Array**:
   ```java
   String[] nameArray = {"Alice", "Bob", "Charlie", "David"};
   Stream<String> streamFromArray = Arrays.stream(nameArray);
   ```

3. **Using Stream.of()**:
   ```java
   Stream<String> streamOf = Stream.of("Alice", "Bob", "Charlie", "David");
   ```

---

## Stream Operations

Stream operations are divided into two categories: **intermediate** and **terminal** operations.

### 1. Intermediate Operations

Intermediate operations return a new stream and can be chained together. They are lazy and do not execute until a terminal operation is invoked. Some common intermediate operations include:

- **`filter(Predicate<T> predicate)`**: Filters elements based on a predicate.
- **`map(Function<T, R> mapper)`**: Transforms each element to another form.
- **`sorted()`**: Sorts the elements of the stream.
- **`distinct()`**: Removes duplicate elements.

### Example of Intermediate Operations
```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class IntermediateOperationsExample {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David", "Alice");

        List<String> filteredNames = names.stream()
                .filter(name -> name.startsWith("A")) // Keep names starting with 'A'
                .distinct() // Remove duplicates
                .sorted() // Sort names
                .collect(Collectors.toList()); // Collect results into a list

        System.out.println(filteredNames); // Output: [Alice]
    }
}
```

### Output
```
[Alice]
```

---

### 2. Terminal Operations

Terminal operations produce a result or side-effect and terminate the stream processing. Some common terminal operations include:

- **`forEach(Consumer<T> action)`**: Performs an action for each element in the stream.
- **`collect(Collector<T, A, R> collector)`**: Collects elements into a collection or another type.
- **`count()`**: Counts the number of elements in the stream.
- **`reduce(BinaryOperator<T> accumulator)`**: Reduces the elements to a single value.

### Example of Terminal Operations
```java
import java.util.Arrays;
import java.util.List;

public class TerminalOperationsExample {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David");

        // Print each name
        names.stream()
             .forEach(name -> System.out.println(name));

        // Count the number of names
        long count = names.stream().count();
        System.out.println("Total Names: " + count); // Output: Total Names: 4
    }
}
```

### Output
```
Alice
Bob
Charlie
David
Total Names: 4
```

---

## Example: Stream API in Action

Here’s a comprehensive example that demonstrates the power of the Stream API with multiple operations.

```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class StreamApiExample {
    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5, 6, 7, 8, 9, 10);

        // Using Stream API to find the square of even numbers greater than 5
        List<Integer> result = numbers.stream()
                .filter(n -> n > 5) // Filter numbers greater than 5
                .filter(n -> n % 2 == 0) // Keep even numbers
                .map(n -> n * n) // Square the numbers
                .collect(Collectors.toList()); // Collect results into a list

        System.out.println("Squares of even numbers greater than 5: " + result);
    }
}
```

### Output
```
Squares of even numbers greater than 5: [64, 100]
```

---

## Conclusion

The Stream API provides a robust and flexible framework for working with sequences of data in Java. By embracing functional programming principles, it enables developers to write more expressive and concise code while efficiently processing data. Whether you're filtering, mapping, or aggregating collections, the Stream API simplifies complex operations, making data manipulation more straightforward and enjoyable.

---
---
---

### Optional Class in Java

The `Optional` class, introduced in Java 8, is a container object used to represent a value that may or may not be present. It is a way to avoid `NullPointerExceptions` by explicitly defining when a value is absent. The `Optional` class is part of the `java.util` package and provides methods to handle potential absence of values gracefully.

---

## Key Features of Optional

1. **Null Safety**: Optional helps to avoid null checks and reduces the chances of `NullPointerExceptions`.
2. **Functional Style**: It supports a functional programming style by providing methods that accept lambda expressions.
3. **Descriptive API**: The API is designed to be descriptive, making it clear when a value might be absent.

### Creating Optional Instances

You can create instances of the `Optional` class using several static methods:

1. **`Optional.empty()`**: Creates an empty Optional instance.
2. **`Optional.of(T value)`**: Creates an Optional containing the given non-null value. If the value is null, it throws a `NullPointerException`.
3. **`Optional.ofNullable(T value)`**: Creates an Optional that may or may not contain a value. It allows null values without throwing an exception.

### Example of Creating Optional Instances
```java
import java.util.Optional;

public class OptionalExample {
    public static void main(String[] args) {
        // Creating an empty Optional
        Optional<String> emptyOptional = Optional.empty();
        
        // Creating an Optional with a non-null value
        Optional<String> nonNullOptional = Optional.of("Hello, World!");
        
        // Creating an Optional that can be null
        Optional<String> nullableOptional = Optional.ofNullable(null);
        
        System.out.println("Empty Optional: " + emptyOptional);
        System.out.println("Non-null Optional: " + nonNullOptional);
        System.out.println("Nullable Optional: " + nullableOptional);
    }
}
```

### Output
```
Empty Optional: Optional.empty
Non-null Optional: Optional[Hello, World!]
Nullable Optional: Optional.empty
```

---

## Common Methods of Optional

The `Optional` class provides several useful methods for handling values. Here are some commonly used methods:

1. **`isPresent()`**: Returns true if a value is present; otherwise, false.
2. **`ifPresent(Consumer<? super T> action)`**: If a value is present, it performs the given action with the value.
3. **`get()`**: Returns the value if present; otherwise, throws `NoSuchElementException`.
4. **`orElse(T other)`**: Returns the value if present; otherwise, returns the provided default value.
5. **`orElseGet(Supplier<? extends T> other)`**: Returns the value if present; otherwise, invokes the provided supplier and returns the result.
6. **`orElseThrow(Supplier<? extends X> exceptionSupplier)`**: Returns the value if present; otherwise, throws an exception created by the provided supplier.

### Example of Using Optional Methods
```java
import java.util.Optional;

public class OptionalMethodsExample {
    public static void main(String[] args) {
        Optional<String> optionalValue = Optional.ofNullable("Java Optional");

        // Check if a value is present
        if (optionalValue.isPresent()) {
            System.out.println("Value is present: " + optionalValue.get());
        }

        // Using ifPresent to perform an action
        optionalValue.ifPresent(value -> System.out.println("Value: " + value));

        // Using orElse to provide a default value
        String defaultValue = optionalValue.orElse("Default Value");
        System.out.println("Value or default: " + defaultValue);

        // Using orElseGet with a supplier
        String generatedValue = optionalValue.orElseGet(() -> "Generated Value");
        System.out.println("Value or generated: " + generatedValue);

        // Using orElseThrow to throw an exception if value is absent
        try {
            Optional<String> emptyOptional = Optional.empty();
            System.out.println(emptyOptional.orElseThrow(() -> new Exception("No value present")));
        } catch (Exception e) {
            System.out.println("Exception: " + e.getMessage());
        }
    }
}
```

### Output
```
Value is present: Java Optional
Value: Java Optional
Value or default: Java Optional
Value or generated: Java Optional
Exception: No value present
```

---

## Conclusion

The `Optional` class in Java provides a clear and effective way to handle the absence of values without resorting to null references. By promoting a more functional programming style and offering a variety of methods for value handling, `Optional` helps improve code readability and safety. It encourages developers to think about the possibility of missing values and handle them explicitly, reducing the likelihood of runtime exceptions and improving overall code quality.

---
---
---

### Functional Interfaces in Java

A **Functional Interface** in Java is an interface that contains exactly one abstract method. They are used primarily in lambda expressions and method references. Java 8 introduced functional programming concepts, making it easier to work with such interfaces.

Functional interfaces are commonly used in the context of lambda expressions to represent behavior as data. The `java.util.function` package provides several standard functional interfaces, including `Predicate`, `Consumer`, `Supplier`, and `Function`.

---

## Key Functional Interfaces

### 1. **Predicate<T>**
The `Predicate` interface represents a single argument function that returns a boolean value. It is commonly used for conditional expressions.

- **Method**: 
  - `boolean test(T t)`: Evaluates this predicate on the given argument.
  
#### Example of Predicate
```java
import java.util.function.Predicate;

public class PredicateExample {
    public static void main(String[] args) {
        Predicate<Integer> isEven = num -> num % 2 == 0;

        System.out.println("Is 4 even? " + isEven.test(4)); // Output: true
        System.out.println("Is 5 even? " + isEven.test(5)); // Output: false
    }
}
```

### 2. **Consumer<T>**
The `Consumer` interface represents a single argument function that does not return any result. It is primarily used to perform operations on the given argument.

- **Method**: 
  - `void accept(T t)`: Performs the operation on the given argument.
  
#### Example of Consumer
```java
import java.util.function.Consumer;

public class ConsumerExample {
    public static void main(String[] args) {
        Consumer<String> print = str -> System.out.println(str);

        print.accept("Hello, Consumer!"); // Output: Hello, Consumer!
    }
}
```

### 3. **Supplier<T>**
The `Supplier` interface represents a supplier of results. It does not take any arguments and returns a result. It is often used for lazy evaluation or when you want to provide values on demand.

- **Method**: 
  - `T get()`: Gets a result.
  
#### Example of Supplier
```java
import java.util.function.Supplier;

public class SupplierExample {
    public static void main(String[] args) {
        Supplier<Double> randomValue = () -> Math.random();

        System.out.println("Random value: " + randomValue.get()); // Output: Random value: [some random number]
    }
}
```

### 4. **Function<T, R>**
The `Function` interface represents a function that takes one argument and produces a result. It is often used to transform data.

- **Method**: 
  - `R apply(T t)`: Applies this function to the given argument and returns the result.
  
#### Example of Function
```java
import java.util.function.Function;

public class FunctionExample {
    public static void main(String[] args) {
        Function<Integer, String> toString = num -> "Number: " + num;

        System.out.println(toString.apply(10)); // Output: Number: 10
    }
}
```

---

## Combining Functional Interfaces

Functional interfaces can be combined using default and static methods. For example, `Predicate` has methods like `and`, `or`, and `negate`, which allow you to compose multiple predicates.

### Example of Combining Predicates
```java
import java.util.function.Predicate;

public class CombinedPredicateExample {
    public static void main(String[] args) {
        Predicate<Integer> isEven = num -> num % 2 == 0;
        Predicate<Integer> isPositive = num -> num > 0;

        Predicate<Integer> isEvenAndPositive = isEven.and(isPositive);

        System.out.println("Is 4 even and positive? " + isEvenAndPositive.test(4)); // Output: true
        System.out.println("Is -4 even and positive? " + isEvenAndPositive.test(-4)); // Output: false
    }
}
```

---

## Conclusion

Functional interfaces play a crucial role in enabling functional programming in Java. They provide a way to represent behaviors as first-class citizens, allowing you to pass around behavior as parameters, return them from methods, and utilize lambda expressions effectively. Understanding `Predicate`, `Consumer`, `Supplier`, and `Function` is essential for leveraging the power of functional programming in Java, making your code more concise, readable, and expressive.

---
---
---

### Method References in Java

**Method References** are a shorthand notation of a lambda expression to call a method. They allow you to refer to methods without executing them, making your code more concise and readable. Method references are a feature introduced in Java 8, and they can be used wherever a functional interface is expected.

---

## Types of Method References

There are four main types of method references in Java:

1. **Reference to a Static Method**
2. **Reference to an Instance Method of a Particular Object**
3. **Reference to an Instance Method of an Arbitrary Object of a Particular Type**
4. **Reference to a Constructor**

### 1. Reference to a Static Method

You can reference a static method of a class. This type of method reference uses the class name followed by `::` and the method name.

#### Example
```java
import java.util.function.Function;

public class StaticMethodReferenceExample {
    public static void main(String[] args) {
        Function<String, Integer> stringLength = String::length;
        
        System.out.println("Length of 'Hello': " + stringLength.apply("Hello")); // Output: 5
    }
}
```

### 2. Reference to an Instance Method of a Particular Object

This type of method reference is used when you want to reference an instance method of a specific object.

#### Example
```java
import java.util.function.Consumer;

public class InstanceMethodReferenceExample {
    public static void main(String[] args) {
        String message = "Hello, World!";
        
        Consumer<String> printer = System.out::println;
        printer.accept(message); // Output: Hello, World!
    }
}
```

### 3. Reference to an Instance Method of an Arbitrary Object of a Particular Type

This type of method reference is used to refer to an instance method of an arbitrary object of a particular type. It is commonly used with collections.

#### Example
```java
import java.util.Arrays;
import java.util.List;

public class ArbitraryObjectMethodReferenceExample {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie");

        names.forEach(System.out::println); // Output: Alice, Bob, Charlie
    }
}
```

### 4. Reference to a Constructor

You can also use method references to refer to a constructor. This is useful for creating instances of a class.

#### Example
```java
import java.util.function.Supplier;

public class ConstructorReferenceExample {
    public static void main(String[] args) {
        Supplier<StringBuilder> stringBuilderSupplier = StringBuilder::new;

        StringBuilder sb = stringBuilderSupplier.get();
        sb.append("Hello, Constructor Reference!");
        
        System.out.println(sb.toString()); // Output: Hello, Constructor Reference!
    }
}
```

---

## Conclusion

Method references provide a clean and concise way to refer to methods in Java, making your code easier to read and maintain. They allow you to eliminate boilerplate code, particularly when working with functional interfaces. By understanding the different types of method references—static methods, instance methods, and constructor references—you can leverage this powerful feature to enhance your Java programming skills and embrace functional programming paradigms effectively.

---
---
---

### Default and Static Methods in Interfaces

Java 8 introduced **default** and **static methods** in interfaces to enhance the flexibility and capability of interfaces. These methods allow you to define behavior directly in interfaces, promoting code reuse and providing a way to evolve interfaces without breaking existing implementations.

---

## 1. Default Methods

**Default methods** are instance methods defined in interfaces with the `default` keyword. They can have a body, and any class that implements the interface inherits these methods. Default methods enable you to add new functionality to interfaces without affecting the classes that already implement them.

### Key Points:
- Default methods can be overridden in implementing classes.
- They are useful for providing a default implementation for new methods in interfaces.

### Example of Default Method
```java
interface Animal {
    void eat(); // Abstract method

    default void sleep() {
        System.out.println("Sleeping...");
    }
}

class Dog implements Animal {
    @Override
    public void eat() {
        System.out.println("Dog is eating.");
    }

    // Dog inherits the default implementation of sleep()
}

public class DefaultMethodExample {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.eat();    // Output: Dog is eating.
        dog.sleep();  // Output: Sleeping...
    }
}
```

### Overriding Default Method
```java
class Cat implements Animal {
    @Override
    public void eat() {
        System.out.println("Cat is eating.");
    }

    @Override
    public void sleep() {
        System.out.println("Cat is sleeping.");
    }
}

public class DefaultMethodOverrideExample {
    public static void main(String[] args) {
        Cat cat = new Cat();
        cat.eat();    // Output: Cat is eating.
        cat.sleep();  // Output: Cat is sleeping.
    }
}
```

---

## 2. Static Methods

**Static methods** in interfaces are defined with the `static` keyword and can be called without an instance of the interface. They can contain implementation logic that can be shared across all implementing classes. Static methods in interfaces are similar to static methods in classes.

### Key Points:
- Static methods cannot be overridden in implementing classes.
- They are used to provide utility or helper methods related to the interface.

### Example of Static Method
```java
interface MathUtils {
    static int add(int a, int b) {
        return a + b;
    }
}

public class StaticMethodExample {
    public static void main(String[] args) {
        int sum = MathUtils.add(5, 10); // Calling static method
        System.out.println("Sum: " + sum); // Output: Sum: 15
    }
}
```

### Example with Default and Static Methods
```java
interface Vehicle {
    default void start() {
        System.out.println("Vehicle starting...");
    }

    static void stop() {
        System.out.println("Vehicle stopped.");
    }
}

public class VehicleExample {
    public static void main(String[] args) {
        Vehicle vehicle = new Vehicle() {}; // Anonymous class implementing Vehicle
        vehicle.start(); // Output: Vehicle starting...
        
        Vehicle.stop(); // Calling static method directly from the interface
    }
}
```

---

## Conclusion

Default and static methods in interfaces significantly enhance the functionality and flexibility of Java interfaces. Default methods allow you to provide default implementations, making it easier to evolve interfaces while maintaining backward compatibility. Static methods enable you to define utility functions related to the interface without requiring an instance of the implementing class. Understanding these concepts is essential for modern Java programming and helps create cleaner, more maintainable code.


---
---
---

# 8. Generics

### Generic Classes in Java

**Generic classes** are a powerful feature in Java that allows you to define classes with type parameters. This means that you can create a class that can operate on objects of various types while providing compile-time type safety. Generics enable you to write more reusable and flexible code, avoiding the need for casting and improving type-checking at compile time.

---

## Benefits of Generics
1. **Type Safety**: By specifying a type parameter, you can ensure that only compatible types are used, preventing `ClassCastException` at runtime.
2. **Code Reusability**: You can create a single class that can handle different types without the need to create multiple versions of the same class.
3. **Elimination of Casts**: Generics allow you to avoid explicit casting when retrieving elements from collections or generic classes.

---

## Syntax of Generic Classes

To declare a generic class, you use angle brackets `<>` after the class name and specify a type parameter (e.g., `T`, `E`, etc.).

### Example of a Generic Class
```java
// Declaration of a generic class with type parameter T
public class GenericBox<T> {
    private T item;

    // Method to set the item
    public void setItem(T item) {
        this.item = item;
    }

    // Method to get the item
    public T getItem() {
        return item;
    }
}

// Testing the GenericBox class
public class GenericClassExample {
    public static void main(String[] args) {
        // Creating a GenericBox for Integer
        GenericBox<Integer> integerBox = new GenericBox<>();
        integerBox.setItem(10);
        System.out.println("Integer Value: " + integerBox.getItem()); // Output: Integer Value: 10

        // Creating a GenericBox for String
        GenericBox<String> stringBox = new GenericBox<>();
        stringBox.setItem("Hello Generics");
        System.out.println("String Value: " + stringBox.getItem()); // Output: String Value: Hello Generics
    }
}
```

---

## Multiple Type Parameters

You can also define a generic class with multiple type parameters by separating them with commas.

### Example of a Generic Class with Multiple Type Parameters
```java
// Generic class with two type parameters
public class Pair<K, V> {
    private K key;
    private V value;

    public Pair(K key, V value) {
        this.key = key;
        this.value = value;
    }

    public K getKey() {
        return key;
    }

    public V getValue() {
        return value;
    }
}

// Testing the Pair class
public class PairExample {
    public static void main(String[] args) {
        Pair<String, Integer> pair = new Pair<>("One", 1);
        System.out.println("Key: " + pair.getKey() + ", Value: " + pair.getValue()); // Output: Key: One, Value: 1
    }
}
```

---

## Bounded Type Parameters

You can restrict the types that can be used as type arguments by using bounds. This is done using the `extends` keyword.

### Example of Bounded Type Parameters
```java
// Bounded generic class where T must extend Number
public class NumberBox<T extends Number> {
    private T number;

    public NumberBox(T number) {
        this.number = number;
    }

    public double doubleValue() {
        return number.doubleValue();
    }
}

// Testing the NumberBox class
public class BoundedTypeExample {
    public static void main(String[] args) {
        NumberBox<Integer> integerBox = new NumberBox<>(10);
        System.out.println("Double Value: " + integerBox.doubleValue()); // Output: Double Value: 10.0

        NumberBox<Double> doubleBox = new NumberBox<>(10.5);
        System.out.println("Double Value: " + doubleBox.doubleValue()); // Output: Double Value: 10.5
    }
}
```

---

## Conclusion

Generic classes are a fundamental feature in Java that allows you to write flexible and type-safe code. By defining classes with type parameters, you can create reusable components that work with different data types while maintaining compile-time type safety. Understanding generics is essential for modern Java programming, especially when working with collections and APIs that utilize generic types.

---
---
---

### Bounded Types in Java

**Bounded types** in Java generics allow you to restrict the types that can be used as type arguments for a generic class, interface, or method. By defining bounds, you can ensure that the type parameters meet certain criteria, which enhances type safety and allows you to invoke methods that are specific to the bounded types.

---

## Types of Bounded Types

There are two main types of bounded types in Java:

1. **Upper Bounded Types**
2. **Lower Bounded Types**

### 1. Upper Bounded Types

Upper bounded types restrict the type parameter to be a specific type or a subtype of that type. This is done using the `extends` keyword.

#### Syntax
```java
<T extends ClassName>
```

#### Example of Upper Bounded Types
In this example, we create a generic class `Box` that accepts only numbers (and their subclasses).

```java
// Upper bounded generic class
public class NumberBox<T extends Number> {
    private T number;

    public NumberBox(T number) {
        this.number = number;
    }

    public double getDoubleValue() {
        return number.doubleValue(); // Only Number has this method
    }
}

// Testing the NumberBox class
public class UpperBoundedExample {
    public static void main(String[] args) {
        NumberBox<Integer> integerBox = new NumberBox<>(10);
        System.out.println("Double Value: " + integerBox.getDoubleValue()); // Output: Double Value: 10.0

        NumberBox<Double> doubleBox = new NumberBox<>(10.5);
        System.out.println("Double Value: " + doubleBox.getDoubleValue()); // Output: Double Value: 10.5

        // This will cause a compile-time error since String is not a subclass of Number
        // NumberBox<String> stringBox = new NumberBox<>("Hello"); 
    }
}
```

### 2. Lower Bounded Types

Lower bounded types restrict the type parameter to be a specific type or a supertype of that type. This is done using the `super` keyword.

#### Syntax
```java
<T super ClassName>
```

#### Example of Lower Bounded Types
In this example, we create a method that accepts a list of objects that are of a specific type or its superclasses.

```java
import java.util.ArrayList;
import java.util.List;

// Method with lower bounded wildcard
public class LowerBoundedExample {
    public static void addNumbers(List<? super Integer> list) {
        for (int i = 1; i <= 5; i++) {
            list.add(i); // We can add integers since the lower bound is Integer or its superclasses
        }
    }

    public static void main(String[] args) {
        List<Number> numberList = new ArrayList<>();
        addNumbers(numberList); // Valid: List of Number is accepted
        System.out.println("List: " + numberList); // Output: List: [1, 2, 3, 4, 5]

        // This will cause a compile-time error since String is not a superclass of Integer
        // List<String> stringList = new ArrayList<>();
        // addNumbers(stringList);
    }
}
```

---

## Wildcards

In addition to bounded types, Java also supports wildcards that provide more flexibility in generics. The wildcard can be used with an upper or lower bound.

### Example of Wildcards
```java
public class WildcardExample {
    public static void printNumbers(List<? extends Number> list) {
        for (Number number : list) {
            System.out.println(number); // Can read numbers, but cannot add to the list
        }
    }

    public static void main(String[] args) {
        List<Integer> intList = List.of(1, 2, 3);
        printNumbers(intList); // Valid: List of Integer is accepted

        List<Double> doubleList = List.of(1.1, 2.2);
        printNumbers(doubleList); // Valid: List of Double is accepted
    }
}
```

---

## Conclusion

Bounded types in Java generics provide a mechanism to enforce type constraints on type parameters, ensuring type safety and flexibility. Upper bounded types allow you to specify that a type must be a specific class or subclass, while lower bounded types enable you to specify that a type must be a superclass. Understanding bounded types is crucial for effectively using generics and writing robust Java applications.

---
---
---

### Wildcards in Java Generics

**Wildcards** in Java generics provide a way to express an unknown type, allowing for more flexible and generic programming. Wildcards are particularly useful when you want to work with a family of types without specifying exact type parameters. They are denoted by the `?` symbol and can be used with bounded types.

---

## Types of Wildcards

There are three types of wildcards in Java:

1. **Unbounded Wildcards**
2. **Upper Bounded Wildcards**
3. **Lower Bounded Wildcards**

### 1. Unbounded Wildcards

An unbounded wildcard is represented by a question mark (`?`) and can accept any type. It is used when you want to allow any type as a parameter.

#### Example of Unbounded Wildcards
```java
import java.util.List;

// Method that accepts a list of any type
public class UnboundedWildcardExample {
    public static void printList(List<?> list) {
        for (Object obj : list) {
            System.out.println(obj); // Can read elements but cannot add
        }
    }

    public static void main(String[] args) {
        List<String> stringList = List.of("Java", "Python", "C++");
        printList(stringList); // Valid

        List<Integer> integerList = List.of(1, 2, 3);
        printList(integerList); // Valid
    }
}
```

### 2. Upper Bounded Wildcards

Upper bounded wildcards restrict the unknown type to be a specific type or a subtype of that type. They are declared using the `extends` keyword.

#### Syntax
```java
<? extends ClassName>
```

#### Example of Upper Bounded Wildcards
```java
import java.util.List;

// Method that accepts a list of Numbers or its subclasses
public class UpperBoundedWildcardExample {
    public static void printNumbers(List<? extends Number> list) {
        for (Number number : list) {
            System.out.println(number); // Can read numbers
        }
    }

    public static void main(String[] args) {
        List<Integer> intList = List.of(1, 2, 3);
        printNumbers(intList); // Valid: List of Integer is accepted

        List<Double> doubleList = List.of(1.1, 2.2);
        printNumbers(doubleList); // Valid: List of Double is accepted

        // This will cause a compile-time error since String is not a subclass of Number
        // List<String> stringList = List.of("Hello", "World");
        // printNumbers(stringList);
    }
}
```

### 3. Lower Bounded Wildcards

Lower bounded wildcards restrict the unknown type to be a specific type or a supertype of that type. They are declared using the `super` keyword.

#### Syntax
```java
<? super ClassName>
```

#### Example of Lower Bounded Wildcards
```java
import java.util.ArrayList;
import java.util.List;

// Method that accepts a list of Integers or its superclasses
public class LowerBoundedWildcardExample {
    public static void addNumbers(List<? super Integer> list) {
        for (int i = 1; i <= 5; i++) {
            list.add(i); // Can add integers
        }
    }

    public static void main(String[] args) {
        List<Number> numberList = new ArrayList<>();
        addNumbers(numberList); // Valid: List of Number is accepted
        System.out.println("List: " + numberList); // Output: List: [1, 2, 3, 4, 5]

        // This will cause a compile-time error since String is not a superclass of Integer
        // List<String> stringList = new ArrayList<>();
        // addNumbers(stringList);
    }
}
```

---

## Summary of Wildcards

- **Unbounded Wildcards**: Use `?` to accept any type. Useful for reading elements without the need to add.
  
- **Upper Bounded Wildcards**: Use `? extends ClassName` to restrict the type to `ClassName` or its subclasses. Useful when you want to read objects that belong to a certain type hierarchy.

- **Lower Bounded Wildcards**: Use `? super ClassName` to restrict the type to `ClassName` or its superclasses. Useful when you want to add objects to a collection.

---

## Conclusion

Wildcards in Java generics provide a flexible way to work with different types while maintaining type safety. Understanding how to use wildcards effectively can enhance your ability to write generic methods and classes, allowing for more reusable and adaptable code in Java.

---
---
---

# 9. Java Memory Management

### Stack vs Heap Memory in Java

In Java, memory management is an essential aspect of application development, and it is primarily divided into two areas: **Stack Memory** and **Heap Memory**. Each of these memory areas serves a different purpose and has distinct characteristics.

---

## Stack Memory

**Stack memory** is used for storing local variables and method call information. It follows the Last In, First Out (LIFO) principle, meaning that the last method called is the first one to be completed.

### Characteristics of Stack Memory

1. **Storage**: Stores primitive data types (int, char, etc.) and object references, but not the objects themselves.
2. **Lifetime**: The memory for local variables is allocated when a method is called and deallocated when the method completes. Therefore, the lifetime of variables is limited to the method scope.
3. **Size**: Generally smaller in size compared to heap memory. The size of the stack is fixed, and you may encounter a `StackOverflowError` if the stack memory limit is exceeded (usually due to deep or infinite recursion).
4. **Access Speed**: Accessing stack memory is faster than heap memory due to its structured and fixed nature.
5. **Memory Management**: Managed automatically by the Java Virtual Machine (JVM) through method calls.

### Example of Stack Memory
```java
public class StackMemoryExample {
    public static void main(String[] args) {
        int localVariable = 10; // Stored in stack memory
        System.out.println("Local Variable: " + localVariable);
        methodA(); // Calling methodA
    }

    public static void methodA() {
        int methodVariable = 20; // Stored in stack memory
        System.out.println("Method Variable: " + methodVariable);
    }
}
```

---

## Heap Memory

**Heap memory** is used for dynamic memory allocation and is where all objects (instances of classes) are stored. It is shared among all threads in a Java application.

### Characteristics of Heap Memory

1. **Storage**: Stores all objects and their instance variables. Unlike stack memory, heap memory stores actual object data.
2. **Lifetime**: Objects in heap memory have a longer lifespan than stack variables. They exist until there are no more references to them, allowing for the possibility of garbage collection to reclaim unused memory.
3. **Size**: Generally larger than stack memory. The size of heap memory can be adjusted through JVM parameters.
4. **Access Speed**: Accessing heap memory is slower than accessing stack memory because it is less structured and can involve more complex memory management.
5. **Memory Management**: Managed by the Java Garbage Collector, which automatically reclaims memory used by objects that are no longer reachable.

### Example of Heap Memory
```java
class Student {
    String name;

    public Student(String name) {
        this.name = name; // 'name' is stored in heap memory
    }
}

public class HeapMemoryExample {
    public static void main(String[] args) {
        Student student = new Student("Alice"); // 'student' reference is in stack, object is in heap
        System.out.println("Student Name: " + student.name);
    }
}
```

---

## Summary of Differences

| Feature           | Stack Memory                                   | Heap Memory                             |
|-------------------|------------------------------------------------|----------------------------------------|
| Storage           | Local variables and method call information    | Objects and their instance variables   |
| Lifetime          | Limited to method scope                         | Longer lifespan until garbage collected|
| Size              | Smaller, fixed size                            | Larger, adjustable size                |
| Access Speed      | Faster access due to LIFO structure            | Slower access due to dynamic allocation|
| Management        | Automatically managed by JVM                   | Managed by the Garbage Collector       |

---

## Conclusion

Understanding the differences between stack and heap memory is crucial for Java developers. It helps in optimizing memory usage, debugging issues related to memory, and improving application performance. Stack memory is best for short-lived, method-scoped variables, while heap memory is suitable for dynamically created objects that need to exist beyond the method execution.

---
---
---

### Garbage Collection in Java

**Garbage Collection (GC)** in Java is the process by which the Java Virtual Machine (JVM) automatically identifies and reclaims memory that is no longer in use. This ensures that memory is efficiently managed and prevents memory leaks by removing unused objects from the heap.

Java uses a built-in garbage collector that runs in the background, making Java applications less prone to memory management errors compared to languages like C or C++ where manual memory management is required.

---

## How Garbage Collection Works

In Java, objects are created on the **heap memory**, and when an object is no longer needed (i.e., there are no references to it), it becomes eligible for garbage collection. The JVM keeps track of object references, and once an object is unreachable, the garbage collector will reclaim the memory.

### Key Points:

- **Automatic Process**: Developers don't need to explicitly free memory as the garbage collector handles it automatically.
- **No Manual Memory Management**: Unlike languages like C/C++, Java abstracts the complexities of memory management.
- **Reachability**: Objects that are unreachable from the root references (like local variables, static variables, and active threads) are eligible for garbage collection.
- **Finalization**: Before the object is garbage collected, the JVM invokes the `finalize()` method (if it exists) on the object for any cleanup.

---

## Phases of Garbage Collection

### 1. **Mark Phase**:
   The garbage collector identifies which objects are still in use and which are not. It starts from **GC roots** (local variables, static fields, etc.) and traces all references to objects. Unreachable objects are marked for deletion.

### 2. **Sweep Phase**:
   After marking unreachable objects, the collector reclaims the memory allocated to them. This is the "clean-up" phase where memory is freed for future object allocation.

### 3. **Compaction (Optional)**:
   In some garbage collection algorithms, memory is compacted after sweeping to reduce fragmentation. Compacting moves objects closer together in memory, allowing for faster allocation of new objects.

---

## Types of Garbage Collectors in Java

Java offers several types of garbage collectors, each designed with different trade-offs in mind. They can be selected using JVM options.

### 1. **Serial Garbage Collector**
   - **Suitable for**: Single-threaded environments and small applications.
   - **Algorithm**: Uses a single thread for both marking and sweeping, which can pause application execution.
   - **JVM Option**: `-XX:+UseSerialGC`

### 2. **Parallel Garbage Collector (Throughput Collector)**
   - **Suitable for**: Applications requiring high throughput and running on multi-core processors.
   - **Algorithm**: Uses multiple threads for marking and sweeping, reducing pause time by working in parallel.
   - **JVM Option**: `-XX:+UseParallelGC`

### 3. **Concurrent Mark-Sweep (CMS) Garbage Collector**
   - **Suitable for**: Applications requiring low pause times.
   - **Algorithm**: Performs most of the marking concurrently with the application to reduce pause times.
   - **JVM Option**: `-XX:+UseConcMarkSweepGC`
   - **Note**: Deprecated in newer Java versions.

### 4. **G1 (Garbage First) Garbage Collector**
   - **Suitable for**: Applications that require predictable pause times and operate on large heaps.
   - **Algorithm**: Divides the heap into regions and collects garbage in phases to avoid full garbage collections.
   - **JVM Option**: `-XX:+UseG1GC`
   - **Note**: Default garbage collector in Java 9 and later.

---

## Code Example: Making Objects Eligible for Garbage Collection

Here’s an example showing how an object becomes eligible for garbage collection when there are no references to it:

```java
public class GarbageCollectionExample {
    public static void main(String[] args) {
        // Creating an object of class Person
        Person person1 = new Person("John");
        
        // Nullifying the reference, making person1 eligible for garbage collection
        person1 = null;

        // Requesting garbage collection
        System.gc();
    }
}

class Person {
    String name;

    Person(String name) {
        this.name = name;
    }

    // finalize method is called before the object is destroyed
    @Override
    protected void finalize() throws Throwable {
        System.out.println("Object is garbage collected");
    }
}
```

In this example:
- The `person1` reference initially points to an object of the `Person` class.
- When `person1` is set to `null`, the object becomes unreachable and is eligible for garbage collection.
- The `System.gc()` method is a request to the JVM to perform garbage collection (though it doesn’t guarantee immediate action).
- Before the object is destroyed, the `finalize()` method is called, though it is rarely used in practice and is considered deprecated in Java 9 and later.

---

## Best Practices and Considerations

1. **Avoid Finalization**: The `finalize()` method is unreliable and has been deprecated since Java 9. Use other resource management techniques like `try-with-resources`.
2. **Object Pooling**: Use object pools (like the `String Pool`) to reuse objects and reduce the need for frequent garbage collection.
3. **Minimize Object Creation**: Reduce unnecessary object creation to avoid frequent GC activity.
4. **Select Appropriate GC**: Depending on your application's performance needs, you can select a garbage collector that balances throughput and pause time.

---

## Summary

- **Garbage Collection**: Automatically manages memory in Java by identifying and removing unused objects.
- **Types of Collectors**: Java offers several garbage collectors (Serial, Parallel, CMS, G1) for different application requirements.
- **Eligible Objects**: An object becomes eligible for GC when there are no more references to it.
- **Manual Trigger**: While you can request GC via `System.gc()`, the JVM decides when to run it.

Garbage collection simplifies memory management for developers, making Java less prone to memory leaks and manual memory allocation issues. Understanding how GC works helps optimize application performance, especially for large-scale, memory-intensive applications.

---
---
---

### JVM, JDK, and JRE in Java

These three terms are fundamental to understanding how Java applications are developed, compiled, and run.

---

### 1. **JVM (Java Virtual Machine)**

The **Java Virtual Machine (JVM)** is an abstract computing machine that enables Java applications to run on any device or operating system (making Java platform-independent). The JVM interprets compiled Java bytecode and translates it to machine-level instructions, allowing the code to be executed.

#### Key Features:
- **Platform-Independent Execution**: The JVM allows Java code to be "write once, run anywhere" by providing an abstraction layer between Java bytecode and the underlying operating system and hardware.
- **Memory Management**: The JVM handles memory allocation and deallocation through garbage collection.
- **Execution of Bytecode**: After the Java source code is compiled into bytecode by the compiler, the JVM executes the bytecode line by line.

#### JVM Workflow:
1. **Compilation**: Java source code is compiled into **bytecode** (a low-level representation of the code that the JVM can understand).
2. **Class Loader**: The JVM’s class loader loads the `.class` files (compiled bytecode) into memory.
3. **Execution**: The **Interpreter** and **JIT (Just-in-Time) compiler** in the JVM interpret and optimize the bytecode into native machine code for execution.

#### Example:

```bash
# Compile the Java file into bytecode
javac HelloWorld.java

# Run the bytecode using JVM
java HelloWorld
```

---

### 2. **JDK (Java Development Kit)**

The **Java Development Kit (JDK)** is a software development environment used for developing Java applications. It provides all the tools required to write, compile, and run Java code.

#### Components of JDK:
- **JRE (Java Runtime Environment)**: The JDK includes the JRE, which contains the JVM and libraries needed to run Java applications.
- **Java Compiler (javac)**: The compiler is responsible for converting Java source code into bytecode.
- **Development Tools**: It includes tools like `javac` (compiler), `javadoc` (documentation generator), `jarsigner` (for signing .jar files), and more for developing Java applications.
  
The JDK is essential for developers as it provides everything needed to build Java programs.

#### Example:
```bash
# Compile Java program using the JDK's javac compiler
javac HelloWorld.java
```

---

### 3. **JRE (Java Runtime Environment)**

The **Java Runtime Environment (JRE)** provides the necessary environment to run Java applications. It includes the JVM, core libraries, and other components necessary to execute Java programs.

#### Components of JRE:
- **JVM**: The Java Virtual Machine is part of the JRE, which is responsible for running Java bytecode.
- **Core Libraries**: The JRE contains the class libraries (Java API) required by Java programs at runtime, such as classes for file input/output, networking, data structures, etc.
- **Other Runtime Components**: It includes components like a loader, interpreter, and garbage collector.

**Note**: The JRE is typically used by end-users who need to run Java applications, but do not need development tools like the compiler (`javac`).

#### Example:

If you're running a Java application:
```bash
java HelloWorld
```

The JRE provides the JVM and libraries necessary to execute the `HelloWorld` program.

---

### Relationship Between JVM, JDK, and JRE:

- **JVM**: Core component that runs the Java bytecode.
- **JRE**: Provides the JVM and libraries needed to run Java programs.
- **JDK**: Provides the JRE and additional tools required for Java development (such as the compiler and debugger).

---

### Diagram of JVM, JRE, and JDK:
```
JDK
└── JRE
    └── JVM
```
- **JDK**: Includes JRE and development tools like the compiler.
- **JRE**: Includes the JVM and libraries required to run Java programs.
- **JVM**: The engine that executes Java bytecode.

---

### Code Compilation and Execution Flow:

1. **Java Source Code** (`HelloWorld.java`)
   - Written by the developer.

2. **Java Compiler** (`javac HelloWorld.java`)
   - Compiles the source code into **bytecode** (`HelloWorld.class`).

3. **JVM Execution** (`java HelloWorld`)
   - The JVM executes the bytecode in the `.class` file and runs the program.

---

### Example Code and Execution:

```java
// Simple Java Program
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

**Steps to Compile and Run:**
1. Save the above code in a file named `HelloWorld.java`.
2. Compile it using the JDK's `javac` tool:
   ```bash
   javac HelloWorld.java
   ```
   This generates a `HelloWorld.class` file containing the bytecode.

3. Run the program using the `java` command (which invokes the JVM):
   ```bash
   java HelloWorld
   ```
   Output:
   ```
   Hello, World!
   ```

---

### Summary:

- **JVM**: Executes Java bytecode and provides platform independence.
- **JRE**: Provides the environment (JVM + libraries) to run Java applications.
- **JDK**: Contains the JRE along with tools needed for Java development (compiler, debugger, etc.).

Together, the JVM, JRE, and JDK form the backbone of Java development and execution. The JDK is for developers, the JRE is for running Java applications, and the JVM is at the core, handling the execution of compiled bytecode.

---
---
---

# 10. Annotations

### Built-in Annotations in Java

Java provides several **built-in annotations** that are used to give the compiler and the JVM instructions about how to handle code elements. Annotations in Java can provide metadata for the code, influence the way it is compiled, and help in providing better documentation or runtime behavior. The built-in annotations can be divided into two categories:

1. **Annotations for Compilation**
2. **Annotations for Runtime**

---

### 1. **Annotations for Compilation**

These annotations give instructions to the compiler. They help to catch errors, suppress warnings, or ensure backward compatibility.

#### **@Override**
- Indicates that a method overrides a method declared in a superclass.
- The compiler will check that the method is indeed overriding a method from its superclass or implementing an interface method. If not, a compilation error occurs.

##### Example:

```java
class Parent {
    public void display() {
        System.out.println("Display in Parent");
    }
}

class Child extends Parent {
    @Override
    public void display() {  // Overrides the parent class method
        System.out.println("Display in Child");
    }
}
```

Here, `@Override` tells the compiler that the `display()` method in the `Child` class overrides the one in the `Parent` class.

---

#### **@Deprecated**
- Marks a method, class, or field as deprecated, meaning it is no longer recommended for use, and may be removed in future versions.
- The compiler issues a warning if a deprecated element is used.

##### Example:

```java
class MyClass {
    @Deprecated
    public void oldMethod() {
        System.out.println("This method is deprecated.");
    }

    public void newMethod() {
        System.out.println("Use this method instead.");
    }
}

public class Test {
    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.oldMethod();  // Compiler will warn that this method is deprecated
    }
}
```

Using the `oldMethod()` will result in a warning.

---

#### **@SuppressWarnings**
- Instructs the compiler to suppress certain warnings that would normally be raised. It is often used when working with older code or APIs that generate warnings.
- The value of this annotation is a string or array of strings representing the types of warnings to suppress (e.g., "unchecked", "deprecation").

##### Example:

```java
public class Test {
    @SuppressWarnings("unchecked")
    public void testRawTypes() {
        // Raw types can generate a warning, but this will suppress it
        List myList = new ArrayList();  // Unchecked type
        myList.add("Example");
    }
}
```

In this example, the `@SuppressWarnings("unchecked")` annotation suppresses the warning about using raw types in generics.

---

### 2. **Annotations for Runtime**

These annotations are used to influence runtime behavior, typically when working with frameworks or libraries like Spring, Hibernate, or custom annotations.

#### **@FunctionalInterface**
- Marks an interface as a **functional interface**, which means it can have exactly one abstract method and can be used in lambda expressions.
- If the interface contains more than one abstract method, the compiler will throw an error.

##### Example:

```java
@FunctionalInterface
interface MyFunctionalInterface {
    void performAction();
}

public class Test {
    public static void main(String[] args) {
        // Using lambda expression for the functional interface
        MyFunctionalInterface action = () -> System.out.println("Action performed!");
        action.performAction();
    }
}
```

In this case, `MyFunctionalInterface` is marked as a `@FunctionalInterface` and is used in a lambda expression.

---

#### **@SafeVarargs**
- Used to suppress warnings for **varargs** (variable arguments) when dealing with generics. This annotation can be applied to constructors or methods that use varargs.
- The method must be `final`, `static`, or `private`.

##### Example:

```java
public class MyClass {
    @SafeVarargs
    private static void printItems(List<String>... items) {
        for (List<String> item : items) {
            System.out.println(item);
        }
    }

    public static void main(String[] args) {
        List<String> list1 = Arrays.asList("One", "Two");
        List<String> list2 = Arrays.asList("Three", "Four");
        printItems(list1, list2);
    }
}
```

The `@SafeVarargs` annotation ensures that no unchecked warnings are issued when using varargs with generics.

---

### 3. **Meta-Annotations**

Java also provides meta-annotations, which are annotations applied to other annotations. They are used to define how annotations behave.

#### **@Retention**
- Specifies how long the annotation is retained in the program (i.e., its lifespan).
- The possible values are:
  - **RetentionPolicy.SOURCE**: The annotation is discarded by the compiler.
  - **RetentionPolicy.CLASS**: The annotation is recorded in the class file, but not available at runtime.
  - **RetentionPolicy.RUNTIME**: The annotation is available at runtime via reflection.

##### Example:

```java
@Retention(RetentionPolicy.RUNTIME)
@interface MyAnnotation {
    String value();
}
```

Here, the `MyAnnotation` annotation is retained at runtime and can be accessed through reflection.

---

#### **@Target**
- Specifies the kinds of elements an annotation can be applied to, such as methods, fields, classes, parameters, etc.
- The possible values are:
  - **ElementType.TYPE**: For classes, interfaces, enums.
  - **ElementType.METHOD**: For methods.
  - **ElementType.FIELD**: For fields.
  - **ElementType.PARAMETER**: For parameters.

##### Example:

```java
@Target(ElementType.METHOD)
@interface MyMethodAnnotation {
    String description();
}
```

Here, `MyMethodAnnotation` can only be applied to methods.

---

#### **@Inherited**
- Allows an annotation to be inherited from a superclass to a subclass.

##### Example:

```java
@Inherited
@Retention(RetentionPolicy.RUNTIME)
@interface MyInheritedAnnotation {}

@MyInheritedAnnotation
class ParentClass {}

class ChildClass extends ParentClass {}
```

In this case, the `ChildClass` inherits the `@MyInheritedAnnotation` from `ParentClass`.

---

#### **@Documented**
- Indicates that the use of the annotated element should be documented by javadoc and similar tools.

---

### Summary of Built-in Annotations:

| Annotation         | Purpose                                                    |
|--------------------|------------------------------------------------------------|
| **@Override**       | Indicates a method is overriding a superclass method.      |
| **@Deprecated**     | Marks a method, class, or field as deprecated.             |
| **@SuppressWarnings** | Suppresses compiler warnings.                            |
| **@FunctionalInterface** | Marks an interface as functional (with one abstract method). |
| **@SafeVarargs**    | Suppresses warnings for varargs with generics.             |
| **@Retention**      | Defines the retention policy of an annotation.             |
| **@Target**         | Specifies the types of elements an annotation can apply to.|
| **@Inherited**      | Indicates that an annotation is inherited by subclasses.   |
| **@Documented**     | Marks the annotation for documentation purposes.           |

---

### Example Code Combining Multiple Annotations:

```java
@FunctionalInterface
interface MathOperation {
    int operation(int a, int b);
}

public class Test {
    @Deprecated
    public static int add(int a, int b) {
        return a + b;
    }

    @Override
    public String toString() {
        return "Test Class";
    }

    public static void main(String[] args) {
        // Suppressing warnings for deprecated method usage
        @SuppressWarnings("deprecation")
        int sum = add(5, 3);

        MathOperation addition = (a, b) -> a + b;
        System.out.println(addition.operation(5, 3)); // Output: 8
    }
}
```

In this example:
- `@Deprecated` is used to mark the `add` method.
- `@Override` is used for the `toString` method.
- `@FunctionalInterface` is used to define the `MathOperation` interface.

---
---
---


### Custom Annotations in Java

Java allows you to create your own **custom annotations** to add metadata or behavior to your code. Custom annotations can be used to apply additional behavior, simplify repetitive tasks, or serve as markers for tools, frameworks, or libraries (like in Spring or JUnit).

---

### 1. **Creating Custom Annotations**

To create a custom annotation, you use the `@interface` keyword. A custom annotation is defined similarly to an interface, and it can have elements (or methods) that behave like attributes.

#### Syntax of a Custom Annotation:

```java
@interface MyAnnotation {
    String value() default "default value";
    int count() default 1;
}
```

- **`@interface`**: This defines an annotation.
- **Elements**: The elements inside the annotation behave like method declarations but without method bodies. They can also have default values.
- **Default values**: You can provide default values for elements.

---

### 2. **Meta-Annotations**

Meta-annotations are annotations applied to other annotations. They are used to define the behavior of your custom annotation.

| Meta-Annotation     | Description                                                 |
|---------------------|-------------------------------------------------------------|
| **@Retention**       | Specifies how long the annotation is retained (runtime, compile-time, or source-level). |
| **@Target**          | Specifies where the annotation can be applied (methods, classes, fields, etc.). |
| **@Inherited**       | Allows the annotation to be inherited by subclasses. |
| **@Documented**      | Ensures the annotation appears in Javadoc. |

#### Example:

```java
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
import java.lang.annotation.Target;
import java.lang.annotation.ElementType;

// Applying meta-annotations
@Retention(RetentionPolicy.RUNTIME)  // Annotation will be available at runtime
@Target({ElementType.TYPE, ElementType.METHOD})  // Can be used on classes and methods
public @interface MyCustomAnnotation {
    String description() default "Default Description";  // Element with default value
    int priority() default 1;
}
```

Here, `@MyCustomAnnotation` is defined with two elements, `description` and `priority`, with default values. The meta-annotations specify that the annotation can be used on classes and methods, and it will be retained at runtime (accessible via reflection).

---

### 3. **Using Custom Annotations**

Once you have defined a custom annotation, you can use it in your code just like the built-in annotations.

#### Example:

```java
@MyCustomAnnotation(description = "Class level annotation", priority = 5)
public class MyClass {

    @MyCustomAnnotation(description = "Method level annotation", priority = 10)
    public void myMethod() {
        System.out.println("Custom annotation applied to method");
    }
}
```

In this example:
- The `@MyCustomAnnotation` is used at both the class level and method level.
- The elements `description` and `priority` are explicitly assigned values.

---

### 4. **Accessing Annotations via Reflection**

If you specify `RetentionPolicy.RUNTIME`, you can access the annotation at runtime using **reflection**. This is useful for creating frameworks or tools that process annotations.

#### Example of Accessing Custom Annotations:

```java
import java.lang.reflect.Method;

public class AnnotationProcessor {
    public static void main(String[] args) {
        // Check if MyClass is annotated
        if (MyClass.class.isAnnotationPresent(MyCustomAnnotation.class)) {
            // Get the annotation from the class
            MyCustomAnnotation annotation = MyClass.class.getAnnotation(MyCustomAnnotation.class);
            System.out.println("Class annotation description: " + annotation.description());
            System.out.println("Class annotation priority: " + annotation.priority());
        }

        // Access annotations on methods
        for (Method method : MyClass.class.getDeclaredMethods()) {
            if (method.isAnnotationPresent(MyCustomAnnotation.class)) {
                MyCustomAnnotation methodAnnotation = method.getAnnotation(MyCustomAnnotation.class);
                System.out.println("Method: " + method.getName());
                System.out.println("Method annotation description: " + methodAnnotation.description());
                System.out.println("Method annotation priority: " + methodAnnotation.priority());
            }
        }
    }
}
```

In this example:
- The `isAnnotationPresent()` method is used to check if a class or method has a specific annotation.
- The `getAnnotation()` method retrieves the annotation, allowing you to access its elements.
  
If `MyClass` is annotated with `@MyCustomAnnotation`, the values of `description` and `priority` will be printed at runtime.

---

### 5. **Single-Element Annotations**

If an annotation only has one element, you can omit the element name when using it. The element must be named `value`.

#### Example:

```java
@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.METHOD)
@interface SingleElementAnnotation {
    String value();  // Single element
}

class MyClass {
    @SingleElementAnnotation("This is a single-element annotation")
    public void myMethod() {
        System.out.println("Method with single-element annotation");
    }
}
```

In this example, since `value` is the only element, it can be provided directly without specifying `value =`.

---

### 6. **Custom Annotations with Multiple Targets**

Custom annotations can be applied to different elements such as classes, fields, methods, parameters, etc., by using the `@Target` meta-annotation.

#### Example:

```java
@Retention(RetentionPolicy.RUNTIME)
@Target({ElementType.FIELD, ElementType.PARAMETER, ElementType.CONSTRUCTOR})
@interface MultiTargetAnnotation {
    String info() default "Default Info";
}

class MyClass {
    @MultiTargetAnnotation(info = "Field annotation")
    private String myField;

    @MultiTargetAnnotation(info = "Constructor annotation")
    public MyClass() {
        // Constructor logic
    }

    public void myMethod(@MultiTargetAnnotation(info = "Parameter annotation") String param) {
        System.out.println(param);
    }
}
```

Here, `@MultiTargetAnnotation` is applied to a field, constructor, and method parameter.

---

### 7. **Marker Annotations**

A marker annotation is a custom annotation without any elements. It is used to signal or mark something in the code.

#### Example:

```java
@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.METHOD)
@interface MarkerAnnotation {}

class MyClass {
    @MarkerAnnotation
    public void markedMethod() {
        System.out.println("This method is marked with a custom marker annotation");
    }
}
```

In this case, `MarkerAnnotation` is a marker annotation with no elements, used to "mark" the `markedMethod()`.

---

### 8. **Custom Annotation Example with Validation**

A common use case for custom annotations is to create validation rules. Below is an example of an annotation used for validating the range of values:

#### Annotation Definition:

```java
import java.lang.annotation.Retention;
import java.lang.annotation.RetentionPolicy;
import java.lang.annotation.Target;
import java.lang.annotation.ElementType;

@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.FIELD)
@interface Range {
    int min();
    int max();
}
```

#### Applying the Annotation:

```java
class MyClass {
    @Range(min = 1, max = 100)
    private int number;

    public MyClass(int number) {
        this.number = number;
    }
}
```

#### Validator Class:

```java
import java.lang.reflect.Field;

public class Validator {
    public static void validate(Object obj) throws IllegalArgumentException, IllegalAccessException {
        Field[] fields = obj.getClass().getDeclaredFields();
        for (Field field : fields) {
            if (field.isAnnotationPresent(Range.class)) {
                Range range = field.getAnnotation(Range.class);
                field.setAccessible(true);
                int value = (int) field.get(obj);
                if (value < range.min() || value > range.max()) {
                    throw new IllegalArgumentException("Value of field " + field.getName() + " is out of range");
                }
            }
        }
    }

    public static void main(String[] args) {
        MyClass myObj = new MyClass(150);
        try {
            validate(myObj);
        } catch (IllegalArgumentException | IllegalAccessException e) {
            System.out.println(e.getMessage());
        }
    }
}
```

In this example, `@Range` is used to define a valid range for the `number` field. The `Validator` class checks if the `number` field is within the specified range at runtime.

---

### Summary of Custom Annotations:

- **Custom annotations** allow you to define metadata for your code and provide instructions for frameworks or tools.
- You can control how custom annotations behave using **meta-annotations** like `@Retention`, `@Target`, `@Inherited`, and `@Documented`.
- Custom annotations are typically processed using **reflection**.
- They can be used to implement validation, processing, and documentation logic, or to mark code for special handling at runtime or compile-time.


---
---
---

# 11. Reflection API

### Accessing Methods and Fields at Runtime in Java

In Java, you can access methods, fields, and constructors of a class at runtime using **reflection**. Reflection is a powerful feature that allows a program to analyze and modify the runtime behavior of an application. The `java.lang.reflect` package provides the classes necessary to perform reflection in Java.

---

### 1. **Why Use Reflection?**
Reflection is often used for:
- Frameworks (e.g., Spring, Hibernate) to dynamically access or modify methods and fields at runtime.
- Performing operations on objects when you don't know their class at compile time.
- Debugging, testing, or implementing generic libraries.

---

### 2. **Basic Classes in Reflection**

| Class         | Description                                                                 |
|---------------|-----------------------------------------------------------------------------|
| **`Class`**   | Represents a class or interface. You can obtain its `Method`, `Field`, or `Constructor` objects to inspect or modify class members. |
| **`Method`**  | Represents a method of a class.                                             |
| **`Field`**   | Represents a field (variable) of a class.                                   |
| **`Constructor`** | Represents a constructor of a class.                                    |

You first obtain a `Class` object, which provides access to methods and fields at runtime.

---

### 3. **Getting the `Class` Object**

You can get the `Class` object in one of the following ways:
- **Using `Class.forName("className")`**: Provides the `Class` object for the given class name.
- **Using `object.getClass()`**: Gets the `Class` object for an object instance.
- **Using `ClassName.class`**: Directly retrieves the `Class` object for a known class.

#### Example:

```java
// Using Class.forName()
Class<?> class1 = Class.forName("com.example.MyClass");

// Using getClass()
MyClass obj = new MyClass();
Class<?> class2 = obj.getClass();

// Using ClassName.class
Class<?> class3 = MyClass.class;
```

---

### 4. **Accessing Methods at Runtime**

You can invoke methods at runtime using the `Method` class. Once you have the `Method` object, you can invoke the method on an instance of the class.

#### Steps to Access Methods:
1. Obtain the `Method` object using `getMethod()` or `getDeclaredMethod()`.
2. Invoke the method using `invoke()`.

#### Example:

```java
import java.lang.reflect.Method;

class MyClass {
    public void greet(String name) {
        System.out.println("Hello, " + name);
    }
}

public class ReflectionExample {
    public static void main(String[] args) throws Exception {
        // Create an instance of MyClass
        MyClass obj = new MyClass();

        // Get the Class object
        Class<?> clazz = obj.getClass();

        // Get the Method object for 'greet' method
        Method method = clazz.getMethod("greet", String.class);

        // Invoke the method with a parameter
        method.invoke(obj, "John");
    }
}
```

In this example:
- We obtain the `Method` object for the `greet()` method of the `MyClass`.
- The `invoke()` method is called to execute the method, passing `"John"` as a parameter.

---

### 5. **Accessing Fields at Runtime**

You can access and modify the fields (variables) of a class at runtime using the `Field` class. This allows you to dynamically read or write data to an object's fields.

#### Steps to Access Fields:
1. Obtain the `Field` object using `getField()` or `getDeclaredField()`.
2. Read or modify the field's value using `get()` or `set()`.

#### Example:

```java
import java.lang.reflect.Field;

class Person {
    public String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

public class FieldAccessExample {
    public static void main(String[] args) throws Exception {
        // Create an instance of Person
        Person person = new Person("Alice", 30);

        // Get the Class object
        Class<?> clazz = person.getClass();

        // Access the public field 'name'
        Field nameField = clazz.getField("name");
        System.out.println("Name before: " + nameField.get(person));

        // Modify the value of 'name'
        nameField.set(person, "Bob");
        System.out.println("Name after: " + nameField.get(person));

        // Access the private field 'age'
        Field ageField = clazz.getDeclaredField("age");
        ageField.setAccessible(true);  // Make the private field accessible
        System.out.println("Age before: " + ageField.get(person));

        // Modify the value of 'age'
        ageField.set(person, 35);
        System.out.println("Age after: " + ageField.get(person));
    }
}
```

In this example:
- We access the public field `name` using `getField()` and modify its value.
- For the private field `age`, we use `getDeclaredField()` and call `setAccessible(true)` to bypass access control. This allows us to modify the private field.

---

### 6. **Accessing Constructors at Runtime**

You can create instances of a class at runtime using constructors and the `Constructor` class.

#### Example:

```java
import java.lang.reflect.Constructor;

class MyClass {
    private String message;

    public MyClass(String message) {
        this.message = message;
    }

    public void printMessage() {
        System.out.println(message);
    }
}

public class ConstructorAccessExample {
    public static void main(String[] args) throws Exception {
        // Get the Class object
        Class<?> clazz = MyClass.class;

        // Get the Constructor object for the constructor that takes a String argument
        Constructor<?> constructor = clazz.getConstructor(String.class);

        // Create a new instance using the constructor
        MyClass obj = (MyClass) constructor.newInstance("Hello from reflection");

        // Invoke a method on the newly created object
        obj.printMessage();
    }
}
```

In this example:
- We access the constructor of `MyClass` that takes a `String` argument.
- We use `newInstance()` to create a new object of `MyClass` and invoke the `printMessage()` method on the object.

---

### 7. **Handling Exceptions in Reflection**

Reflection operations often throw several checked exceptions that need to be handled:
- **`ClassNotFoundException`**: Thrown when trying to load a class with `Class.forName()` and the class is not found.
- **`NoSuchMethodException`**: Thrown when a specified method is not found.
- **`NoSuchFieldException`**: Thrown when a specified field is not found.
- **`IllegalAccessException`**: Thrown when the program does not have access to the field, method, or constructor.
- **`InvocationTargetException`**: Thrown if the underlying method or constructor throws an exception.

It is important to handle these exceptions properly, either using `try-catch` blocks or declaring them in the method signature.

---

### 8. **Limitations and Drawbacks of Reflection**
- **Performance**: Reflection operations are generally slower compared to direct method/field access.
- **Security**: Reflection can bypass normal access control (e.g., private fields and methods), which can introduce security risks.
- **Compile-time safety**: Reflection reduces type-safety because method and field names are provided as strings, which means errors are only caught at runtime.

---

### Summary of Accessing Methods and Fields at Runtime:

- **Reflection** allows you to inspect and modify the structure and behavior of objects at runtime.
- You can dynamically access methods using `getMethod()` and `invoke()`.
- Fields can be accessed and modified using `getField()`, `getDeclaredField()`, `get()`, and `set()`.
- Reflection is useful for dynamic frameworks, testing, and advanced Java programs but should be used carefully due to its performance and security implications.

---
---
---

# 12. Networking in Java

### Sockets in Java (TCP, UDP)

Sockets are endpoints for communication between two machines over a network. They provide a way for applications to communicate using the **Transport Layer** protocols, like **TCP** and **UDP**. 

Java provides support for both **TCP (Transmission Control Protocol)** and **UDP (User Datagram Protocol)** through classes in the `java.net` package.

---

### 1. **TCP (Transmission Control Protocol)**
TCP is a connection-oriented protocol that ensures reliable data transmission between a client and server. It guarantees that packets are delivered in order and without any loss.

#### Characteristics of TCP:
- **Reliable**: Guarantees data delivery.
- **Connection-Oriented**: A connection is established before data transfer.
- **Stream-Based**: Data is read as a continuous stream.
- **Slower but Accurate**: TCP checks for errors and retransmits lost packets.

In Java, TCP communication is handled using:
- **ServerSocket**: For server-side communication.
- **Socket**: For client-side communication.

#### Example: TCP Server-Client Communication

##### TCP Server:
```java
import java.io.*;
import java.net.*;

public class TCPServer {
    public static void main(String[] args) {
        try (ServerSocket serverSocket = new ServerSocket(8080)) {
            System.out.println("Server is listening on port 8080");

            while (true) {
                Socket socket = serverSocket.accept();  // Accept incoming client connection
                System.out.println("Client connected");

                // Get input and output streams
                InputStream input = socket.getInputStream();
                BufferedReader reader = new BufferedReader(new InputStreamReader(input));

                OutputStream output = socket.getOutputStream();
                PrintWriter writer = new PrintWriter(output, true);

                String message;
                // Receive message from client
                while ((message = reader.readLine()) != null) {
                    System.out.println("Received: " + message);
                    writer.println("Message received: " + message);  // Send response to client
                }
            }
        } catch (IOException ex) {
            ex.printStackTrace();
        }
    }
}
```

##### TCP Client:
```java
import java.io.*;
import java.net.*;

public class TCPClient {
    public static void main(String[] args) {
        try (Socket socket = new Socket("localhost", 8080)) {
            // Get input and output streams
            OutputStream output = socket.getOutputStream();
            PrintWriter writer = new PrintWriter(output, true);

            InputStream input = socket.getInputStream();
            BufferedReader reader = new BufferedReader(new InputStreamReader(input));

            // Send a message to the server
            writer.println("Hello Server!");

            // Receive and print the server's response
            String response = reader.readLine();
            System.out.println("Server response: " + response);
        } catch (IOException ex) {
            ex.printStackTrace();
        }
    }
}
```

In this example:
- The **TCP server** listens for incoming connections on port 8080.
- When a client connects, the server accepts the connection and starts communication.
- The **TCP client** sends a message to the server, and the server responds with a confirmation message.

---

### 2. **UDP (User Datagram Protocol)**
UDP is a connectionless, lightweight protocol that doesn't guarantee reliable communication. It’s faster than TCP but does not ensure the delivery of data packets.

#### Characteristics of UDP:
- **Unreliable**: No guarantee of packet delivery.
- **Connectionless**: No formal connection is established.
- **Packet-Based**: Data is sent in discrete packets.
- **Faster but Less Reliable**: No error checking or retransmission.

In Java, UDP communication is handled using:
- **DatagramSocket**: For both server and client communication.
- **DatagramPacket**: To send and receive packets.

#### Example: UDP Server-Client Communication

##### UDP Server:
```java
import java.net.*;

public class UDPServer {
    public static void main(String[] args) {
        try (DatagramSocket socket = new DatagramSocket(9876)) {
            byte[] buffer = new byte[1024];

            System.out.println("UDP server is running...");

            while (true) {
                DatagramPacket request = new DatagramPacket(buffer, buffer.length);
                socket.receive(request);  // Receive request from client
                String message = new String(request.getData(), 0, request.getLength());
                System.out.println("Received: " + message);

                // Send response back to client
                String responseMessage = "Message received";
                byte[] responseData = responseMessage.getBytes();
                DatagramPacket response = new DatagramPacket(responseData, responseData.length, request.getAddress(), request.getPort());
                socket.send(response);  // Send response
            }
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

##### UDP Client:
```java
import java.net.*;

public class UDPClient {
    public static void main(String[] args) {
        try (DatagramSocket socket = new DatagramSocket()) {
            byte[] buffer = "Hello UDP Server".getBytes();
            InetAddress address = InetAddress.getByName("localhost");

            // Send packet to server
            DatagramPacket request = new DatagramPacket(buffer, buffer.length, address, 9876);
            socket.send(request);

            // Receive response from server
            byte[] responseBuffer = new byte[1024];
            DatagramPacket response = new DatagramPacket(responseBuffer, responseBuffer.length);
            socket.receive(response);  // Receive response from server

            String message = new String(response.getData(), 0, response.getLength());
            System.out.println("Server response: " + message);
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

In this example:
- The **UDP server** listens on port 9876 and waits for incoming packets.
- The **UDP client** sends a message to the server, and the server responds with a confirmation message.

---

### 3. **Key Differences Between TCP and UDP**

| **Aspect**               | **TCP**                                                   | **UDP**                              |
|--------------------------|-----------------------------------------------------------|--------------------------------------|
| **Connection**            | Connection-oriented (a connection must be established)    | Connectionless (no connection setup) |
| **Reliability**           | Ensures reliable, ordered, and error-checked delivery     | No guarantee of delivery, unordered  |
| **Data Transmission**     | Stream-based (continuous flow of data)                    | Packet-based (discrete data packets) |
| **Speed**                 | Slower due to reliability mechanisms                      | Faster, but less reliable            |
| **Use Cases**             | File transfer, web browsing, email                        | Streaming, gaming, voice calls       |

---

### 4. **When to Use TCP vs UDP?**

- **Use TCP** when data integrity and order are crucial. For example, file transfer, web pages, and emails where data must arrive without errors.
- **Use UDP** when speed is critical and occasional data loss is acceptable. For example, real-time applications like online gaming, video streaming, and VoIP where speed is more important than 100% accuracy.

---

### Summary:
- **TCP** ensures reliable, ordered communication through a connection-oriented protocol.
- **UDP** is connectionless, faster, and suitable for applications where occasional data loss is acceptable.
- Java provides classes like `ServerSocket`, `Socket`, `DatagramSocket`, and `DatagramPacket` to implement both TCP and UDP communication.

---
---
---


### URL and HttpURLConnection in Java

Java provides a powerful API to interact with web resources using classes from the `java.net` package. The two key classes for interacting with URLs and performing HTTP requests are:
- **URL**: Represents a Uniform Resource Locator, which is a pointer to a resource on the web.
- **HttpURLConnection**: Allows for HTTP-specific interactions with URLs (GET, POST, PUT, DELETE).

---

### 1. **URL Class**
The **URL** class represents a URL (Uniform Resource Locator). It encapsulates a web address and provides methods to access the various components of a URL such as protocol, host, port, file path, and query.

#### Key Components of a URL:
- **Protocol**: The communication protocol (e.g., HTTP, HTTPS, FTP).
- **Host**: The domain name or IP address of the server.
- **Port**: The port number (optional, defaults to 80 for HTTP).
- **File**: The resource path on the server (e.g., `/index.html`).
- **Query**: Optional parameters in the form of key-value pairs (e.g., `?id=100`).

#### Example: Working with the URL Class
```java
import java.net.URL;

public class URLExample {
    public static void main(String[] args) {
        try {
            URL url = new URL("https://example.com:8080/docs/index.html?id=100");

            System.out.println("Protocol: " + url.getProtocol());  // https
            System.out.println("Host: " + url.getHost());          // example.com
            System.out.println("Port: " + url.getPort());          // 8080
            System.out.println("Path: " + url.getPath());          // /docs/index.html
            System.out.println("Query: " + url.getQuery());        // id=100
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

### Methods of `URL` Class:
- `getProtocol()`: Returns the protocol of the URL (e.g., `http`, `https`).
- `getHost()`: Returns the host name of the URL.
- `getPort()`: Returns the port number.
- `getPath()`: Returns the file path after the host.
- `getQuery()`: Returns the query string, which comes after the '?' in the URL.

---

### 2. **HttpURLConnection Class**
The **HttpURLConnection** class is used for creating an HTTP connection to a URL. It allows you to send requests and receive responses from a web server. You can perform different types of HTTP requests, such as:
- **GET**: Retrieve data from a server.
- **POST**: Submit data to be processed to a server.
- **PUT**, **DELETE**: Modify or delete a resource.

#### Steps to Use HttpURLConnection:
1. Create a `URL` object.
2. Call `openConnection()` on the `URL` object to get an `HttpURLConnection` instance.
3. Set the HTTP request method (e.g., GET, POST).
4. Read or write data as required (for POST/PUT requests).
5. Read the response from the server.

#### Example: GET Request using HttpURLConnection
```java
import java.io.*;
import java.net.HttpURLConnection;
import java.net.URL;

public class HttpURLConnectionExample {
    public static void main(String[] args) {
        try {
            // Step 1: Create a URL object
            URL url = new URL("https://jsonplaceholder.typicode.com/posts/1");

            // Step 2: Open the connection and cast to HttpURLConnection
            HttpURLConnection connection = (HttpURLConnection) url.openConnection();

            // Step 3: Set the request method to GET
            connection.setRequestMethod("GET");

            // Step 4: Get the response code
            int responseCode = connection.getResponseCode();
            System.out.println("Response Code: " + responseCode);

            // Step 5: Read the response from the input stream
            BufferedReader in = new BufferedReader(new InputStreamReader(connection.getInputStream()));
            String inputLine;
            StringBuilder content = new StringBuilder();

            while ((inputLine = in.readLine()) != null) {
                content.append(inputLine);
            }

            // Close the streams
            in.close();
            connection.disconnect();

            // Step 6: Print the response content
            System.out.println("Response: " + content.toString());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

#### Example Output:
```json
Response Code: 200
Response: {
    "userId": 1,
    "id": 1,
    "title": "Sample Post",
    "body": "This is a sample post from jsonplaceholder"
}
```

In this example:
- We make a **GET** request to retrieve a post from `jsonplaceholder.typicode.com`, which is a free REST API for testing.
- The `HttpURLConnection` is opened, and the response is read from the input stream.

---

#### Example: POST Request using HttpURLConnection
To send data to a server using a **POST** request:

```java
import java.io.*;
import java.net.HttpURLConnection;
import java.net.URL;

public class HttpPostExample {
    public static void main(String[] args) {
        try {
            URL url = new URL("https://jsonplaceholder.typicode.com/posts");

            // Open connection
            HttpURLConnection connection = (HttpURLConnection) url.openConnection();

            // Set request method to POST
            connection.setRequestMethod("POST");

            // Enable sending data
            connection.setDoOutput(true);

            // Set request properties
            connection.setRequestProperty("Content-Type", "application/json; utf-8");
            connection.setRequestProperty("Accept", "application/json");

            // Create the JSON request body
            String jsonInputString = "{\"title\": \"New Post\", \"body\": \"This is the body of the new post\", \"userId\": 1}";

            // Send the JSON request
            try (OutputStream os = connection.getOutputStream()) {
                byte[] input = jsonInputString.getBytes("utf-8");
                os.write(input, 0, input.length);
            }

            // Get the response code
            int responseCode = connection.getResponseCode();
            System.out.println("Response Code: " + responseCode);

            // Read the response
            BufferedReader in = new BufferedReader(new InputStreamReader(connection.getInputStream(), "utf-8"));
            String inputLine;
            StringBuilder response = new StringBuilder();
            while ((inputLine = in.readLine()) != null) {
                response.append(inputLine);
            }

            // Close connections
            in.close();
            connection.disconnect();

            // Print response
            System.out.println("Response: " + response.toString());

        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}
```

#### Example Output (Partial):
```json
Response Code: 201
Response: {
  "id": 101,
  "title": "New Post",
  "body": "This is the body of the new post",
  "userId": 1
}
```

In this example:
- A **POST** request is sent to `jsonplaceholder.typicode.com` with a JSON payload.
- The server creates a new post and returns a response with the newly created post.

---

### Key Methods of **HttpURLConnection**:
- `setRequestMethod(String method)`: Sets the HTTP method (e.g., GET, POST, PUT, DELETE).
- `getResponseCode()`: Returns the HTTP status code (e.g., 200 for success, 404 for not found).
- `getInputStream()`: Returns the input stream for reading the server’s response.
- `getOutputStream()`: Returns the output stream to send data to the server.
- `setDoOutput(boolean)`: Enables output for POST/PUT requests.
- `disconnect()`: Closes the connection.

---

### Summary:
- The **URL** class in Java represents a web address and provides methods to access its components.
- The **HttpURLConnection** class is used to send HTTP requests (GET, POST, etc.) to a server and read its response.
- You can easily perform network operations like fetching data, submitting data, and handling responses using `URL` and `HttpURLConnection`.

---
---
---

# 13. JDBC (Java Database Connectivity)