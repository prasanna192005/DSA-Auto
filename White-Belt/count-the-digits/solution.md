# Solution

**Approach:**

The simplest approach is to convert the integer to a string and then find the length of the string.  Alternatively, we can repeatedly divide by 10 until the number becomes 0 and count the number of times we perform the division. This avoids string conversion.

**C++:**
cpp
#include <iostream>
#include <algorithm>
#include <string>

using namespace std;

int countDigits(long long n) {
  //Approach 1: String Conversion
  //return to_string(n).length();

  //Approach 2: Repeated Division
  if (n == 0) return 1;
  if (n < 0) n = -n; //Handle negative numbers
  int count = 0;
  while (n > 0) {
    n /= 10;
    count++;
  }
  return count;
}

int main() {
  long long num;
  cin >> num;
  cout << countDigits(num) << endl;
  return 0;
}


**Java:**
java
import java.util.*;

public class CountDigits {
    public static int countDigits(long n) {
        //Approach 1: String Conversion
        //return String.valueOf(n).length();
        
        //Approach 2: Repeated Division
        if (n == 0) return 1;
        if (n < 0) n = -n; //Handle negative numbers
        int count = 0;
        while (n > 0) {
            n /= 10;
            count++;
        }
        return count;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        long num = sc.nextLong();
        System.out.println(countDigits(num));
        sc.close();
    }
}


**Python:**
python
def count_digits(n):
  #Approach 1: String Conversion
  #return len(str(n))

  #Approach 2: Repeated Division
  if n == 0: return 1
  if n < 0: n = -n #Handle negative numbers
  count = 0
  while n > 0:
    n //= 10
    count += 1
  return count

num = int(input())
print(count_digits(num))


**JavaScript:**
javascript
function countDigits(n) {
  //Approach 1: String Conversion
  //return String(n).length;
  
  //Approach 2: Repeated Division
  if (n === 0) return 1;
  if (n < 0) n = -n; //Handle negative numbers
  let count = 0;
  while (n > 0) {
    n = Math.floor(n / 10);
    count++;
  }
  return count;
}

let num = parseInt(prompt());
console.log(countDigits(num));
