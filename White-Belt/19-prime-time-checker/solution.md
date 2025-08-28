# Solutions for Prime Time Checker
### Approach
This problem can be solved by iterating from 2 up to the square root of the input number. If any number in this range divides the input number without a remainder, it's not prime. Otherwise, it's prime.  The time complexity is approximately O(√n), where n is the input number. The space complexity is O(1).
## C Solution
c
#include <stdio.h>
#include <stdbool.h>
#include <math.h>

boolean isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= sqrt(n); i++) {
        if (n % i == 0) return false;
    }
    return true;
}

int main() {
    int num;
    scanf("%d", &num);
    if (isPrime(num)) {
        printf("true\n");
    } else {
        printf("false\n");
    }
    return 0;
}

## C++ Solution
cpp
#include <iostream>
#include <cmath>

bool isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= sqrt(n); i++) {
        if (n % i == 0) return false;
    }
    return true;
}

int main() {
    int num;
    std::cin >> num;
    if (isPrime(num)) {
        std::cout << "true" << std::endl;
    } else {
        std::cout << "false" << std::endl;
    }
    return 0;
}

## Java Solution
java
import java.util.Scanner;
import java.lang.Math;

public class PrimeCheck {
    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i <= Math.sqrt(n); i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num = scanner.nextInt();
        if (isPrime(num)) {
            System.out.println("true");
        } else {
            System.out.println("false");
        }
        scanner.close();
    }
}

## Python Solution
python
import math

def is_prime(n):
    if n <= 1:
        return False
    for i in range(2, int(math.sqrt(n)) + 1):
        if n % i == 0:
            return False
    return True

num = int(input())
print("true" if is_prime(num) else "false")

## JavaScript Solution
javascript
function isPrime(n) {
    if (n <= 1) return false;
    for (let i = 2; i <= Math.sqrt(n); i++) {
        if (n % i === 0) return false;
    }
    return true;
}

const num = parseInt(require('readline-sync').question());
console.log(isPrime(num) ? "true" : "false");
