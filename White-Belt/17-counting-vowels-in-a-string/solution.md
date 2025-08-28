# Solutions for Counting Vowels in a String

### Approach
This problem can be solved efficiently using a loop to iterate through each character of the input string.  A conditional statement checks if each character is a vowel (case-insensitive). A counter variable keeps track of the total number of vowels encountered. The time complexity is O(n), where n is the length of the string, and the space complexity is O(1).

## C Solution
c
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int countVowels(char *str) {
    int count = 0;
    for (int i = 0; i < strlen(str); i++) {
        char c = tolower(str[i]);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            count++;
        }
    }
    return count;
}

int main() {
    char str[101];
    scanf("%s", str);
    printf("%d\n", countVowels(str));
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <string>
#include <algorithm>

using namespace std;

int countVowels(string str) {
    int count = 0;
    for (char c : str) {
        c = tolower(c);
        if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') {
            count++;
        }
    }
    return count;
}

int main() {
    string str;
    cin >> str;
    cout << countVowels(str) << endl;
    return 0;
}


## Java Solution
java
import java.util.Scanner;

public class Main {
    public static int countVowels(String str) {
        int count = 0;
        for (char c : str.toLowerCase().toCharArray()) {
            if ("aeiou".indexOf(c) != -1) {
                count++;
            }
        }
        return count;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();
        System.out.println(countVowels(str));
        scanner.close();
    }
}


## Python Solution
python
def count_vowels(s):
    count = 0
    for char in s.lower():
        if char in "aeiou":
            count += 1
    return count

if __name__ == "__main__":
    s = input()
    print(count_vowels(s))


## JavaScript Solution
javascript
function countVowels(str) {
  let count = 0;
  for (let i = 0; i < str.length; i++) {
    const char = str[i].toLowerCase();
    if ("aeiou".includes(char)) {
      count++;
    }
  }
  return count;
}

const readline = require('readline').createInterface({
    input: process.stdin,
    output: process.stdout,
});

readline.on('line', (line) => {
    console.log(countVowels(line));
    readline.close();
});
