# Find the GCD - Solution

**Approach:**

We'll use the Euclidean algorithm, which is an efficient method for computing the greatest common divisor (GCD) of two integers. The algorithm is based on the principle that the GCD of two numbers does not change if the larger number is replaced by its difference with the smaller number. This process is repeated until the two numbers are equal, which is the GCD.

**Code:**

cpp
// C++
#include <iostream>

int gcd(int a, int b) {
  if (b == 0) {
    return a;
  }
  return gcd(b, a % b);
}

int main() {
  int a, b;
  std::cin >> a >> b;
  std::cout << gcd(a, b) << std::endl;
  return 0;
}


java
// Java
import java.util.Scanner;

public class GCD {
    public static int gcd(int a, int b) {
        if (b == 0) {
            return a;
        }
        return gcd(b, a % b);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        System.out.println(gcd(a, b));
        scanner.close();
    }
}


python
# Python
def gcd(a, b):
    if b == 0:
        return a
    return gcd(b, a % b)

a, b = map(int, input().split())
print(gcd(a, b))


javascript
// JavaScript
function gcd(a, b) {
  if (b === 0) {
    return a;
  }
  return gcd(b, a % b);
}

const [a, b] = process.argv.slice(2).map(Number);
console.log(gcd(a, b));
