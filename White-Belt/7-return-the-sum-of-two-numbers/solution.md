# Solutions for Return the Sum of Two Numbers

## C Solution
c
#include <stdio.h>

int sum(int a, int b) {
  return a + b;
}

int main() {
  int a = 5, b = 3;
  int result = sum(a, b);
  printf("Sum: %d\n", result);
  return 0;
}


## C++ Solution
cpp
#include <iostream>

int sum(int a, int b) {
  return a + b;
}

int main() {
  int a = 5, b = 3;
  int result = sum(a, b);
  std::cout << "Sum: " << result << std::endl;
  return 0;
}


## Java Solution
java
class Solution {
    public int sum(int a, int b) {
        return a + b;
    }
    public static void main(String[] args) {
        Solution sol = new Solution();
        int a = 5, b = 3;
        int result = sol.sum(a, b);
        System.out.println("Sum: " + result);
    }
}


## Python Solution
python
def sum(a, b):
  return a + b

a = 5
b = 3
result = sum(a, b)
print(f"Sum: {result}")


## JavaScript Solution
javascript
function sum(a, b) {
  return a + b;
}

let a = 5, b = 3;
let result = sum(a, b);
console.log("Sum: " + result);
