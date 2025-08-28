# Solutions for Weekday Name Generator

### Approach

This problem uses conditional statements to map an integer input to a day of the week.  We use a `switch-case` (or equivalent `if-else if-else` chain) statement to handle the different integer inputs and return the appropriate day name. Invalid input is detected and a message is printed if the input is outside of the valid range (1-7).
The time complexity is O(1) because the lookup is constant time, irrespective of the input value.

## C Solution
c
#include <stdio.h>

char* getDayName(int day) {
    switch (day) {
        case 1: return "Monday";
        case 2: return "Tuesday";
        case 3: return "Wednesday";
        case 4: return "Thursday";
        case 5: return "Friday";
        case 6: return "Saturday";
        case 7: return "Sunday";
        default: return "Invalid day number";
    }
}

int main() {
    int day;
    scanf("%d", &day);
    printf("%s\n", getDayName(day));
    return 0;
}


## C++ Solution
cpp
#include <iostream>
#include <string>

std::string getDayName(int day) {
    switch (day) {
        case 1: return "Monday";
        case 2: return "Tuesday";
        case 3: return "Wednesday";
        case 4: return "Thursday";
        case 5: return "Friday";
        case 6: return "Saturday";
        case 7: return "Sunday";
        default: return "Invalid day number";
    }
}

int main() {
    int day;
    std::cin >> day;
    std::cout << getDayName(day) << std::endl;
    return 0;
}


## Java Solution
java
import java.util.Scanner;

public class Main {
    public static String getDayName(int day) {
        switch (day) {
            case 1: return "Monday";
            case 2: return "Tuesday";
            case 3: return "Wednesday";
            case 4: return "Thursday";
            case 5: return "Friday";
            case 6: return "Saturday";
            case 7: return "Sunday";
            default: return "Invalid day number";
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int day = scanner.nextInt();
        System.out.println(getDayName(day));
        scanner.close();
    }
}


## Python Solution
python
def get_day_name(day):
    days = {1: "Monday", 2: "Tuesday", 3: "Wednesday", 4: "Thursday", 5: "Friday", 6: "Saturday", 7: "Sunday"}
    return days.get(day, "Invalid day number")

if __name__ == "__main__":
    day = int(input())
    print(get_day_name(day))


## JavaScript Solution
javascript
function getDayName(day) {
    switch (day) {
        case 1: return "Monday";
        case 2: return "Tuesday";
        case 3: return "Wednesday";
        case 4: return "Thursday";
        case 5: return "Friday";
        case 6: return "Saturday";
        case 7: return "Sunday";
        default: return "Invalid day number";
    }
}

const readline = require('readline');
const rl = readline.createInterface({ input: process.stdin, output: process.stdout });
rl.on('line', (line) => {
    const day = parseInt(line);
    console.log(getDayName(day));
    rl.close();
});
