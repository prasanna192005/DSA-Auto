# Solutions for Analyzing Array Operations: Best, Worst, and Average Case

### Approach

The problem involves finding the maximum element in an unsorted array. A simple linear scan approach is used: we iterate through the array, keeping track of the maximum element encountered so far.  The best-case scenario occurs when the maximum element is the first element (O(1)).  The worst-case scenario occurs when the maximum element is the last element (O(n)). The average-case scenario is O(n) as well, since on average we would expect to check roughly half of the array elements.

## C Solution
c
#include <stdio.h>
#include <limits.h>

int findMax(int arr[], int size) {
    int max = INT_MIN; 
    for (int i = 0; i < size; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}

int main() {
    int arr[] = {3, 1, 4, 1, 5, 9, 2, 6};
    int size = sizeof(arr) / sizeof(arr[0]);
    int max = findMax(arr, size);
    printf("%d\n", max);
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <limits>

int findMax(int arr[], int size) {
    int max = std::numeric_limits<int>::min();
    for (int i = 0; i < size; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}

int main() {
    int arr[] = {3, 1, 4, 1, 5, 9, 2, 6};
    int size = sizeof(arr) / sizeof(arr[0]);
    int max = findMax(arr, size);
    std::cout << max << std::endl;
    return 0;
}


## Java Solution
java
import java.util.Arrays;

public class Main {
    public static int findMax(int[] arr) {
        int max = Integer.MIN_VALUE;
        for (int num : arr) {
            if (num > max) {
                max = num;
            }
        }
        return max;
    }

    public static void main(String[] args) {
        int[] arr = {3, 1, 4, 1, 5, 9, 2, 6};
        int max = findMax(arr);
        System.out.println(max);
    }
}


## Python Solution
python
def findMax(arr):
    max_num = float('-inf')
    for num in arr:
        if num > max_num:
            max_num = num
    return max_num

if __name__ == "__main__":
    arr = [3, 1, 4, 1, 5, 9, 2, 6]
    max_num = findMax(arr)
    print(max_num)


## JavaScript Solution
javascript
function findMax(arr) {
  let max = -Infinity;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i];
    }
  }
  return max;
}

const arr = [3, 1, 4, 1, 5, 9, 2, 6];
const max = findMax(arr);
console.log(max);
