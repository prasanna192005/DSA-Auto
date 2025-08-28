# Solutions for Linear Search Best/Worst/Average Case

### Approach
This problem is solved using a simple linear search algorithm. The algorithm iterates through the array, comparing each element to the target.  
The best-case scenario occurs when the target is the first element (O(1)). The worst-case occurs when the target is the last element or not present (O(n)). The average-case scenario is also O(n), as the average number of comparisons is proportional to the array size.

## C Solution
c
#include <stdio.h>

int main() {
    int arr[] = {5, 2, 8, 1, 9, 4, 7, 3, 6};
    int target = 8;
    int n = sizeof(arr) / sizeof(arr[0]);
    int index = -1;

    for (int i = 0; i < n; i++) {
        if (arr[i] == target) {
            index = i;
            break;
        }
    }

    if (index != -1) {
        printf("Index: %d\n", index);
    } else {
        printf("Target not found\n");
    }
    printf("Best-case time complexity: O(1)\n");
    printf("Worst-case time complexity: O(n)\n");
    printf("Average-case time complexity: O(n)\n");
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <vector>

using namespace std;

int main() {
    vector<int> arr = {5, 2, 8, 1, 9, 4, 7, 3, 6};
    int target = 8;
    int n = arr.size();
    int index = -1;

    for (int i = 0; i < n; i++) {
        if (arr[i] == target) {
            index = i;
            break;
        }
    }

    if (index != -1) {
        cout << "Index: " << index << endl;
    } else {
        cout << "Target not found" << endl;
    }
    cout << "Best-case time complexity: O(1)" << endl;
    cout << "Worst-case time complexity: O(n)" << endl;
    cout << "Average-case time complexity: O(n)" << endl;
    return 0;
}


## Java Solution
java
public class LinearSearch {
    public static void main(String[] args) {
        int[] arr = {5, 2, 8, 1, 9, 4, 7, 3, 6};
        int target = 8;
        int n = arr.length;
        int index = -1;

        for (int i = 0; i < n; i++) {
            if (arr[i] == target) {
                index = i;
                break;
            }
        }

        if (index != -1) {
            System.out.println("Index: " + index);
        } else {
            System.out.println("Target not found");
        }
        System.out.println("Best-case time complexity: O(1)");
        System.out.println("Worst-case time complexity: O(n)");
        System.out.println("Average-case time complexity: O(n)");
    }
}


## Python Solution
python
arr = [5, 2, 8, 1, 9, 4, 7, 3, 6]
target = 8

index = -1
for i, num in enumerate(arr):
    if num == target:
        index = i
        break

if index != -1:
    print(f"Index: {index}")
else:
    print("Target not found")
print("Best-case time complexity: O(1)")
print("Worst-case time complexity: O(n)")
print("Average-case time complexity: O(n)")


## JavaScript Solution
javascript
const arr = [5, 2, 8, 1, 9, 4, 7, 3, 6];
const target = 8;

let index = -1;
for (let i = 0; i < arr.length; i++) {
  if (arr[i] === target) {
    index = i;
    break;
  }
}

if (index !== -1) {
  console.log(`Index: ${index}`);
} else {
  console.log("Target not found");
}
console.log("Best-case time complexity: O(1)");
console.log("Worst-case time complexity: O(n)");
console.log("Average-case time complexity: O(n)");
