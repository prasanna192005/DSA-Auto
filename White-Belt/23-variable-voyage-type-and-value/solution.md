### Approach

This problem focuses on understanding basic variable declaration and data types. The solution declares variables of different types, assigns values, and prints them along with their types using formatted output.



## C++ Solution

```cpp

#include <iostream>

#include <string>

#include <typeinfo>



void printVariableInfo(int val, std::string typeName){

    std::cout << typeName << ": " << val << std::endl;

}



void printVariableInfo(double val, std::string typeName){

    std::cout << typeName << ": " << val << std::endl;

}



void printVariableInfo(char val, std::string typeName){

    std::cout << typeName << ": " << val << std::endl;

}



void printVariableInfo(bool val, std::string typeName){

    std::cout << typeName << ": " << val << std::endl;

}



int main() {

    int intValue = 10;

    double floatValue = 3.14;

    char charValue = 'A';

    bool boolValue = true;



    printVariableInfo(intValue, "Integer");

    printVariableInfo(floatValue, "Float");

    printVariableInfo(charValue, "Character");

    printVariableInfo(boolValue, "Boolean");



    return 0;

}


```


## Python Solution

python

def print_variable_info(val, type_name):

    print(f"{type_name}: {val}")



def main():

    int_value = 10

    float_value = 3.14

    char_value = 'A'

    bool_value = True



    print_variable_info(int_value, "Integer")

    print_variable_info(float_value, "Float")

    print_variable_info(char_value, "Character")

    print_variable_info(bool_value, "Boolean")



if __name__ == "__main__":

    main()





## Java Solution

java

public class VariableVoyage {

    public static void printVariableInfo(int val, String typeName) {

        System.out.println(typeName + ": " + val);

    }



    public static void printVariableInfo(double val, String typeName) {

        System.out.println(typeName + ": " + val);

    }



    public static void printVariableInfo(char val, String typeName) {

        System.out.println(typeName + ": " + val);

    }



    public static void printVariableInfo(boolean val, String typeName) {

        System.out.println(typeName + ": " + val);

    }



    public static void main(String[] args) {

        int intValue = 10;

        double floatValue = 3.14;

        char charValue = 'A';

        boolean boolValue = true;



        printVariableInfo(intValue, "Integer");

        printVariableInfo(floatValue, "Float");

        printVariableInfo(charValue, "Character");

        printVariableInfo(boolValue, "Boolean");

    }

}





## JavaScript Solution

javascript

function printVariableInfo(val, typeName) {

    console.log(`${typeName}: ${val}`);

}



function main() {

    let intValue = 10;

    let floatValue = 3.14;

    let charValue = 'A';

    let boolValue = true;



    printVariableInfo(intValue, "Integer");

    printVariableInfo(floatValue, "Float");

    printVariableInfo(charValue, "Character");

    printVariableInfo(boolValue, "Boolean");

}



main();

