Q1. Demonstrate the working of array which reads 10 elements by using 
array and display all the elements in reverse order. Receive the input 
from the user.


#include <stdio.h>

int main() {
    int elements[10];
    int i;


    for (i = 0; i < 10; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &elements[i]);
    }

  
    printf("Elements in reverse order:\n");
    for (i = 9; i >= 0; i--) {
        printf("%d\n", elements[i]);
    }

    return 0;
}

Q2. Write a C program to find maximum number in array containing 
five elements of integer type.

#include <stdio.h>

int main() {
    int elements[5];
    int max;

    
    for (int i = 0; i < 5; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%d", &elements[i]);
    }

    
    max = elements[0];

  
    for (int i = 1; i < 5; i++) {
        if (elements[i] > max) {
            max = elements[i];
        }
    }

  
    printf("The maximum element in the array is: %d\n", max);

    return 0;
}

Q3 Write a program in C to create a structure having named as books 
consists of title, author, subject, book_id as its members. Read the 
details of five books from user and display the data entered by the 
user on screen(Use array of structure)

#include <stdio.h>

 {
    char title[50];
    char author[50];
    char subject[100];
    int book_id;
};

int main() {
    
    struct books library[5];

    
    for (int i = 0; i < 5; i++) {
        printf("Enter details for Book %d:\n", i + 1);
        printf("Title: ");
        scanf("%s", library[i].title);
        printf("Author: ");
        scanf("%s", library[i].author);
        printf("Subject: ");
        scanf("%s", library[i].subject);
        printf("Book ID: ");
        scanf("%d", &library[i].book_id);
    }

    
    printf("\nDetails of Books Entered:\n");
    for (int i = 0; i < 5; i++) {
        printf("Book %d:\n", i + 1);
        printf("Title: %s\n", library[i].title);
        printf("Author: %s\n", library[i].author);
        printf("Subject: %s\n", library[i].subject);
        printf("Book ID: %d\n", library[i].book_id);
    }

    return 0;
}


Q4 Define a structure named ‘State’ which contains four fields name,
population, lit_rate, income. Declare a structure variable as 
st1.Assign the values for your structure members as 
Maharashtra,1000000,5.8,6000.00 respectively.



#include <stdio.h>

struct State {
    char name[50];
    int population;
    float lit_rate;
    float income;
};

int main() {
    struct State st1;
    strcpy(st1.name, "Maharashtra");
    st1.population = 1000000;
    st1.lit_rate = 5.8;
    st1.income = 6000.00;

    printf("State Name: %s\n", st1.name);
    printf("Population: %d\n", st1.population);
    printf("Literacy Rate: %.1f\n", st1.lit_rate);
    printf("Income: %.2f\n", st1.income);

    return 0;
}
