# Solutions for Swap Two Variables

### Approach
This problem can be solved using the addition and subtraction operators.  We add the two numbers, then subtract one from the sum to get the other. This effectively swaps their values without needing an extra variable.

## C Solution
c
#include <stdio.h>

int main() {
    int a, b;
    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);

    a = a + b;
    b = a - b;
    a = a - b;

    printf("After swapping: a = %d, b = %d\n", a, b);
    return 0;
}


## C++ Solution
cpp
#include <iostream>

int main() {
    int a, b;
    std::cout << "Enter two integers: ";
    std::cin >> a >> b;

    a = a + b;
    b = a - b;
    a = a - b;

    std::cout << "After swapping: a = " << a << ", b = " << b << std::endl;
    return 0;
}


## Java Solution
java
import java.util.Scanner;

public class SwapVariables {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter two integers: ");
        int a = scanner.nextInt();
        int b = scanner.nextInt();

        a = a + b;
        b = a - b;
        a = a - b;

        System.out.println("After swapping: a = " + a + ", b = " + b);
        scanner.close();
    }
}


### Python Solution
python
a, b = map(int, input("Enter two integers: ").split())

a = a + b
b = a - b
a = a - b

print(f"After swapping: a = {a}, b = {b}")


## JavaScript Solution
javascript
const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout,
});

readline.question('Enter two integers: ', (input) => {
    const [a, b] = input.split(' ').map(Number);

    let temp = a;
    a = b;
    b = temp; //Using a temp variable for demonstration purposes.  The approach above works as well.

    console.log(`After swapping: a = ${a}, b = ${b}`);
    readline.close();
});
