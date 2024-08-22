# Exp-9
# Aim
To study and implement C++Pointer basics
# Software Used
Visual Studio Code
# Theory
Pointers are a fundamental concept in C++ that allows for efficient and flexible data manipulation by providing direct access to memory addresses. A pointer is essentially a variable that contains the memory address of another variable, allowing you to access and modify the value stored at that address.

Pointers are declared with an asterisk (*) before the variable name and must be initialized with the address of another variable using the address-of operator (&). Dereferencing is the process of accessing the value at the address stored in a pointer using the asterisk operator. 

Pointer arithmetic enables traversal through contiguous memory locations, such as array elements, by incrementing or decrementing pointers.In fact, in C++, an array name functions as a pointer to the first element, making pointers an effective tool for working with arrays. Furthermore, pointers can refer to other pointers, known as double pointers, which are useful for managing complex data structures such as matrices and dynamic memory allocation. Pointers can also be passed to functions, allowing them to directly modify the original variables. 

This is especially useful when modifying arrays or returning multiple values from a function. Understanding pointers is essential in C++ programming because they are used in advanced topics such as dynamic memory management and efficient array and string handling.

Syntax:
```
datatype *var_name;
int *ptr; //ptr can point to an address which holds in data
```

CODES: 

1.Illustrate Pointers:

```
#include <bits/stdc++.h> 
using namespace std;
void geeks()
{
    int var = 5;
    int* ptr;                  
    ptr = &var;

    cout<<"Value at ptr = "<<ptr<<"\n";
    cout<<"Value at var = " <<var<<"\n";
    cout<<"Value at *ptr = "<<*ptr<<"\n";

}

int main()
{
    geeks();
    return 0;
}
```
O/P:

![image](https://github.com/user-attachments/assets/a92ff49b-d7dc-4104-9238-3d0f53b13aae)


2. 1D Array of pointers:
```
#include <iostream> 
using namespace std; 

int main() 
{
    int* p=new int[7];  

    for (int i=0; i<5; i++)  
    {
        p[i]=10*(i+1);
    }

    cout<<*p<<"\n"; 
    cout<<*p+1<<"\n";
    cout<<*(p+1)<<"\n";
    cout<<2[p]<<"\n";
    cout<<p[2]<<"\n";
    *p++;

    cout<<*p;                

    return 0; 
}
```
O/P:

![image](https://github.com/user-attachments/assets/21cd2319-0771-4aaf-bfdb-2f01ead0a301)

3. Pointer Arithmetic in C++ :
```
#include<iostream>
using namespace std;

int main() {
    int b = 10;
    int *ptr = &b;
    cout << "*ptr: " << *ptr << "   b: " << b << endl;
    ptr++;
    cout << "After increment: " << *ptr << endl;
    float *n, a = 8.923;
    n = &a;
    cout << endl << "*n: " << *n << "   a: " << a << "   n: " << n << "   &a: " << &a << endl;
    n++;
    cout << "After increment: " << n << endl;
    char *ch, c = 'c';
    ch = &c;
    cout << endl << (void*)ch << endl;
    ch++;
    cout << "After increment: " << (void*)ch << endl;

    return 0;
}
```

O/P:

![image](https://github.com/user-attachments/assets/4a2048df-eb85-474a-96c3-0d13ee1aa115)


4. Modifying the Contents of a Memory Location Using Pointers :
```
#include<iostream>
using namespace std;

int main() {
    int a = 10;
    int* aptr = &a;
    cout << *aptr << endl;  
    *aptr = 20;             
    cout << a << endl;      
    int arr[] = {10, 20, 30};
    cout << *arr << endl;  
    return 0;
}
```
O/P:

![image](https://github.com/user-attachments/assets/7fbfdad2-e510-4222-85bb-b140f2652e01)


5. Incrementing a Pointer to Traverse an Array :
```
#include<iostream>
using namespace std;

int main() {
    int arr[] = {10, 20, 30};
    cout << *arr << endl; 
    int *ptr = arr;
    for(int i = 0; i < 3; i++) {
        cout << *ptr << endl;  
        ptr++;                 
    }
    return 0;
}
```

O/P:

![image](https://github.com/user-attachments/assets/e6f706a4-e7e4-4060-bbbf-3a01b32665cd)

# Conclusion 
Understanding pointers is critical for effective C++ programming. They allow for direct memory access, which improves performance and flexibility in data manipulation, dynamic memory allocation, and managing complex structures. Pointer proficiency is critical for optimizing code and handling advanced programming tasks, making it essential for high-performance application development and system-level programming.
