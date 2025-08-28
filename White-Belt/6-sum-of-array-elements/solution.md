# Approach

The approach is straightforward. We iterate through the array, adding each element to a running sum.  The final sum is then returned.

**C++**
cpp
#include <iostream>
#include <vector>

int sumArray(std::vector<int> arr) {
  int sum = 0;
  for (int i = 0; i < arr.size(); i++) {
    sum += arr[i];
  }
  return sum;
}

int main() {
  std::vector<int> arr = {1, 2, 3, 4, 5};
  std::cout << sumArray(arr) << std::endl; // Output: 15
  return 0;
}


**Java**
java
import java.util.Arrays;

class Solution {
    public int sumArray(int[] arr) {
        int sum = 0;
        for (int i = 0; i < arr.length; i++) {
            sum += arr[i];
        }
        return sum;
    }
    public static void main(String[] args) {
        Solution sol = new Solution();
        int[] arr = {1, 2, 3, 4, 5};
        System.out.println(sol.sumArray(arr)); // Output: 15
    }
}


**Python**
python
def sum_array(arr):
  sum = 0
  for i in range(len(arr)):
    sum += arr[i]
  return sum

arr = [1, 2, 3, 4, 5]
print(sum_array(arr)) # Output: 15


**JavaScript**
javascript
function sumArray(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum;
}

let arr = [1, 2, 3, 4, 5];
console.log(sumArray(arr)); // Output: 15
