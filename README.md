# Exception-handling-in-cpp


## Aim
To study and understand the concept of **exception handling in C++**, and explore how runtime errors can be managed gracefully using `try`, `throw`, and `catch`.  
The goal is to make programs more robust and reliable by handling errors instead of letting the program terminate unexpectedly.

---

## Theory
Exception handling in C++ provides a mechanism to detect and handle errors that occur during program execution.  
Instead of terminating the program immediately when an error occurs, exceptions allow programmers to transfer control to a safe handling block.  

### Key Concepts:
- **try block**: Contains the code that may cause an exception.  
- **throw statement**: Used to signal an error when it occurs.  
- **catch block**: Handles the error and executes corrective actions.  

### Benefits of Exception Handling:
- Prevents abrupt program termination.  
- Allows separation of error-handling code from normal code.  
- Provides a structured mechanism to manage different types of errors.  
- Improves program reliability and user experience.

### Common Exceptions in C++:
- Division by zero  
- Array index out of bounds  
- Null pointer access  
- Memory allocation failure  
- Invalid user input  
- Custom user-defined exceptions  

---

## Algorithms

### 1. Division by Zero Handling
Start  
Input two integers (a, b).  
Enter try block.  
  If b == 0, throw an exception.  
  Else, compute result = a / b.  
Catch the exception if thrown.  
Display error message or result.  
End  

### 2. Array Index Out of Bounds
Start  
Define an array with fixed size.  
Input index value.  
Enter try block.  
  If index < 0 or index >= array size, throw exception.  
  Else, access array[index].  
Catch the exception if thrown.  
Display error message or array value.  
End  

### 3. Multiple Exception Handling
Start  
Enter try block.  
  Perform operation that may throw integer, double, or unknown exception.  
Catch block 1 handles integer exception.  
Catch block 2 handles double exception.  
Catch block 3 (default) handles unknown exceptions.  
Display appropriate message.  
End  

### 4. File Handling Exception (Optional Use Case)
Start  
Open a file for reading or writing.  
Enter try block.  
  If file fails to open, throw an exception.  
Catch the exception if thrown.  
Display error message or process the file.  
End  

### 5. Custom Exception Handling
Start  
Define a custom exception class.  
Enter try block.  
  If a specific condition occurs, throw an object of the custom exception class.  
Catch block handles the custom exception.  
Display custom error message.  
End  

---

## Best Practices
- Always include a base case to prevent unhandled exceptions.  
- Use multiple catch blocks for handling different types of exceptions.  
- Avoid using exceptions for normal program flow; they should only handle exceptional conditions.  
- Clean up resources (like memory or file handles) in a `catch` block or use RAII for automatic cleanup.  

---

## Conclusion
- Exception handling in C++ provides a structured way to manage runtime errors.  
- `try` contains risky code, `throw` signals errors, and `catch` handles them.  
- It prevents abrupt program termination and ensures smooth execution.  
- Multiple exceptions can be handled using multiple catch blocks.  
- Real-life applications include file operations, memory management, invalid input handling, and custom error scenarios.  
- Exception handling improves program robustness, reliability, and user experience.  
- It is an essential concept for writing professional-quality, maintainable C++ programs.
