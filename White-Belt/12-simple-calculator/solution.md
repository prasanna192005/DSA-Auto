# Solutions for Simple Calculator

### Approach
This problem is solved by reading three inputs from the user: two integers (operands) and a character representing the arithmetic operator.  A switch statement (or equivalent) is used to select the appropriate arithmetic operation based on the operator.  Error handling is implemented to prevent division by zero.

## C Solution
c
#include <stdio.h>

int main() {
    int a, b, result;
    char operator;

    printf("Enter two integers: ");
    scanf("%d %d", &a, &b);
    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator); // Note the space before %c to consume any leftover newline

    switch (operator) {
        case '+':
            result = a + b;
            printf("%d\n", result);
            break;
        case '-':
            result = a - b;
            printf("%d\n", result);
            break;
        case '*':
            result = a * b;
            printf("%d\n", result);
            break;
        case '/':
            if (b == 0) {
                printf("Division by zero error!\n");
            } else {
                result = a / b;
                printf("%d\n", result);
            }
            break;
        default:
            printf("Invalid operator!\n");
    }

    return 0;
}


## C++ Solution
cpp
#include <iostream>

using namespace std;

int main() {
    int a, b, result;
    char op;

    cout << "Enter two integers: ";
    cin >> a >> b;
    cout << "Enter an operator (+, -, *, /): ";
    cin >> op;

    switch (op) {
        case '+':
            result = a + b;
            cout << result << endl;
            break;
        case '-':
            result = a - b;
            cout << result << endl;
            break;
        case '*':
            result = a * b;
            cout << result << endl;
            break;
        case '/':
            if (b == 0) {
                cout << "Division by zero error!" << endl;
            } else {
                result = a / b;
                cout << result << endl;
            }
            break;
        default:
            cout << "Invalid operator!" << endl;
    }

    return 0;
}


## Java Solution
java
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        int a, b, result;
        char operator;

        System.out.print("Enter two integers: ");
        a = input.nextInt();
        b = input.nextInt();
        System.out.print("Enter an operator (+, -, *, /): ");
        operator = input.next().charAt(0);

        switch (operator) {
            case '+':
                result = a + b;
                System.out.println(result);
                break;
            case '-':
                result = a - b;
                System.out.println(result);
                break;
            case '*':
                result = a * b;
                System.out.println(result);
                break;
            case '/':
                if (b == 0) {
                    System.out.println("Division by zero error!");
                } else {
                    result = a / b;
                    System.out.println(result);
                }
                break;
            default:
                System.out.println("Invalid operator!");
        }
        input.close();
    }
}


## Python Solution
python
a, b = map(int, input().split())
op = input()

if op == '+':
    print(a + b)
elif op == '-':
    print(a - b)
elif op == '*':
    print(a * b)
elif op == '/':
    if b == 0:
        print("Division by zero error!")
    else:
        print(a // b) # Integer division
else:
    print("Invalid operator!")


## JavaScript Solution
javascript
const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout,
});

readline.question('Enter two integers: ', (input) => {
    const [a, b] = input.split(' ').map(Number);
    readline.question('Enter an operator (+, -, *, /): ', (op) => {
        let result;
        switch (op) {
            case '+':
                result = a + b;
                break;
            case '-':
                result = a - b;
                break;
            case '*':
                result = a * b;
                break;
            case '/':
                if (b === 0) {
                    console.log('Division by zero error!');
                    readline.close();
                    return;
                }
                result = Math.floor(a / b); //Integer division
                break;
            default:
                console.log('Invalid operator!');
                readline.close();
                return;
        }
        console.log(result);
        readline.close();
    });
});
