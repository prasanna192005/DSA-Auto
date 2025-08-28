# Solutions for The Curious Case of the Reversed Sum

### Approach
The algorithm involves three steps:  First, calculate the sum of the two input integers. Second, convert the sum to a string. Third, reverse the string and convert it back to an integer. This approach uses basic arithmetic and string manipulation. The time complexity is O(1) because the operations on integers are constant time, and string manipulation on these relatively small numbers is also effectively constant. The space complexity is also O(1) as we are only storing a few integer and string variables. An alternative approach would be to reverse the numbers individually before summing, however this is more complex and unnecessary for this problem.

## C Solution
```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int reverseSum(int a, int b) {
    int sum = a + b;
    char sumStr[10];
    sprintf(sumStr, "%d", sum);
    int len = strlen(sumStr);
    for (int i = 0; i < len / 2; i++) {
        char temp = sumStr[i];
        sumStr[i] = sumStr[len - 1 - i];
        sumStr[len - 1 - i] = temp;
    }
    return atoi(sumStr);
}

int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d\n", reverseSum(a, b));
    return 0;
}
```

## C++ Solution
```cpp
#include <iostream>
#include <algorithm>

using namespace std;

int reverseSum(int a, int b) {
    int sum = a + b;
    string sumStr = to_string(sum);
    reverse(sumStr.begin(), sumStr.end());
    return stoi(sumStr);
}

int main() {
    int a, b;
    cin >> a >> b;
    cout << reverseSum(a, b) << endl;
    return 0;
}
```

## Java Solution
```java
import java.util.*;

class Solution {
    public int reverseSum(int a, int b) {
        int sum = a + b;
        String sumStr = Integer.toString(sum);
        String reversedStr = new StringBuilder(sumStr).reverse().toString();
        return Integer.parseInt(reversedStr);
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int a = scanner.nextInt();
        int b = scanner.nextInt();
        Solution solution = new Solution();
        System.out.println(solution.reverseSum(a, b));
        scanner.close();
    }
}
```

## Python Solution
```python
def reverse_sum(a, b):
    sum_ab = a + b
    return int(str(sum_ab)[::-1])

if __name__ == "__main__":
    a, b = map(int, input().split())
    print(reverse_sum(a, b))
```

## JavaScript Solution
```javascript
function reverseSum(a, b) {
  let sum = a + b;
  let sumStr = sum.toString();
  let reversedStr = sumStr.split("").reverse().join("");
  return parseInt(reversedStr);
}

let input = require('fs').readFileSync('/dev/stdin', 'utf8');
let lines = input.trim().split(' ');
let a = parseInt(lines[0]);
let b = parseInt(lines[1]);
console.log(reverseSum(a,b));
```