# Uninitialized Property Access in C#

This repository demonstrates a common error in C#: accessing a property of a class before it has been initialized. This can lead to unpredictable behavior or exceptions.

The `bug.cs` file contains the code with the error. The `bugSolution.cs` shows how to correctly initialize the property to avoid this issue.

## How to Reproduce
1. Clone this repository.
2. Open `bug.cs` in a C# IDE.
3. Run the `MyMethod()` function.  Observe the potential default value.
4. Open `bugSolution.cs` and see how the property is initialized before access.

## Key Points
* Always initialize properties, especially when dealing with value types (like `int`), to avoid unexpected values.
* Using constructor initialization or setting the value explicitly before accessing the property ensures predictable behavior. 
* Consider using nullable types (`int?`) if the property can legitimately be uninitialized.