# Solutions for String Palindrome Checker

### Approach

This solution efficiently checks for palindromes by processing the input string from both ends. It first cleans the string by removing non-alphanumeric characters and converting to lowercase for case-insensitive comparison. Then, two pointers, one at the beginning and one at the end, are used to compare characters. The time complexity is O(n), where n is the length of the string, as each character is visited once. The space complexity is O(1) as the in-place comparison uses constant extra space. 

## C Solution
c
#include <stdio.h>
#include <ctype.h>
#include <string.h>
#include <stdbool.h>

bool isPalindrome(char *str) {
    int left = 0;
    int right = strlen(str) - 1;

    while (left < right) {
        while (left < right && !isalnum(str[left])) {
            left++;
        }
        while (left < right && !isalnum(str[right])) {
            right--;
        }
        if (tolower(str[left]) != tolower(str[right])) {
            return false;
        }
        left++;
        right--;
    }
    return true;
}

int main() {
    char str[1001];
    fgets(str, sizeof(str), stdin);
    str[strcspn(str, "\n")] = 0; //Remove trailing newline
    if (isPalindrome(str)) {
        printf("true\n");
    } else {
        printf("false\n");
    }
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <string>
#include <algorithm>
#include <cctype>

bool isPalindrome(std::string s) {
    std::string alphanumeric = "";
    for (char c : s) {
        if (isalnum(c)) {
            alphanumeric += tolower(c);
        }
    }
    std::string reversed_alphanumeric = alphanumeric;
    std::reverse(reversed_alphanumeric.begin(), reversed_alphanumeric.end());
    return alphanumeric == reversed_alphanumeric;
}

int main() {
    std::string str;
    std::getline(std::cin, str);
    if (isPalindrome(str)) {
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
    public static boolean isPalindrome(String s) {
        String cleanString = s.replaceAll("[^a-zA-Z0-9]", "").toLowerCase();
        String reversedString = new StringBuilder(cleanString).reverse().toString();
        return cleanString.equals(reversedString);
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();
        System.out.println(isPalindrome(str));
        scanner.close();
    }
}


## Python Solution
python
import re
def isPalindrome(s):
    s = re.sub(r'[^a-zA-Z0-9]', '', s).lower()
    return s == s[::-1]
if __name__ == "__main__":
    s = input()
    print(isPalindrome(s))


## JavaScript Solution
javascript
function isPalindrome(s) {
    s = s.toLowerCase().replace(/[^a-z0-9]/g, '');
    return s === s.split('').reverse().join('');
}
const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout,
});
readline.on('line', (line) => {
    console.log(isPalindrome(line));
    readline.close();
});
