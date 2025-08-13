# Exp10-Call-By-

## Aim

To learn about call by reference and call by value.

## Apparatus-
   Programiz

## Theory:

## Call By Value

 Call by Value is a method of passing arguments to a function where a copy of the variable’s value is given to the function.

Key points:

1.The function works on its own copy of the data.

2.Changes made inside the function do not affect the original variable.

3.Memory-wise: the original variable and the function parameter are stored in different memory locations.

4.Copy is passed – The actual value of the argument is copied into the function’s parameter.

5.Original is safe – Changes inside the function do not affect the original variable.

6.Separate memory – The parameter and the original variable are stored in different memory locations.

7.Good for safety – Useful when you don’t want the function to accidentally change your data.

8.Overhead for large data – For big objects/arrays, copying can be slower and use more memory.

9.Default method in C/C++ – If you don’t use pointers or references, parameters are passed by value by default.

10.Cannot return multiple results directly – Since it only has a copy, the function can’t modify multiple original variables unless you return them explicitly.

11.Immutable in effect – The function works as if the parameter were read-only (even if you modify the copy).

## Call By Reference

1.Reference is passed – The function gets the memory address of the original variable, not a copy.

2.Direct effect – Changes made in the function affect the original variable.

3.Same memory location – Parameter and argument refer to the same storage in memory.

4.Faster for large data – No copying needed, so it’s more efficient for big structures or arrays.

5.Can return multiple results – Since you can modify the originals, you can change several variables at once.

6.Risk of unintended changes – If not careful, the function may accidentally overwrite important data.

7.Implemented in C++ using references (&) or pointers (*) – C only supports it via pointers.


| Feature | Call by Value | Call by Reference |
|---------|--------------|-------------------|
| **What is passed** | Copy of the actual value | Memory address (reference) of the actual value |
| **Effect on original variable** | No change in the original variable | Changes affect the original variable |
| **Memory location** | Function parameter stored separately | Function parameter refers to the same memory location as the argument |
| **Performance** | Slower for large data (copying overhead) | Faster for large data (no copying) |
| **Safety** | Safer – original data is protected | Risky – original data can be changed unintentionally |
| **Multiple return values** | Not possible directly | Possible, since you can modify multiple variables |
| **Implementation in C++** | Default method (no `&` or `*` needed) | Use references (`&`) or pointers (`*`) |
| **Usage in C** | Supported directly | Only possible using pointers |

## Program 1

## Algorithm

1. **Start**
2. Initialize two integers:
   - `a = 5`
   - `b = 10`
3. Call the function `swap(a, b)`:
   - Inside the function:
     1. Store `x` in a temporary variable `temp`.
     2. Assign the value of `y` to `x`.
     3. Assign the value of `temp` to `y`.
   - **Note:** This uses *Call by Value*, so only copies of `a` and `b` are swapped; originals remain unchanged.
4. Display `a` and `b` in the main function.
5. **Stop**

## Program 2:

## Algorithm

1. **Start**
2. Initialize two integers:
   - `a = 5`
   - `b = 10`
3. Call the function `swap(&a, &b)`:
   - Inside the function:
     1. Store the value pointed to by `x` in a temporary variable `temp`.
     2. Assign the value pointed to by `y` to the location pointed to by `x`.
     3. Assign the value of `temp` to the location pointed to by `y`.
   - **Note:** This uses *Call by Reference* (via pointers), so the original `a` and `b` in `main` are swapped.
4. Display `a` and `b` in the main function.
5. **Stop**

## Program 3:

## Algorithm

1. **Start**
2. Initialize two integers:
   - `a = 5`
   - `b = 10`
3. Call the function `swap(a, b)`:
   - Inside the function:
     1. Store the value of `x` in a temporary variable `temp`.
     2. Assign the value of `y` to `x`.
     3. Assign the value of `temp` to `y`.
   - **Note:** This uses *Call by Reference* (via C++ references), so the original `a` and `b` in `main` are swapped.
4. Display `a` and `b` in the main function.
5. **Stop**

## Program 4:

## Algorithm

1. **Start**
2. Input the employee’s salary.
3. Input the following details:
   - Number of Research Projects (`proj`)
   - Number of Research Publications (`pub`)
   - Profit (`prof`)
   - Number of New Projects (`new_proj`)
4. **Check the increment condition**:
   - If at least **three out of four** criteria are satisfied (combinations checked in the `if` statement), then:
     - Call `increment_ref(salary)` → salary is increased by 20%.
     - Display the new salary.
   - Else:
     - Call `increment_val(salary)` → only a copy of salary is changed, original salary remains the same.
     - Display the unchanged salary with the message **"No increment!"**.
5. **Stop**

## Program 5

## Algorithm

## Algorithm

1. **Start**
2. Initialize two integer arrays:
   - `arr = {1, 2, 3, 4, 5}`
   - `arr1 = {2, 4, 6, 8, 10}`
3. Display **"Initial Array"** by printing all elements of `arr`.
4. For each index `i` from 0 to 4:
   - Call the function `change_val(arr[i], arr1[i])`:
     - Inside the function:
       1. Assign the value `val` to `x` (reference to `arr[i]`).
       2. This changes the original element in `arr` to `arr1[i]`.
5. Display **"Changed Array"** by printing all updated elements of `arr`.
6. **Stop**









