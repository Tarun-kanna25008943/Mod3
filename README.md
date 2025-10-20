# EX-01 Program to Convert a Given Decimal Value to Binary Using Function (Without Arguments and Without Return Type)

## AIM:
To write a C program that converts a decimal number to its binary equivalent using a function without arguments and without return type.

## ALGORITHM:
1. Start
2. Declare variables: n, bin = 0, rem, pl = 1.
3. Read the decimal number n.
4. Store org = n.
5. Repeat while n > 0:
    a. rem = n % 2
    b. n = n / 2
    c. bin = bin + (rem * pl)
    d. pl = pl * 10
6. Print: org in decimal = bin in binary.
7. Stop

## PROGRAM:
```
#include <stdio.h>

int main()
{
    int n, bin = 0, rem, pl = 1;
    printf("Enter the decimal number: ");
    scanf("%d",&n);
    int org = n;
    
    while(n>0)
    {
        rem = n%2;
        n = n/2;
        bin = bin + (rem*pl);
        pl = pl * 10;
    }
    
    printf("%d in decimal = %d in binary",org,bin);
    return 0;
}
```
## OUTPUT:

<img width="660" height="122" alt="image" src="https://github.com/user-attachments/assets/64e92811-cef2-4cc7-bdfb-de507daf8f3d" />

## RESULT:

The program successfully converts a given decimal number into its binary equivalent using a function without arguments and without return type.

# EX-02 Program to Print Number Pattern

## AIM:
To write a C program to print the following number pattern:

3 3 3 3 3

3 2 2 2 3

3 2 1 2 3

3 2 2 2 3

3 3 3 3 3

## ALGORITHM:
1. Start
2. Declare integer variables i, j, and set n = 3.
3. First half of pattern:
    a. Repeat for i = n down to 2:
    b. Repeat for j = n down to 1:
    c. If j > i, print j, else print i.
    d. Repeat for j = 2 to n:
    e. If j > i, print j, else print i.
4. Move to the next line.
5. Second half of pattern:
6. Repeat for i = 1 to n:
7. Repeat same inner loops and conditions as above.
8. Move to the next line.
9. Stop

## PROGRAM:
```
#include<stdio.h>
int main()
{
    int i, j, n=3;
    
    for(i=n; i>1; i--)
    {
        for(j=n;j>=1;j--)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        for(j=2;j<=n;j++)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        printf("\n");
    }    
    for(i=1; i<=n; i++)
    {
        for(j=n;j>=1;j--)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        for(j=2;j<=n;j++)
        {
            if(j>i) printf("%d ", j);
            else printf("%d ", i);
        }
        printf("\n");
    }
    
    return 0;
}
```
## OUTPUT:

<img width="716" height="226" alt="image" src="https://github.com/user-attachments/assets/77381932-c7e3-425f-a80f-87b6e3817b89" />

## RESULT:
The program successfully prints the number pattern using nested loops and conditional logic to determine the value at each position based on its distance from the border.

# EX-03 Program to Print the Second Element of an Array

## AIM:
To write a C program that reads n integer elements into an array and prints the second element of the array.

## ALGORITHM:

1. Start
2. Declare an integer variable num.
3. Read the number of elements (num) from the user.
4. Declare an integer array arr[num].
5. Use a for loop from i = 0 to i < num:
     a. Read each element and store it in arr[i].
7. Print the second element of the array using arr[1].
8. Stop

## PROGRAM:
```
#include <stdio.h>

int main()
{
    int num;
    printf("Enter the size of the array: ");
    scanf("%d",&num);
    int arr[num];
    printf("Enter the elements: ");
	for(int i = 0; i<num; i++)
    {
        scanf("%d",&arr[i]);
    }
    printf("The second element of the arry is: %d",arr[1]);
    return 0;
}
```

## OUTPUT:
<img width="667" height="152" alt="image" src="https://github.com/user-attachments/assets/b24ae800-d346-419a-8b9f-40f0ee948bad" />

## RESULT:
The program successfully reads n integer elements from the user and prints the second element of the array.

# EX-04 Program to Print the Count of Even Numbers in an Array

## AIM:
To write a C program that reads elements into an array and prints the count of even numbers present in it.

## ALGORITHM:
1. Start
2. Declare an integer array arr[7] and a variable count = 0.
3. Use a for loop from i = 0 to 6:
    a. Read each element of the array using scanf().
4. Use another for loop from j = 0 to 6:
    a. If arr[j] % 2 == 0, increment count by 1.
5. After the loop ends, print "Even numbers: %d", count - 1.
6. Stop

## PROGRAM:
```
#include <stdio.h>
int main()
{
	int num;
	printf("Enter the size of array: ");
	scanf("%d",&num);
    int arr[num],count = 0;
    printf("Enter the array elements: ");
    for(int i = 0; i < num; i++)
    {
        scanf("%d",&arr[i]);
    }
    
    for(int j = 0; j < num; j++)
    {
        if(arr[j] % 2 == 0)
        {
            count++;
        }
    }
    printf("Even numbers: %d",count);
    return 0;
}
```
## OUTPUT:
<img width="659" height="149" alt="image" src="https://github.com/user-attachments/assets/9a315fe5-fadc-4105-9fa8-7614e4b8f379" />


## RESULT:
The program successfully counts and displays the total number of even numbers in the given array.

# EX-05 Program to Check Whether the First Element of an Array is Divisible by 3

## AIM:
To write a C program that reads n elements into an array and checks whether the first element is divisible by 3.

## ALGORITHM:

1. Start
2. Declare an integer variable num.
3. Read the value of num (size of the array) from the user.
4. Declare an integer array arr[num].
5. Use a for loop from i = 0 to i < num:
    a. Read each element and store it in arr[i].
6. Check if the first element arr[0] is divisible by 3 using the condition:
    a. If arr[0] % 3 == 0, print "The first element is divisible by 3".
    b. Else, print "The first element is not divisible by 3".
7. Stop

## PROGRAM:
```
#include <stdio.h>

int main()
{
    int num;
    printf("Enter the size of the array: ");
    scanf("%d",&num);
    int arr[num];
    printf("Enter the elemnts of the array: ");
    for(int i = 0; i < num; i++)
    {
        scanf("%d",&arr[i]);
    }
    if(arr[0] % 3 == 0)
    {
        printf("The first element %d is divisible by 3",arr[0]);
    }
    else
    {
        printf("The first element %d is not divisible by 3",arr[0]);
    }
    return 0;
}
```

## OUTPUT:
<img width="676" height="146" alt="image" src="https://github.com/user-attachments/assets/483c568e-eabe-4967-846f-7e3197643df9" />

## RESULT:
The program successfully reads n elements from the user and checks whether the first element of the array is divisible by 3.
