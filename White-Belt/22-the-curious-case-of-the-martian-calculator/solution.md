### Approach

The solution involves performing the four basic arithmetic operations on the input integers.  The results are then checked against the specified conditions using relational and logical operators. The output is formatted to clearly display the results of each operation and condition.

c
#include <stdio.h>
#include <stdbool.h>

void martianCalculator(int a, int b) {
    if (b == 0) {
        printf("Error: Division by zero");
        return;
    }
    int sum = a + b;
    int diff = a - b;
    int prod = a * b;
    int quot = a / b;
    bool sumGT10 = sum > 10;
    bool diffLTNeg5 = diff < -5;
    bool prodEven = prod % 2 == 0;
    bool quotZero = quot == 0;
    printf("Sum: %d, Greater than 10: %s\n", sum, sumGT10 ? "True" : "False");
    printf("Difference: %d, Less than -5: %s\n", diff, diffLTNeg5 ? "True" : "False");
    printf("Product: %d, Even: %s\n", prod, prodEven ? "True" : "False");
    printf("Quotient: %d, Zero: %s\n", quot, quotZero ? "True" : "False");
}

int main() {
    martianCalculator(15, 5);
    return 0;
}


cpp
#include <iostream>

void martianCalculator(int a, int b) {
    if (b == 0) {
        std::cout << "Error: Division by zero" << std::endl;
        return;
    }
    int sum = a + b;
    int diff = a - b;
    int prod = a * b;
    int quot = a / b;
    std::cout << "Sum: " << sum << ", Greater than 10: " << (sum > 10) << std::endl;
    std::cout << "Difference: " << diff << ", Less than -5: " << (diff < -5) << std::endl;
    std::cout << "Product: " << prod << ", Even: " << (prod % 2 == 0) << std::endl;
    std::cout << "Quotient: " << quot << ", Zero: " << (quot == 0) << std::endl;
}

int main() {
    martianCalculator(15, 5);
    return 0;
}


java
public class MartianCalculator {
    public static void martianCalculator(int a, int b) {
        if (b == 0) {
            System.out.println("Error: Division by zero");
            return;
        }
        int sum = a + b;
        int diff = a - b;
        int prod = a * b;
        int quot = a / b;
        System.out.println("Sum: " + sum + ", Greater than 10: " + (sum > 10));
        System.out.println("Difference: " + diff + ", Less than -5: " + (diff < -5));
        System.out.println("Product: " + prod + ", Even: " + (prod % 2 == 0));
        System.out.println("Quotient: " + quot + ", Zero: " + (quot == 0));
    }
    public static void main(String[] args) {
        martianCalculator(15, 5);
    }
}


python
def martian_calculator(a, b):
    if b == 0:
        print("Error: Division by zero")
        return
    sum_ab = a + b
    diff_ab = a - b
    prod_ab = a * b
    quot_ab = a // b
    print(f"Sum: {sum_ab}, Greater than 10: {sum_ab > 10}")
    print(f"Difference: {diff_ab}, Less than -5: {diff_ab < -5}")
    print(f"Product: {prod_ab}, Even: {prod_ab % 2 == 0}")
    print(f"Quotient: {quot_ab}, Zero: {quot_ab == 0}")

martian_calculator(15, 5)


javascript
function martianCalculator(a, b) {
    if (b === 0) {
        console.log("Error: Division by zero");
        return;
    }
    let sum = a + b;
    let diff = a - b;
    let prod = a * b;
    let quot = Math.floor(a / b);
    console.log(`Sum: ${sum}, Greater than 10: ${sum > 10}`);
    console.log(`Difference: ${diff}, Less than -5: ${diff < -5}`);
    console.log(`Product: ${prod}, Even: ${prod % 2 === 0}`);
    console.log(`Quotient: ${quot}, Zero: ${quot === 0}`);
}

martianCalculator(15, 5);
