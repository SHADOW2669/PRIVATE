# PHP Variable Scope

The scope of a variable is defined as its range in the program under which it can be accessed. In other words, "The scope of a variable is the portion of the program within which it is defined and can be accessed."

PHP has three types of variable scopes:

---

## **1. Local Variable**
1. The variables that are declared within a function are called local variables for that function. These local variables have their scope only in that particular function in which they are declared. This means that these variables cannot be accessed outside the function, as they have local scope.
2. A variable declaration outside the function with the same name is completely different from the variable declared inside the function.

### **Example: Local Variable (local_variable1.php)**
```php
<?php
function local_var() {
    $num = 45; // Local variable
    echo "Local variable declared inside the function is: " . $num;
}
local_var();
?>
```
**Output:**  
_Local variable declared inside the function is: 45_

---

## **2. Global Variable**
1. Global variables are the variables that are declared outside the function. These variables can be accessed anywhere in the program.
2. To access a global variable within a function, use the `global` keyword before the variable. However, these variables can be directly accessed or used outside the function without any keyword.

### **Example: Global Variable (global_variable1.php)**
```php
<?php
$name = "Sanaya Sharma"; // Global Variable

function global_var() {
    global $name;
    echo "Variable inside the function: " . $name;
    echo "</br>";
}

global_var();
echo "Variable outside the function: " . $name;
?>
```
**Output:**  
_Variable inside the function: Sanaya Sharma_  
_Variable outside the function: Sanaya Sharma_

---

## **3. Static Variable**
1. In PHP, local variables are deleted once the function completes execution and memory is freed. However, sometimes we need to retain a variable's value even after function execution.
2. To achieve this, we use the `static` keyword to define a variable, creating a static variable.
3. Static variables exist only in a local function, but they do not lose their value between function calls.

### **Example: Static Variable (static_variable.php)**
```php
<?php
function static_var() {
    static $num1 = 3; // Static variable
    $num2 = 6; // Non-static variable
    
    $num1++; // Increment static variable
    $num2++; // Increment non-static variable
    
    echo "Static: " . $num1 . "</br>";
    echo "Non-static: " . $num2 . "</br>";
}

// First function call
static_var();

// Second function call
static_var();
?>
```
**Output:**  
_Static: 4_  
_Non-static: 7_  
_Static: 5_  
_Non-static: 7_

---

## **4. Function Scope**
1. Function scope refers to the visibility of variables within a function.
2. Variables declared inside a function are only accessible within that function.
3. If a variable is required inside a function but declared outside, it must be accessed using `global` or `$GLOBALS`.

### **Example: Function Scope**
```php
<?php
function exampleFunction() {
    $message = "Hello from inside the function!";
    echo $message;
}

exampleFunction(); // Works fine

// echo $message; // This would cause an error, as $message is not accessible outside the function
?>
```
**Output:**  
_Hello from inside the function!_

---
