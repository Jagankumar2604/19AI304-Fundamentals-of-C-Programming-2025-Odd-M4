# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
## 7. Implementation of Functions.
## 8. Implementation of passing parameters.
# Ex.No:16
  Implement a C program to read a date in the format DD/MM/YYYY and determine whether the entered date is valid. The program should check the correctness of the day, month, and year, including leap year calculations for February.
# Date : 
# Aim:
 To implement a C program that validates a user-entered date using a function without parameters and without return value, ensuring the correctness of day, month, year, and leap year conditions.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3:
### Call the function `validateDate()`.
### Inside `validateDate()` function:
### Step 4: 
  Declare variables `dd`, `mm`, and `yy`.
### Step 5: 
  Ask the user to enter a date in `DD/MM/YYYY` format.
### Step 6: 
  Read the date values using `scanf`.
### Step 7: 
  Check if the year is between **1900 and 9999**.
 - If the year is invalid, display **"Year is not valid"** and stop further checks.
### Step 8: 
  Check if the month is between **1 and 12**.
- If the month is invalid, display **"Month is not valid"** and stop further checks.
### Step 9: 
  If the month has **31 days**, check if the day is between **1 and 31**.
### Step 10: 
  If the month has **30 days**, check if the day is between **1 and 30**.
### Step 11: 
  If the month is **February**:
  - Check if the day is between **1 and 28**, or if the day is **29**, verify if it's a **leap year**.
### Step 12: 
  If any valid condition is satisfied, display **"Date is valid."**
### Step 13: 
  Otherwise, display **"Date is invalid."**
### Step 14: 
  Stop
# Program:
```
#include <stdio.h>

int main()
{
    int d, m, y, maxDays;

    scanf("%d/%d/%d", &d, &m, &y);

    if(m == 2)
    {
        if((y % 400 == 0) || (y % 4 == 0 && y % 100 != 0))
            maxDays = 29;
        else
            maxDays = 28;
    }
    else if(m == 4 || m == 6 || m == 9 || m == 11)
        maxDays = 30;
    else if(m >= 1 && m <= 12)
        maxDays = 31;
    else
        maxDays = 0;

    if(d >= 1 && d <= maxDays)
        printf("Valid Date");
    else
        printf("Invalid Date");

    return 0;
}
```
# Output:
<img width="237" height="221" alt="image" src="https://github.com/user-attachments/assets/f97ac926-9448-4878-8fb4-a633b7fa833b" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:17
  Develop a C program to read two numbers from the user and determine the maximum and minimum values. Use user-defined functions with arguments and return values—one function to find the maximum (max()) and another to find the minimum (min()).
# Date : 
# Aim:
 To develop a C program that uses functions with parameters and return values to compute and display the maximum and minimum of two user-entered numbers.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.
### Step 3: 
  Declare variables `num1`, `num2`, `maximum`, and `minimum`.
### Step 4: 
  Ask the user to enter two numbers.
### Step 5: 
  Read the numbers using `scanf`.
### Step 6: 
  Call the function `max(num1, num2)`.
### Step 7: 
  Inside function `max(num1, num2)`:
- **Step 7.1:** Receive two integer arguments.  
- **Step 7.2:** Compare the two numbers.  
- **Step 7.3:** If `num1 > num2`, return `num1`.  
- **Step 7.4:** Otherwise, return `num2`.
### Step 8: 
  Store the returned value in `maximum`.
### Step 9: 
  Call the function `min(num1, num2)`.
### Step 10: 
  Inside function `min(num1, num2)`:
- **Step 10.1:** Receive two integer arguments.  
- **Step 10.2:** Compare the two numbers.  
- **Step 10.3:** If `num1 > num2`, return `num2`.  
- **Step 10.4:** Otherwise, return `num1`.
### Step 11: 
  Store the returned value in `minimum`.
### Step 12: 
  Display the returned maximum and minimum values.
### Step 13: 
  Stop
# Program:
```
#include <stdio.h>

int max(int a, int b)
{
    return (a > b) ? a : b;
}

int min(int a, int b)
{
    return (a < b) ? a : b;
}

int main()
{
    int n1, n2;

    printf("Enter two numbers: ");
    scanf("%d%d", &n1, &n2);

    printf("Maximum = %d\n", max(n1, n2));
    printf("Minimum = %d\n", min(n1, n2));

    return 0;
}
```
# Output:
<img width="290" height="112" alt="image" src="https://github.com/user-attachments/assets/69a8474a-4b21-4046-a1ba-f822c5097dc6" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.



# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:18
  Develop a C program to convert temperatures between Celsius and Fahrenheit: Convert Celsius to Fahrenheit using a function that returns the converted value. Convert Fahrenheit to Celsius using another function that returns the converted value. Display the results in the main() function.
# Date : 
# Aim:
 To develop a C program that converts temperatures between Celsius and Fahrenheit using functions with return values.
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.  
### Step 3:
 Declare function prototypes:
 - `float celtof();`  
 - `float ftocel();`
### Step 4: 
  Enter the `main()` function.
### Step 5:
  Call the `celtof()` function to convert Celsius to Fahrenheit.
### Step 6: 
  Inside `celtof()` function:
 - Declare float variables `C` and `F`.  
 - Display the message: **"Enter the temperature in Celsius"**.  
 - Read the value of `C` from the user.  
 - Calculate Fahrenheit using the formula: `F = (C * 9 / 5) + 32`.  
 - Return `F` to `main()`.
### Step 7: 
  Print the returned Fahrenheit value in `main()`.
### Step 8: 
  Call the `ftocel()` function to convert Fahrenheit to Celsius.
### Step 9: 
  Inside `ftocel()` function:
 - Declare float variables `f` and `celsius`.  
 - Display the message: **"Enter the temperature in Fahrenheit"**.  
 - Read the value of `f` from the user.  
 - Calculate Celsius using the formula: `celsius = (f - 32) * 5 / 9`.  
 - Return `celsius` to `main()`.
### Step 10: 
 Print the returned Celsius value in `main()`.
### Step 11: 
 Stop
# Program:
```
#include <stdio.h>

float ctof(float c)
{
    return (c * 9 / 5) + 32;
}

float ftoc(float f)
{
    return (f - 32) * 5 / 9;
}

int main()
{
    float c, f;

    printf("Enter temperature in Celsius: ");
    scanf("%f", &c);

    printf("Enter temperature in Fahrenheit: ");
    scanf("%f", &f);

    printf("\n%.2f Celsius = %.2f Fahrenheit\n", c, ctof(c));
    printf("%.2f Fahrenheit = %.2f Celsius\n", f, ftoc(f));

    return 0;
}
```
# Output:
<img width="412" height="152" alt="image" src="https://github.com/user-attachments/assets/ac6ede4f-ab4f-4f3a-b0db-d181c50d51fb" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.


 
# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:19
  Build a C program to print the elements of a given 4×4 matrix in spiral order starting from the top-left element and moving clockwise,using a user-defined parameterized function without return spiralPrint().
# Date : 
# Aim:
 To build a C program to display the elements of a 2D array in spiral form, traversing the outer elements first and then moving inward in a clockwise direction, using a user-defined parameterized function without return spiralPrint().
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.  
### Step 3: 
  Define constants `R` and `C` for the number of rows and columns in the matrix.
### Step 4: 
  Declare a function `spiralPrint(int m, int n, int a[R][C])` to print the matrix in spiral order.
### Step 5: 
  Inside `spiralPrint()` function:
 - Initialize variables:  
   - `k = 0` → starting row index  
   - `l = 0` → starting column index  
   - `m` → ending row index  
   - `n` → ending column index  
 - Repeat the following while `k < m` and `l < n`:
   - a. **Print the top row from left to right**:  
     - Loop from column `l` to `n-1` and print `a[k][i]`.  
     - Increment `k`.       
   - b. **Print the last column from top to bottom**:  
     - Loop from row `k` to `m-1` and print `a[i][n-1]`.  
     - Decrement `n`.       
   - c. **If `k < m`, print the bottom row from right to left**:  
     - Loop from column `n-1` to `l` and print `a[m-1][i]`.  
     - Decrement `m`.       
   - d. **If `l < n`, print the first column from bottom to top**:  
     - Loop from row `m-1` to `k` and print `a[i][l]`.  
     - Increment `l`.
### Step 6: 
  In the `main()` function:
- Declare and initialize a 4×4 matrix `a`.  
- Call `spiralPrint(R, C, a)` to print the elements in spiral order.
### Step 7: 
  Stop
# Program:
```
#include <stdio.h>

int main()
{
    int a[4][4], i, t=0, b=3, l=0, r=3;

    for(i=0;i<4;i++)
        for(int j=0;j<4;j++)
            scanf("%d",&a[i][j]);

    while(t<=b && l<=r)
    {
        for(i=l;i<=r;i++) printf("%d ",a[t][i]);
        t++;

        for(i=t;i<=b;i++) printf("%d ",a[i][r]);
        r--;

        for(i=r;i>=l;i--) printf("%d ",a[b][i]);
        b--;

        for(i=b;i>=t;i--) printf("%d ",a[i][l]);
        l++;
    }

    return 0;
}
```
# Output:
<img width="517" height="52" alt="image" src="https://github.com/user-attachments/assets/869899a5-64fe-4be3-9049-eeb5022df35b" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.



# 19AI304-Fundamentals-of-C-Programming-2025-Odd-M4
# IAPR-4- Module 4 - FoC
# Ex.No:20
  Build a C program to convert a string such that the first and last characters, as well as the characters before and after each space, are converted to uppercase. Implement this using a user-defined parameterized function without return.
# Date : 
# Aim:
To build a C program to convert a string as described above, using a user-defined parameterized function without return convertFirstCLastC(char str[]).
# Algorithm:
### Step 1:
  Start
### Step 2: 
  Include the standard input-output library: #include<stdio.h>.  
### Step 3: 
  Declare a user-defined void function `convertFirstCLastC(char str[])` that takes the string as a parameter.
### Step 4: 
 Inside `convertFirstCLastC(char str[])` function:
 - Find the length of the string `len`.  
 - Convert the first character `str[0]` to uppercase.  
 - Loop through the string from index `1` to `len-2`:  
   - If a character is a space, capitalize the character before and after it.  
 - Convert the last character `str[len-1]` to uppercase.
### Step 5: 
 In `main()` function:
 - Declare a string `str[100]`.  
 - Read the input string from the user.  
 - Call the function `convertFirstCLastC(char str[])`.  
 - Print the modified string.
### Step 6: 
 Stop
# Program:
```
#include <stdio.h>
#include <ctype.h>
#include <string.h>

void convert(char s[])
{
    int i, n = strlen(s);

    s[0] = toupper(s[0]);
    s[n-1] = toupper(s[n-1]);

    for(i = 1; s[i]; i++)
        if(s[i]==' ')
            s[i-1]=toupper(s[i-1]), s[i+1]=toupper(s[i+1]);

    printf("%s", s);
}

int main()
{
    char s[100];

    fgets(s, 100, stdin);
    s[strcspn(s, "\n")] = 0;

    convert(s);

    return 0;
}
```
# Output:
<img width="323" height="243" alt="image" src="https://github.com/user-attachments/assets/f0b0f576-b558-4d4d-b679-168c972f0606" />

# Result: 
Thus, the program was implemented and executed successfully, and the required output was obtained.

