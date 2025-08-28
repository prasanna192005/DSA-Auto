# Solution

**Approach:**

The solution directly uses the modulo operator (`%`) provided by most programming languages. This operator returns the remainder of the division.  We handle potential errors (like division by zero, though constraints prevent this in the problem description) gracefully though error checking is unnecessary given the constraints.

**C++:**
cpp
#include <iostream>

int modulo(int a, int b) {
  //Error handling is not needed given the problem constraints.
  return a % b;
}

int main() {
  std::cout << modulo(10, 3) << std::endl; // Output: 1
  std::cout << modulo(17, 5) << std::endl; // Output: 2
  return 0;
}


**Java:**
java
class Solution {
    public int modulo(int a, int b) {
        //Error handling is not needed given the problem constraints.
        return a % b;
    }
    public static void main(String[] args) {
        Solution sol = new Solution();
        System.out.println(sol.modulo(10, 3)); // Output: 1
        System.out.println(sol.modulo(17, 5)); // Output: 2
    }
}


**Python:**
python
def modulo(a, b):
    #Error handling is not needed given the problem constraints.
    return a % b

print(modulo(10, 3))  # Output: 1
print(modulo(17, 5))  # Output: 2


**JavaScript:**
javascript
function modulo(a, b) {
  //Error handling is not needed given the problem constraints.
  return a % b;
}

console.log(modulo(10, 3)); // Output: 1
console.log(modulo(17, 5)); // Output: 2
