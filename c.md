## Hello, World! in C

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```
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
