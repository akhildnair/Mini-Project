# Mini-Project
C Program to store Student's Information
#include <stdio.h>
struct student 
{
    char firstName[50];
    int roll;
    float marks;
} s[5];
int main() 
{
    int i;
    printf("Enter information of students:\n");
    for (i = 0; i < 5; ++i) {
        s[i].roll = i + 1;
        printf("\n For roll number: %d \n", s[i].roll);
        printf("Enter the First Name: ");
        scanf("%s", s[i].firstName);
        printf("Enter the marks scored: ");
        scanf("%f", &s[i].marks);
    }
    printf("Displaying Information:\n\n");
    for (i = 0; i < 5; ++i) 
    {
        printf("\n Roll number: %d\n", i + 1);
        printf("First name: ");
        puts(s[i].firstName);
        printf("Marks: %.1f", s[i].marks);
        printf("\n");
    }
    return 0;
}
