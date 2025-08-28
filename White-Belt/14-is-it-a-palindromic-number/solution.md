# Solutions for Is it a Palindromic Number?

### Approach
The solution involves converting the integer to a string, then comparing the string to its reverse.  This approach avoids the complexities of digit-by-digit manipulation. The time complexity is O(n), where n is the number of digits in the integer, due to the string reversal. The space complexity is O(n) in the worst case, due to the creation of the reversed string.   Negative numbers are explicitly checked and handled to maintain consistent behavior as outlined in the problem description.

## C Solution
c
#include <stdio.h>
#include <stdbool.h>
#include <string.h>
#include <stdlib.h>

boolean isPalindrome(int x) {
    if (x < 0) return false; // Negative numbers are not palindromes
    char str[12]; //sufficient for 32-bit integers
    sprintf(str, "%d", x);
    int len = strlen(str);
    for (int i = 0; i < len / 2; i++) {
        if (str[i] != str[len - 1 - i]) {
            return false;
        }
    }
    return true;
}

int main() {
    int num;
    scanf("%d", &num);
    if (isPalindrome(num)) {
        printf("true\n");
    } else {
        printf("false\n");
    }
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <algorithm>
#include <string>

bool isPalindrome(int x) {
    if (x < 0) return false;
    std::string s = std::to_string(x);
    std::string rs = s;
    std::reverse(rs.begin(), rs.end());
    return s == rs;
}

int main() {
    int num;
    std::cin >> num;
    if (isPalindrome(num)) {
        std::cout << "true" << std::endl;
    } else {
        std::cout << "false" << std::endl;
    }
    return 0;
}


## Java Solution
java
import java.util.Scanner;

public class Main {
    public static boolean isPalindrome(int x) {
        if (x < 0) return false;
        String s = Integer.toString(x);
        String rs = new StringBuilder(s).reverse().toString();
        return s.equals(rs);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num = scanner.nextInt();
        System.out.println(isPalindrome(num));
        scanner.close();
    }
}


## Python Solution
python
def is_palindrome(n):
    return str(n) == str(n)[::-1] and n >=0

if __name__ == "__main__":
    num = int(input())
    print(is_palindrome(num))


## JavaScript Solution
javascript
function isPalindrome(x) {
  if (x < 0) return false;
  const s = x.toString();
  const rs = s.split('').reverse().join('');
  return s === rs;
}

const readline = require('readline').createInterface({
  input: process.stdin,
  output: process.stdout,
});

readline.on('line', (line) => {
  const num = parseInt(line, 10);
  console.log(isPalindrome(num));
  readline.close();
});
