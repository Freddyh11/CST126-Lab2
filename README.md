# CST126-Lab2
Oregon Institute of Technology
CST 126 Solving Complex Problems
Lab #2: Dynamic Memory


CST126
Module 2: Lab 2


Dynamic Memory Allocation
Write a program that:
1. Reads the number of students from the keyboard.
2. Allocates enough room to store the final exam scores for each of the students.
3. Reads in each of the students’ scores.
4. Display to the screen all of the scores and the average of the scores.


Submit: full development process
10 pts


Concatenation
Write a program that includes a function called StrCat_s which simulates its predefined namesake. 
StrCat_s receives three parameters:
* src: a pointer to the source string
* dest: a pointer to the destination string
* d_size: int destination size
Dynamically allocate the appropriate amount of memory.
Return the pointer to the destination string.


Submit: full development process
10 pts


Memory Leak Detection
Write a program that stores stock symbols into dynamic arrays.
The user will enter as many stocks as desired.
Display the list of stocks after each entry.
Add the code necessary to detect any memory leaks.


Submit: full development process
10 pts


Debugging


1. Go to learnbydoingbooks.com
2. Select STUDENT RESOURCES
3. Download Chapter 09.zip
4. Load the Chapter 9 Debug.cpp code
5. Follow the instructions in the top of the code.


Submit: code & runs
10 pts


________________


Sorting/Code Modification


Modify the following code so that it sorts in descending order.
#include <iostream>
#include <string.h>
 
using namespace std;
 
int compare_ints(const void*, const void*);
int compare_strs(const void*, const void*);
 
int main()
{
    const char * shrooms[10] =
    {
        "Matsutake", "Lobster", "Oyster", "King Boletus",
        "Shaggy Mane", "Morel", "Chanterelle", "Calf Brain",
        "Pig's Ear", "Chicken of the Woods"
 
    };
 
    int nums[10] = { 99, 43, 23, 100, 66, 12, 0, 125, 76, 2 };
 
    // The address of the array, number of elements the size of each      
    // element, the function pointer to compare two of the elements 
    qsort((void*)shrooms, 10, sizeof(char*), compare_strs);
    qsort((void*)nums, 10, sizeof(int), compare_ints);
 
    // Output sorted lists 
 
    for (int i = 0; i < 10; ++i)
        cout << shrooms[i] << endl;
 
    for (int i = 0; i < 10; ++i)
        cout << nums[i] << endl;
 
    return 0;
}
 
________________


int compare_ints(const void* arg1, const void* arg2)
{
    int return_value = 0;
 
    if (*(int*)arg1 < *(int*)arg2)
        return_value = -1;
    else if (*(int*)arg1 > *(int*)arg2)
        return_value = 1;
 
    return return_value;
}
 
int compare_strs(const void* arg1, const void* arg2)
{
    return (_stricmp(*((char**)arg1), *((char**)arg2))); // note: some IDE’s use strcmp here
}


Submit: code & runs
10 pts




Total: 50 pts
