# Solutions for Find the First Even Number

## C Solution
c
#include <stdio.h>

int findFirstEven(int arr[], int size) {
    for (int i = 0; i < size; i++) {
        if (arr[i] % 2 == 0) {
            return arr[i];
        }
    }
    return -1;
}

int main() {
    int arr1[] = {1, 3, 5, 2, 4, 6};
    int size1 = sizeof(arr1) / sizeof(arr1[0]);
    printf("First even number in arr1: %d\n", findFirstEven(arr1, size1));

    int arr2[] = {1, 3, 5, 7, 9};
    int size2 = sizeof(arr2) / sizeof(arr2[0]);
    printf("First even number in arr2: %d\n", findFirstEven(arr2, size2));
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <vector>

int findFirstEven(const std::vector<int>& arr) {
    for (int num : arr) {
        if (num % 2 == 0) {
            return num;
        }
    }
    return -1;
}

int main() {
    std::vector<int> arr1 = {1, 3, 5, 2, 4, 6};
    std::cout << "First even number in arr1: " << findFirstEven(arr1) << std::endl;

    std::vector<int> arr2 = {1, 3, 5, 7, 9};
    std::cout << "First even number in arr2: " << findFirstEven(arr2) << std::endl;
    return 0;
}


## Java Solution
java
import java.util.Arrays;

public class FirstEven {
    public static int findFirstEven(int[] arr) {
        for (int num : arr) {
            if (num % 2 == 0) {
                return num;
            }
        }
        return -1;
    }

    public static void main(String[] args) {
        int[] arr1 = {1, 3, 5, 2, 4, 6};
        System.out.println("First even number in arr1: " + findFirstEven(arr1));

        int[] arr2 = {1, 3, 5, 7, 9};
        System.out.println("First even number in arr2: " + findFirstEven(arr2));
    }
}


## Python Solution
python
def find_first_even(arr):
    for num in arr:
        if num % 2 == 0:
            return num
    return -1

arr1 = [1, 3, 5, 2, 4, 6]
print(f"First even number in arr1: {find_first_even(arr1)}")

arr2 = [1, 3, 5, 7, 9]
print(f"First even number in arr2: {find_first_even(arr2)}")


## JavaScript Solution
javascript
function findFirstEven(arr) {
    for (let num of arr) {
        if (num % 2 === 0) {
            return num;
        }
    }
    return -1;
}

let arr1 = [1, 3, 5, 2, 4, 6];
console.log("First even number in arr1: "+ findFirstEven(arr1));

let arr2 = [1, 3, 5, 7, 9];
console.log("First even number in arr2: " + findFirstEven(arr2));
