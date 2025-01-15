## Hello, World! in C

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

## Summation of Two Numbers in C

```c
#include <stdio.h>

int main() {
    int num1, num2, sum;

    printf("Enter the first number: ");
    scanf("%d", &num1);
    printf("Enter the second number: ");
    scanf("%d", &num2);

    sum = num1 + num2;

    printf("The sum of %d and %d is: %d\n", num1, num2, sum);

    return 0;
}
```

## Subtraction of Two Numbers in C

```c
#include <stdio.h>

int main() {
    int num1, num2, sub;

    printf("Enter the first number: ");
    scanf("%d", &num1);
    printf("Enter the second number: ");
    scanf("%d", &num2);

    sub = num1 - num2;

    printf("The subtraction of %d and %d is: %d\n", num1, num2, sub);

    return 0;
}
```

## Multiplication of Two Numbers (using function) in C

```c
#include <stdio.h>
float multiply(float x, float y);

int main() {
    
    float a, b, mul;
    
    printf("Enter your first value: ");
    scanf("%f", &a);
    
    printf("Enter your second value: ");
    scanf("%f", &b);
    
    mul = multiply(a, b);
    
    printf("Multiplication of %f & %f is %.2f (in 2 dec. place)", a, b, mul);

    return 0;
}

float multiply(float x, float y){
    float result;
    
    result = x * y;
    
    return result;
}
```

## Division of Two Numbers (using function) in C

```c
#include <stdio.h>
float divide(float x, float y);

int main() {
    
    float a, b, div;
    
    printf("Enter your first value: ");
    scanf("%f", &a);
    
    printf("Enter your second value: ");
    scanf("%f", &b);
    
    div = divide(a, b);
    
    printf("Division of %f & %f is %.2f (in 2 dec. place)", a, b, div);

    return 0;
}

float divide(float x, float y){
    float result;
    
    result = x / y;
    
    return result;
}
```

## Remainder of a number in C

```c
#include <stdio.h>

int main() {
    int dividend, divisor, remainder;

    // Input the dividend and divisor
    printf("Enter the dividend: ");
    scanf("%d", &dividend);

    printf("Enter the divisor: ");
    scanf("%d", &divisor);

    // Calculate remainder
    remainder = dividend % divisor;

    // Display the result
    printf("The remainder when %d is divided by %d is: %d\n", dividend, divisor, remainder);

    return 0;
}
```

## Basic calculator in C

```c
#include <stdio.h>

double add(double a, double b) {
    return a + b;
}

double subtract(double a, double b) {
    return a - b;
}

double multiply(double a, double b) {
    return a * b;
}

double divide(double a, double b) {
    if (b != 0) {
        return a / b;
    }
    printf("Error: Division by zero\n");
    return 0;
}

int main() {
    double num1, num2, result;
    char operator;

    printf("Enter first number: ");
    scanf("%lf", &num1);
    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);
    printf("Enter second number: ");
    scanf("%lf", &num2);

    switch (operator) {
        case '+':
            result = add(num1, num2);
            break;
        case '-':
            result = subtract(num1, num2);
            break;
        case '*':
            result = multiply(num1, num2);
            break;
        case '/':
            result = divide(num1, num2);
            if (num2 == 0) return 1;
            break;
        default:
            printf("Error: Invalid operator\n");
            return 1;
    }

    printf("Result: %.2lf\n", result);
    return 0;
}
```
