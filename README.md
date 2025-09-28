# Error Handling in C++

##  Overview
Error handling in C++ is a programming mechanism used to **detect and manage runtime errors** in a controlled way.  
- It ensures that a program does not **crash unexpectedly** when encountering exceptional situations like division by zero, file not found, invalid input, or memory allocation failure.  
- C++ provides **exception handling** features using `try`, `catch`, and `throw` keywords to manage errors efficiently.  
- Proper error handling improves the **robustness and reliability** of software applications.

---

##  Theory

###  Exception Handling Mechanism
C++ uses **exceptions** to report and handle errors:
1. **Throwing an Exception (`throw`)**:  
   - When a problem occurs, an exception is thrown using the `throw` keyword.  
   ```cpp
   if (denominator == 0) {
       throw "Division by zero error!";
   }

2. **Catching an Exception (`catch`)
   - Exceptions thrown in a `try` block can be handled using one or more `catch` blocks.  
   - Each `catch` block specifies the type of exception it can handle.  
   - The first `catch` block matching the exception type executes, and the program continues after the try-      catch structure.
  ```cpp
      catch (const char* msg) {
      cout << "Error: " << msg << endl;
      }
```
3. **Try Block (`try`)
  - The `try` block contains the code that might generate an exception.  
  - Any exception thrown within the `try` block is caught by the corresponding `catch` block(s).  
  - Multiple `catch` blocks can follow a single `try` block to handle different types of exceptions.  
  ```cpp
    try {
      int result = numerator / denominator;
    }
  ```
---

###  Flow of Exception Handling
The flow of exception handling in C++ follows these steps:

1. The code inside a `try` block executes normally.  
2. If an exception occurs within the `try` block:  
   - The remaining code in the `try` block is **skipped**.  
   - Control is transferred to the **first matching `catch` block** that can handle the exception type.  
3. The `catch` block executes, handling the exception.  
4. After executing the `catch` block, the program **continues execution** after the try-catch structure.  
5. If no matching `catch` block is found, the program terminates and may display an **uncaught exception** error.

---

# Program Summary

##  1.Division of Two Numbers with Exception Handling in C++
This program performs **division of two numbers** while handling the **division by zero** error using **C++ exception handling**.  
- The user inputs two numbers, `n1` and `n2`.  
- The program checks if the denominator `n2` is zero.  
  - If `n2` is zero, it **throws an exception**.  
  - Otherwise, it performs the division and displays the result.  
- The thrown exception is **caught in the `catch` block**, displaying a proper error message.  
- This program demonstrates how to **prevent runtime errors** using `try` and `catch`.

---

##  Algorithm
1. **Start**  
2. Input two numbers: `n1` (numerator) and `n2` (denominator).  
3. Use a `try` block to check for division by zero:
   - If `n2 == 0`, throw an exception with the value of `n2`.  
   - Else, perform the division `ans = n1 / n2` and display the result.  
4. Use a `catch` block to handle the exception:
   - Display an error message showing that division by zero occurred.  
5. Continue program execution after the exception is handled.  
6. **End**

---

##  2.Age Validation for Voting using Exception Handling in C++
This program checks if a user is eligible to vote based on their age using **C++ exception handling**.  
- The user inputs their age.  
- If the age is **less than 18**, the program **throws an exception**.  
- The exception is **caught in a `catch` block**, displaying an error message indicating ineligibility.  
- If the age is **18 or above**, the program displays the entered age and confirms eligibility.  
- This demonstrates how **exceptions can be used for input validation** and error handling.

---

##  Algorithm
1. **Start**  
2. Input `age` from the user.  
3. Use a `try` block to check eligibility:
   - If `age < 18`, throw `age` as an exception.  
   - Else, display `"Your age is: <age>"` and confirm eligibility.  
4. Use a `catch` block to handle the exception:
   - Display `"ERROR! YOU ARE NOT ELIGIBLE FOR VOTING."`  
5. Continue program execution after handling the exception.  
6. **End**

---

##  Conclusion
- Exception handling in C++ provides a **structured way to detect and manage runtime errors** without crashing the program.  
- The combination of **`try`, `throw`, and `catch`** separates normal program logic from error-handling logic, making code cleaner and easier to maintain.  
- Proper error handling improves the **robustness, reliability, and user experience** of software applications.  
- It is recommended to handle **expected errors** using exceptions and avoid using exceptions for normal program flow.  
- By effectively using exception handling, programs can **recover from errors gracefully** and continue execution safely.
