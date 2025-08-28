# Recursive Factorial Solution

**Approach:**
The factorial of a number can be recursively defined as follows:
* If n is 0, then n! = 1 (base case).
* If n is greater than 0, then n! = n * (n-1)!

We use this recursive definition to create our function. The base case stops the recursion when n becomes 0. Otherwise, the function calls itself with a smaller value of n.

**Code:**

**C++:**
cpp
#include <iostream>

long long factorial(int n) {
  if (n == 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

int main() {
  int n;
  std::cin >> n;
  std::cout << factorial(n) << std::endl;
  return 0;
}


**Java:**
java
class Solution {
    public long factorial(int n) {
        if (n == 0) {
            return 1;
        } else {
            return n * factorial(n - 1);
        }
    }

    public static void main(String[] args) {
        Solution sol = new Solution();
        java.util.Scanner scanner = new java.util.Scanner(System.in);
        int n = scanner.nextInt();
        System.out.println(sol.factorial(n));
        scanner.close();
    }
}


**Python:**
python
def factorial(n):
  if n == 0:
    return 1
  else:
    return n * factorial(n - 1)

n = int(input())
print(factorial(n))


**JavaScript:**
javascript
function factorial(n) {
  if (n === 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

let n = parseInt(prompt());
console.log(factorial(n));
