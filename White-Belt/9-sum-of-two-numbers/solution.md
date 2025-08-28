# Solutions for Sum of Two Numbers

### Approach
This problem is straightforward.  We simply add the two input integers together and return the result. No special data structures or algorithms are needed.

## C Solution
c
#include <stdio.h>

int sum(int a, int b) {
  return a + b;
}

int main() {
  int num1, num2;
  scanf("%d %d", &num1, &num2);
  printf("%d\n", sum(num1, num2));
  return 0;
}


## C++ Solution
cpp
#include <iostream>

int sum(int a, int b) {
  return a + b;
}

int main() {
  int num1, num2;
  std::cin >> num1 >> num2;
  std::cout << sum(num1, num2) << std::endl;
  return 0;
}


## Java Solution
java
import java.util.*;
public class Main {
    public static int sum(int a, int b) {
        return a + b;
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num1 = scanner.nextInt();
        int num2 = scanner.nextInt();
        System.out.println(sum(num1, num2));
        scanner.close();
    }
}


## Python Solution
python
def sum(a, b):
  return a + b

num1, num2 = map(int, input().split())
print(sum(num1, num2))


## JavaScript Solution
javascript
const readline = require('readline');
const rl = readline.createInterface({ input: process.stdin, output: process.stdout });

function sum(a, b) {
  return a + b;
}

rl.on('line', (line) => {
  const [num1, num2] = line.split(' ').map(Number);
  console.log(sum(num1, num2));
  rl.close();
});
