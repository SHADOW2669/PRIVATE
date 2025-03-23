### 1. **String Length**  
The `length()` method returns the number of characters in a string.  

**Example:**  
```java
public class Main {
    public static void main(String[] args) {
        String text = "Hello, World!";
        System.out.println("Length: " + text.length()); // Output: 13
    }
}
```

### 2. **Special String Operations**  
Special operations include substring extraction, replacing characters, and changing case.  

**Example (Substring & Replace):**  
```java
public class Main {
    public static void main(String[] args) {
        String text = "Java Programming";
        System.out.println("Substring: " + text.substring(5, 16)); // "Programming"
        System.out.println("Replace: " + text.replace("Java", "Python")); // "Python Programming"
    }
}
```

### 3. **String Literals**  
A string literal is any text enclosed in double quotes (`""`). Java automatically stores string literals in a special pool for efficiency.  

**Example:**  
```java
public class Main {
    public static void main(String[] args) {
        String str1 = "Hello"; // String literal
        String str2 = "Hello"; // Uses the same memory location as str1
        System.out.println(str1 == str2); // true (same memory reference)
    }
}
```

### 4. **String Concatenation**  
Concatenation means joining two strings using `+`.  

**Example:**  
```java
public class Main {
    public static void main(String[] args) {
        String firstName = "John";
        String lastName = "Doe";
        String fullName = firstName + " " + lastName;
        System.out.println("Full Name: " + fullName); // "John Doe"
    }
}
```

### 5. **String Concatenation with Other Data Types**  
When you concatenate a string with a number or other data type, Java automatically converts the other type into a string.  

**Example:**  
```java
public class Main {
    public static void main(String[] args) {
        int age = 25;
        double height = 5.9;
        String message = "Age: " + age + ", Height: " + height;
        System.out.println(message); // "Age: 25, Height: 5.9"
    }
}
```
