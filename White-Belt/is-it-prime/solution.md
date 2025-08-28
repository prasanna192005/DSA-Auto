# Approach

The most straightforward approach is to iterate from 2 up to the square root of the input number. If any number in this range divides the input number evenly, then the input number is not prime.  We handle the special case of 1 and 2 separately.

c
#include <stdio.h>
#include <stdbool.h>
#include <math.h>

boolean isPrime(int n) {
  if (n <= 1) return false;
  if (n <= 3) return true;
  if (n % 2 == 0 || n % 3 == 0) return false;

  for (int i = 5; i * i <= n; i = i + 6) 
    if (n % i == 0 || n % (i + 2) == 0)
      return false;

  return true;
}

int main() {
  int num;
  printf("Enter a number (2-1000): ");
  scanf("%d", &num);
  if (isPrime(num)) {
    printf("%d is a prime number\n", num);
  } else {
    printf("%d is not a prime number\n", num);
  }
  return 0;
}


cpp
#include <iostream>
#include <cmath>

bool isPrime(int n) {
  if (n <= 1) return false;
  if (n <= 3) return true;
  if (n % 2 == 0 || n % 3 == 0) return false;

  for (int i = 5; i * i <= n; i = i + 6) {
    if (n % i == 0 || n % (i + 2) == 0) {
      return false;
    }
  }
  return true;
}

int main() {
  int num;
  std::cout << "Enter a number (2-1000): ";
  std::cin >> num;
  if (isPrime(num)) {
    std::cout << num << " is a prime number\n";
  } else {
    std::cout << num << " is not a prime number\n";
  }
  return 0;
}


java
import java.util.Scanner;

public class PrimeCheck {

    public static boolean isPrime(int n) {
        if (n <= 1) return false;
        if (n <= 3) return true;
        if (n % 2 == 0 || n % 3 == 0) return false;

        for (int i = 5; i * i <= n; i = i + 6) {
            if (n % i == 0 || n % (i + 2) == 0) {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number (2-1000): ");
        int num = scanner.nextInt();
        if (isPrime(num)) {
            System.out.println(num + " is a prime number");
        } else {
            System.out.println(num + " is not a prime number");
        }
        scanner.close();
    }
}


python
import math

def is_prime(n):
  if n <= 1:
    return False
  if n <= 3:
    return True
  if n % 2 == 0 or n % 3 == 0:
    return False
  for i in range(5, int(math.sqrt(n)) + 1, 6):
    if n % i == 0 or n % (i + 2) == 0:
      return False
  return True

num = int(input("Enter a number (2-1000): "))
if is_prime(num):
  print(f"{num} is a prime number")
else:
  print(f"{num} is not a prime number")


javascript
function isPrime(n) {
  if (n <= 1) return false;
  if (n <= 3) return true;
  if (n % 2 === 0 || n % 3 === 0) return false;

  for (let i = 5; i * i <= n; i += 6) {
    if (n % i === 0 || n % (i + 2) === 0) {
      return false;
    }
  }
  return true;
}

let num = parseInt(prompt("Enter a number (2-1000):"));
if (isPrime(num)) {
  console.log(num + " is a prime number");
} else {
  console.log(num + " is not a prime number");
}
