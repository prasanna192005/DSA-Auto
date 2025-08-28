# Solutions for Integer to String Conversion Challenge

### Approach
This problem involves converting an integer to its string representation without using built-in functions. We'll handle positive and negative numbers separately.  The core logic is to repeatedly extract the last digit using the modulo operator (`%`) and build the string from right to left. We use a StringBuilder-like approach (depending on the language) to efficiently concatenate characters. The time complexity is O(log n) because we iterate through the digits of the number, and the space complexity is O(log n) to store the string.

## C Solution
c
#include <stdio.h>
#include <stdlib.h>

char* intToString(int num) {
    char* str;
    int sign = 1;
    if (num < 0) {
        sign = -1;
        num = -num;
    }
    int len = 0;
    int temp = num;
    while (temp > 0) {
        len++;
        temp /= 10;
    }
    str = (char*)malloc(sizeof(char) * (len + (sign == -1 ? 1 : 0) + 1)); // +1 for null terminator
    if (sign == -1) str[0] = '-';
    str[len + (sign == -1 ? 1 : 0)] = '\0';
    int i = len + (sign == -1 ? 1 : 0) - 1;
    while (num > 0) {
        str[i] = num % 10 + '0';
        num /= 10;
        i--;
    }
    return str;
}

int main() {
    int num;
    scanf("%d", &num);
    char* result = intToString(num);
    printf("%s\n", result);
    free(result);
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <string>
#include <algorithm>

std::string intToString(int num) {
    std::string result = "";
    bool isNegative = num < 0;
    if (isNegative) num = -num;
    do {
        result += (num % 10 + '0');
    } while (num /= 10);
    if (isNegative) result += "-";
    std::reverse(result.begin(), result.end());
    return result;
}

int main() {
    int num;
    std::cin >> num;
    std::cout << intToString(num) << std::endl;
    return 0;
}


## Java Solution
java
import java.util.Scanner;
public class Main {
    public static String intToString(int num) {
        StringBuilder sb = new StringBuilder();
        boolean negative = num < 0;
        if (negative) num = -num;
        do {
            sb.append((char)(num % 10 + '0'));
        } while ((num /= 10) > 0);
        if (negative) sb.append('-');
        return sb.reverse().toString();
    }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int num = scanner.nextInt();
        System.out.println(intToString(num));
        scanner.close();
    }
}


## Python Solution
python
def int_to_string(num):
    sign = '-' if num < 0 else ''
    num = abs(num)
    result = ''
    while num > 0:
        result = str(num % 10) + result
        num //= 10
    return sign + result

if __name__ == "__main__":
    num = int(input())
    print(int_to_string(num))


## JavaScript Solution
javascript
function intToString(num) {
    let sign = num < 0 ? '-' : '';
    num = Math.abs(num);
    let result = '';
    do {
        result = (num % 10) + result;
        num = Math.floor(num / 10);
    } while (num > 0);
    return sign + result;
}

const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout,
});

readline.on('line', (line) => {
    const num = parseInt(line);
    console.log(intToString(num));
    readline.close();
});
