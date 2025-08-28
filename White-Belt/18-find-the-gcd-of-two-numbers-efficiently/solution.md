# Solutions for Find the GCD of Two Numbers Efficiently

### Approach

The solution employs the Euclidean algorithm to efficiently compute the GCD of two non-negative integers. The Euclidean algorithm is based on the principle that the GCD of two numbers does not change if the smaller number is subtracted from the larger number. This process is repeated until one of the numbers becomes zero, at which point the other number is the GCD.  The time complexity is O(log(min(a, b))), which is very efficient even for large numbers. The space complexity is O(1) as it uses only a few variables.

## C Solution
c
#include <stdio.h>

int gcd(int a, int b) {
    while (b) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int main() {
    int num1, num2;
    scanf("%d %d", &num1, &num2);
    printf("%d\n", gcd(num1, num2));
    return 0;
}


## C++ Solution
cpp
#include <iostream>

int gcd(int a, int b) {
    while (b) {
        int temp = b;
        b = a % b;
        a = temp;
    }
    return a;
}

int main() {
    int num1, num2;
    std::cin >> num1 >> num2;
    std::cout << gcd(num1, num2) << std::endl;
    return 0;
}


## Java Solution
java
import java.util.Scanner;

public class GCD {
    public static int gcd(int a, int b) {
        while (b != 0) {
            int temp = b;
            b = a % b;
            a = temp;
        }
        return a;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        System.out.println(gcd(num1, num2));
        scanner.close();
    }
}


## Python Solution
python
def gcd(a, b):
    while b:
        a, b = b, a % b
    return a

if __name__ == "__main__":
    num1, num2 = map(int, input().split())
    print(gcd(num1, num2))


## JavaScript Solution
javascript
function gcd(a, b) {
  while (b) {
    let temp = b;
    b = a % b;
    a = temp;
  }
  return a;
}

const readline = require('readline');
const rl = readline.createInterface({ input: process.stdin, output: process.stdout });
rl.on('line', (line) => {
  const [num1, num2] = line.split(' ').map(Number);
  console.log(gcd(num1, num2));
  rl.close();
});
