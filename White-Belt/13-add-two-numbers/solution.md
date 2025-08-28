### Solutions for Add Two Numbers

### Approach
This problem is straightforward.  We simply add the two input integers together and return the result. No complex data structures or algorithms are needed. 

## C Solution
c
#include <stdio.h>

int addNumbers(int num1, int num2) {
  return num1 + num2;
}

int main() {
  int num1, num2;
  scanf("%d %d", &num1, &num2);
  printf("%d\n", addNumbers(num1, num2));
  return 0;
}


## C++ Solution
cpp
#include <iostream>

int addNumbers(int num1, int num2) {
  return num1 + num2;
}

int main() {
  int num1, num2;
  std::cin >> num1 >> num2;
  std::cout << addNumbers(num1, num2) << std::endl;
  return 0;
}


## Java Solution
java
import java.util.Scanner;

public class AddTwoNumbers {

    public static int addNumbers(int num1, int num2) {
        return num1 + num2;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        System.out.println(addNumbers(num1, num2));
        scanner.close();
    }
}


## Python Solution
python
def add_numbers(num1, num2):
    return num1 + num2

num1, num2 = map(int, input().split())
print(add_numbers(num1, num2))


## JavaScript Solution
javascript
const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout,
});

function addNumbers(num1, num2) {
    return num1 + num2;
}

readline.question('Enter two numbers separated by space: ', (input) => {
    const [num1, num2] = input.split(' ').map(Number);
    console.log(addNumbers(num1, num2));
    readline.close();
});
