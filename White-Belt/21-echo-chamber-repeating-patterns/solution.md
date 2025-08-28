### Approach
The solution iterates through the input string. For each character, it repeats the character a number of times equal to its index (starting from 1). The repeated characters are then appended to the output string.

c
#include <stdio.h>
#include <string.h>

char* repeatChars(char* input) {
    int len = strlen(input);
    char* output = (char*)malloc(len * len + 1); //allocate enough space
    output[0] = '\0';
    for (int i = 0; i < len; i++) {
        for (int j = 0; j <= i; j++) {
            strncat(output, &input[i], 1);
        }
    }
    return output;
}

int main(){
    char str[] = "abc";
    char *result = repeatChars(str);
    printf("%s\n",result);
    free(result);
    return 0;
}


cpp
#include <iostream>
#include <string>

std::string repeatChars(std::string input) {
    std::string output = "";
    for (int i = 0; i < input.length(); i++) {
        for (int j = 0; j <= i; j++) {
            output += input[i];
        }
    }
    return output;
}

int main() {
    std::string str = "abc";
    std::string result = repeatChars(str);
    std::cout << result << std::endl;
    return 0;
}


java
public class RepeatChars {
    public static String repeatChars(String input) {
        String output = "";
        for (int i = 0; i < input.length(); i++) {
            for (int j = 0; j <= i; j++) {
                output += input.charAt(i);
            }
        }
        return output;
    }
    public static void main(String[] args) {
        String str = "abc";
        String result = repeatChars(str);
        System.out.println(result);
    }
}


python
def repeat_chars(input_str):
    output_str = ""
    for i, char in enumerate(input_str):
        output_str += char * (i + 1)
    return output_str

print(repeat_chars("abc"))


javascript
function repeatChars(input) {
  let output = "";
  for (let i = 0; i < input.length; i++) {
    for (let j = 0; j <= i; j++) {
      output += input[i];
    }
  }
  return output;
}

console.log(repeatChars("abc"));
