### **Java Stream API Cheat Sheet**

---

### **What is Stream API?**  
The **Stream API**, introduced in Java 8, provides a powerful way to process sequences of data (like collections) in a declarative and functional style. It helps in **filtering, mapping, reducing**, and performing operations like **sorting and aggregation** on data.

---

### **Stream API Basics**

1. **Creating Streams**
   - From a Collection:  
     ```java
     List<String> list = Arrays.asList("A", "B", "C");
     Stream<String> stream = list.stream();
     ```
   - From an Array:  
     ```java
     String[] array = {"A", "B", "C"};
     Stream<String> stream = Arrays.stream(array);
     ```
   - Using `Stream.of`:  
     ```java
     Stream<Integer> stream = Stream.of(1, 2, 3);
     ```

2. **Terminal vs. Intermediate Operations**  
   - **Intermediate Operations**: Transform a stream into another stream (lazy evaluation).  
     Example: `filter`, `map`, `sorted`.  
   - **Terminal Operations**: Produce a result or a side effect (eager evaluation).  
     Example: `forEach`, `collect`, `reduce`.

---

### **Common Stream API Operations**

1. **Filter**: Keep elements that match a condition.  
   ```java
   List<String> filtered = list.stream()
                               .filter(str -> str.startsWith("A"))
                               .collect(Collectors.toList());
   ```

2. **Map**: Transform each element.  
   ```java
   List<Integer> lengths = list.stream()
                               .map(String::length)
                               .collect(Collectors.toList());
   ```

3. **Sorted**: Sort elements.  
   ```java
   List<String> sorted = list.stream()
                             .sorted()
                             .collect(Collectors.toList());
   ```

4. **forEach**: Perform an action for each element.  
   ```java
   list.stream().forEach(System.out::println);
   ```

5. **Reduce**: Combine elements to produce a single result.  
   ```java
   Optional<Integer> sum = list.stream()
                               .map(String::length)
                               .reduce((a, b) -> a + b);
   ```

6. **Distinct**: Remove duplicates.  
   ```java
   List<Integer> distinct = numbers.stream()
                                   .distinct()
                                   .collect(Collectors.toList());
   ```

7. **Limit and Skip**: Limit the number of elements or skip elements.  
   ```java
   List<Integer> limited = numbers.stream()
                                  .limit(3)
                                  .collect(Collectors.toList());

   List<Integer> skipped = numbers.stream()
                                  .skip(2)
                                  .collect(Collectors.toList());
   ```

8. **Count**: Count the number of elements.  
   ```java
   long count = list.stream()
                    .filter(str -> str.startsWith("A"))
                    .count();
   ```

---

### **Collectors**

1. **Collect to a List**:  
   ```java
   List<String> result = stream.collect(Collectors.toList());
   ```

2. **Collect to a Set**:  
   ```java
   Set<String> result = stream.collect(Collectors.toSet());
   ```

3. **Joining Strings**:  
   ```java
   String joined = stream.collect(Collectors.joining(", "));
   ```

4. **Group By**:  
   ```java
   Map<Integer, List<String>> grouped = list.stream()
                                           .collect(Collectors.groupingBy(String::length));
   ```

---

### **Example Workflow**
```java
import java.util.Arrays;
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<String> names = Arrays.asList("Alice", "Bob", "Charlie", "David", "Alice");

        // Filter names that start with 'A', convert to uppercase, and remove duplicates
        List<String> result = names.stream()
                                   .filter(name -> name.startsWith("A"))
                                   .map(String::toUpperCase)
                                   .distinct()
                                   .sorted()
                                   .collect(Collectors.toList());

        System.out.println(result);  // Output: [ALICE]
    }
}
```

---

### **Common Method Reference Shortcuts**
1. **Static Method Reference**:  
   ```java
   Stream<Double> randoms = Stream.generate(Math::random);
   ```

2. **Instance Method Reference**:  
   ```java
   list.stream().forEach(System.out::println);
   ```

3. **Constructor Reference**:  
   ```java
   Stream<String> stream = list.stream().map(String::new);
   ```

---

This cheat sheet should help you quickly recall essential **Stream API** operations!