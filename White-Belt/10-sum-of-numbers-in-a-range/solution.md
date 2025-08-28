# Solutions for Sum of Numbers in a Range

### Approach
This problem can be solved using a simple `for` loop. The loop iterates through the numbers in the specified range, adding each number to a running sum.  Alternatively, a mathematical formula can be used for efficiency:  sum = n*(a + l)/2, where n is the number of terms, a is the first term, and l is the last term.

## C Solution
c
#include <stdio.h>

int main() {
    int start, end, sum = 0;
    scanf("%d %d", &start, &end);
    for (int i = start; i <= end; i++) {
        sum += i;
    }
    printf("%d\n", sum);
    return 0;
}


## C++ Solution
cpp
#include <iostream>

int main() {
    int start, end, sum = 0;
    std::cin >> start >> end;
    for (int i = start; i <= end; i++) {
        sum += i;
    }
    std::cout << sum << std::endl;
    return 0;
}


## Java Solution
java
import java.util.*;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int start = scanner.nextInt();
        int end = scanner.nextInt();
        int sum = 0;
        for (int i = start; i <= end; i++) {
            sum += i;
        }
        System.out.println(sum);
        scanner.close();
    }
}


## Python Solution
python
start, end = map(int, input().split())
sum = 0
for i in range(start, end + 1):
    sum += i
print(sum)


## JavaScript Solution
javascript
const readline = require('readline');
const rl = readline.createInterface({ input: process.stdin, output: process.stdout });

rl.on('line', (line) => {
    const [start, end] = line.split(' ').map(Number);
    let sum = 0;
    for (let i = start; i <= end; i++) {
        sum += i;
    }
    console.log(sum);
    rl.close();
});
