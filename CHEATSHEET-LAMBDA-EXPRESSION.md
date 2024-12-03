Here’s a **cheat sheet** for Lambda Expressions in Java:

---

### **Syntax Basics**
1. **No Parameters**:  
   ```java
   () -> System.out.println("Hello, World!");
   ```

2. **Single Parameter** (Parentheses optional):  
   ```java
   name -> System.out.println("Hello, " + name + "!");
   ```

3. **Multiple Parameters**:  
   ```java
   (a, b) -> a + b;
   ```

4. **Code Block**:  
   ```java
   (a, b) -> {
       int result = a + b;
       return result;
   };
   ```

---

### **Using Functional Interfaces**
1. **Custom Functional Interface**:  
   ```java
   @FunctionalInterface
   interface Calculator {
       int add(int a, int b);
   }

   Calculator calc = (a, b) -> a + b;
   System.out.println(calc.add(5, 3));  // Output: 8
   ```

2. **Built-in Functional Interfaces**:  
   - **Consumer**: Accepts a value and performs an action.  
     ```java
     Consumer<String> print = message -> System.out.println(message);
     print.accept("Hello!");  // Output: Hello!
     ```

   - **Predicate**: Tests a condition and returns `true` or `false`.  
     ```java
     Predicate<Integer> isEven = num -> num % 2 == 0;
     System.out.println(isEven.test(4));  // Output: true
     ```

   - **Function**: Takes one argument and returns a result.  
     ```java
     Function<String, Integer> length = str -> str.length();
     System.out.println(length.apply("Lambda"));  // Output: 6
     ```

   - **Supplier**: Supplies a value with no arguments.  
     ```java
     Supplier<Double> random = () -> Math.random();
     System.out.println(random.get());
     ```

---

### **Using Lambda with Collections**
1. **Iterating Over a List**:  
   ```java
   List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
   names.forEach(name -> System.out.println(name));
   ```

2. **Filtering a Stream**:  
   ```java
   names.stream()
        .filter(name -> name.startsWith("C"))
        .forEach(name -> System.out.println(name));
   ```

3. **Mapping Values**:  
   ```java
   names.stream()
        .map(name -> name.toUpperCase())
        .forEach(System.out::println);
   ```

---

### **Common Shortcuts**
1. **Using Method References**:  
   ```java
   names.forEach(System.out::println);
   ```

2. **Inline Return (Single Statement)**:  
   ```java
   (a, b) -> a + b;
   ```

3. **Multiline Code Block**:  
   ```java
   (a, b) -> {
       int sum = a + b;
       System.out.println("Sum: " + sum);
       return sum;
   };
   ```

---

This cheat sheet provides concise examples for quick reference while working with Lambda Expressions!