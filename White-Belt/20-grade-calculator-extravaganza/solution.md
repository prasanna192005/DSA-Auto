# Solutions for Grade Calculator Extravaganza
### Approach
This problem involves calculating the average of three exam scores. The approach is straightforward:  The function `calculateGrade` takes three integer exam scores as input, sums them, converts the sum to a floating-point number, divides by 3 (to compute the average), and returns the result formatted to two decimal places.  The time complexity is O(1). The space complexity is O(1).
## C Solution
c
#include <stdio.h>
#include <stdlib.h>

double calculateGrade(int exam1, int exam2, int exam3) {
    double sum = (double)(exam1 + exam2 + exam3);
    return sum / 3.0;
}

int main() {
    int exam1, exam2, exam3;
    scanf("%d %d %d", &exam1, &exam2, &exam3);
    printf("%.2lf\n", calculateGrade(exam1, exam2, exam3));
    return 0;
}

## C++ Solution
cpp
#include <iostream>
#include <iomanip>

double calculateGrade(int exam1, int exam2, int exam3) {
    double sum = (double)(exam1 + exam2 + exam3);
    return sum / 3.0;
}

int main() {
    int exam1, exam2, exam3;
    std::cin >> exam1 >> exam2 >> exam3;
    std::cout << std::fixed << std::setprecision(2) << calculateGrade(exam1, exam2, exam3) << std::endl;
    return 0;
}

## Java Solution
java
import java.util.Scanner;
import java.text.DecimalFormat;

public class GradeCalculator {
    public static double calculateGrade(int exam1, int exam2, int exam3) {
        double sum = (double)(exam1 + exam2 + exam3);
        return sum / 3.0;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int exam1 = scanner.nextInt();
        int exam2 = scanner.nextInt();
        int exam3 = scanner.nextInt();
        scanner.close();
        DecimalFormat df = new DecimalFormat("#.##");
        System.out.println(df.format(calculateGrade(exam1, exam2, exam3)));
    }
}

## Python Solution
python
def calculateGrade(exam1, exam2, exam3):
    sum = exam1 + exam2 + exam3
    return "%.2f" % (sum / 3.0)

exam1, exam2, exam3 = map(int, input().split())
print(calculateGrade(exam1, exam2, exam3))

## JavaScript Solution
javascript
function calculateGrade(exam1, exam2, exam3) {
  const sum = exam1 + exam2 + exam3;
  return (sum / 3).toFixed(2);
}

const input = require('readline-sync').question().split(' ');
const exam1 = parseInt(input[0]);
const exam2 = parseInt(input[1]);
const exam3 = parseInt(input[2]);
console.log(calculateGrade(exam1, exam2, exam3));
