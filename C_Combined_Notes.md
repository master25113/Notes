# Day 1 - Basic of C programming

## My_Notes:
```
* # -> Preprocessor Directive 

* C is case sensitive

* Header File will compile first then after only code compile

* Basic Structure:
    #include<stdio.h>
    --Declare functions here {user defined functions}
    int main()
    {
        //code
    }

* printf("   ") -> print format

* int main(){
    return 0; 
  } // Send message to OS -> Successfully exceuted program without any error | int here is a Return Value | Said as Error Code

* Kamalraj Sir Gitlab link - https://git.selfmade.ninja/sibidharan/c-by-kamalraj

* Data Types: Number - Whole , Decimal | Characters - Single character, String(Group of chars)
    Whole - int 
    Decimal - float
    Single character - char
    Word (string) - char name[10]; //In C -> Word after whitespace it will end the string (ex:leo das | string=leo)

* About scanf
```

## Code:

### datatype.c
```  c
#include<stdio.h>
int main() {
    int x=10; //static intialization
    float X=2.5;
    char c='a'; //if single char - '' use single quote only
    char name[10]="leo dass"; //here double word output get because of static initilization
    char Name[7]="master"; //This line defines a char array of size 6, but you're trying to store the string "master", which has 7 characters (including the null terminator \0 that marks the end of a string)

    printf("x = %d\n",x);
    printf("X = %f\n",X);
    printf("X = %0.3f\n",X);
    printf("x = %c\n",c);
    printf("x = %s\n",name);
    printf("x = %s\n",Name);
}

/*  Output:
    x = 10
    X = 2.500000
    X = 2.500
    x = a
    x = leo dass
    x = master
*/
```

### hello.c 
``` c
#include<stdio.h>
int main() {
    printf("Hello World...\n");
    return 0;
    
}

/*  Output:
    Hello World...
*/
```

### scanf.c 
``` c
#include<stdio.h>
int main() {
    int x;
    float X;
    char ch;

printf("Enter the Integer value : ");
scanf("%d",&x);

printf("Enter the Float value : ");
scanf("%f",&X);

printf("Enter the Character : ");
scanf(" %c",&ch); //Added space before "%c" to skip leftover newline

printf("Entered Integer value is : %d \n",x);
printf("Entered Float value is : %f \n",X);
printf("Entered Character is : %c \n",ch);

    return 0;
}

/*  Output:
    Enter the Integer value : 5
    Enter the Float value : 7.5
    Enter the Character : Y
    Entered Integer value is : 5 
    Entered Float value is : 7.500000 
    Entered Character is : Y
*/ 
```

### scanf2.c 
``` c
#include<stdio.h>

int main() {
    int x;
    float y;
    char ch;

    printf("Enter int float char : ");
    scanf("%d %c %f",&x,&ch,&y);
    printf("You Entered int =%d , float =%c , char =%f",x,ch,y);
    return 0;
}

/*  Output:
    Enter int float char : 1a2.2
    You Entered int =1 , float =a , char =2.200000
*/
```

### scanf3.c
``` c
#include<stdio.h>
int main() {
    char c[10];
    printf("Enter characters : ");
    scanf("%s",c); //Here don't use ambescenr(&) &c because scaning string
    printf("You Entered characters are: %s",c);
}

/*  Output:
    Enter characters : leodass
    You Entered characters are: leodass
*/
```
  
### pre_post_increment.c
``` c
#include<stdio.h>
int main()
{
    int a=10;
    printf("a = %d\n",a++);
    printf("a after increment = %d\n",a);
    printf("a before increment = %d\n",++a);
}

/* Output:
    a = 10
    a after increment = 11
    a before increment = 12
*/
```


___
---
***



# Day 2 - Operator & Control Structures

## My_Notes:
```
* About Operators

* Arithematic Operators - Add + ,Sub - ,Multiply * ,Division / ,Modulo % (Remainder of Division)

* Bitwise Operators - AND &, OR |, XOR ^ & LEFT Shift <<, RIGHT Shift >>

* Bitwise Operators are used in Image Processing & Comparing
  LEFT SHIFT & RIGHT SHIFT Bitwise Operators are used in Encryption & Hashing

* Relational Operator - less than: < | greater than : > | less than or equal : <= | greater than equal : >= | not equal: != | both equal or not : == 

* Logical Operators - AND &&, OR ||, NOT !

* About Control Structures - Simple If, If Else, If Else If lader, Nested If
```

## Code:

### arithematic-operators.c 
``` c
#include<stdio.h>
    int main()
    {
        int a=25,b=1,c;

        c=a+b;
        printf("Sum of a & b: %d\n",c);
        printf("Sum of a & b: %d\n",a+b); //Use this way also, it is reduce memory
        printf("Difference of a & b = %d\n",a-b);
        printf("Multiplication: %d\n",a*b);
        printf("Quotient of a / b = %d\n",a/b);
        printf("Reminder of a/b = %d",a%b);
    }

/*  Output
    Sum of a & b: 26
    Sum of a & b: 26
    Difference of a & b = 24
    Multiplication: 25
    Quotient of a / b = 25
    Reminder of a/b = 0
*/
```

### bitwise-operators.c
``` c
/*Bitwise Operator:
    Bitwise AND &
    Bitwise OR |
    Bitwise xor ^
a = 60 Binary value=>  111100
b = 30 Binary value=>  011110

Bitwise AND a&b   =>   011100 (28)  [Two side 11 => 1]
Bitwise OR   a|b  =>   111110 (62)  [Two side 11 or 01 or 10 => 1]
Bitwise xor  a^b  =>   100010 (34)  [Two side 00 or 11 => 0] 

Left shift c = 6,  c<<2, 0110 => 11000 (24)
Right shift : c=6, 0110, c>>3 => 0000 (0)
*/

#include<stdio.h>
int main() {
    int a=60,b=30,c=6;
    printf("Bitwise AND a & b = %d\n",a&b);
    printf("Bitwise OR a or b = %d\n",a|b);
    printf("Bitwise xor a ^ b = %d\n",a^b);
    printf("Left shift op res = %d\n",c<<2);
    printf("Rightshift result = %d\n",c>>3);
}

/*  Output:
    Bitwise AND a & b = 28
    Bitwise OR a or b = 62
    Bitwise xor a ^ b = 34
    Left shift op res = 24
    Rightshift result = 0
*/
```

### if_else_if-controlstrucutre.c
``` c
/*
if(condtion1)
{

}
else if(condition2)
{

}
else if(condition3)
{

}
else{

}*/


#include<stdio.h>
int main()
{
    int a;
    printf("Enter a number: ");
    scanf("%d",&a);
    if(a>0)
    {
        printf(" +ve ");
    }
    else if(a<0)
    {
        printf(" -ve ");
    }
    else
    {
        printf("Given is zero");
    }
}

/*  Output:
    Enter a number: 3
    +ve
*/
```

### ifelse-controlstructure.c 
``` c
#include<stdio.h>
int main()
{
    int a=5;
    if(a<10){
        printf("Yes a is < 10");
    }
    else{
        printf("a is not less than 10");
    }
}

/*  Output:
    Yes a is < 10
*/
```

### logical-operators.c
``` c
/*Logical operators: Output in Only Boolean (0/1) 
    AND op:  &&   ex: a&&b [Both values are non zero values => True (1)]
    OR op:   ||   ex: a||b [Both values are zero values => (0)]
    NOT op:   !   ex:  !(a<b) [Change value by opposite value(Negation), Ex: 1 means 0 | 0 means 1]
*/

#include<stdio.h>
int main()
{
    int a=2,b=4;
    printf("a&&b = %d\n",a&&b);
    printf("a || b = %d\n",a||b);
    printf("!(a<b) = %d\n",!(a<b));
}

/*  Output:
    a&&b = 1
    a || b = 1
    !(a<b) = 0
*/
```

### relational-operators.c
``` c
    /*
    Relational operators
    less than:  <
    greater than : >
    less than or equal : <=
    greater than equal : >=
    not equal:    !=
    both equal or not :  == 
    */

    #include<stdio.h>
    int main()
    {
        int a=6, b=4;
        printf("A==B = %d\n", a==b);
        printf("A<B=%d\n",a<b);
        printf("A>B = %d\n",a>b);
        printf("A!=B %d",a!=b);
    }

    /*  Output:
        A==B = 0
        A<B=0
        A>B = 1
    /*
```

### simple_if-controlstructure.c
``` c
    /*control structures:
        if(condition){
            //if condition true
            //what to do
        }
    */

    #include<stdio.h>
    int main(){
        int a=10,b=10;
        if(a==b)
        {
            printf("Yes both a & b are equal\n");
        }
    }

    /*  Output:
        Yes both a & b are equal
    */
```



___
---
***



# Day 3 (P1 & P2)- Control Structures 

## My_Notes:
```
* About If elese if: 
    if(choice==1) {
        ....
    }
    else if(choice==2) {
       ....
    }
    else {

    }

* About Swich case:
    swich(choice) {
        case 1:
            //add
            break;
        case 2:
            //sub
            break;
        default:
            Error:message
            break;  
    }

* About ifelse inside use parent & child conditions

* About Nested Control Structure - Parent if condition Inside Child if condition 

* Loop Structure - Iterative (Repeatative)
    - do while Loop
        do{
            printf{"Hello"}
        }while(0); //Here 0 means it print 1th time
    
    - while Loop
        while(0){
            printf{"Hello"} //Here 0 means it will not print because entry is zero
        }

    - for loop
        for(condition){

        }

* About Increment operator & Decrement operator
    a=a+1;

* For loop 
    for(start:range;incr/decr) {
        ....
    }

* About While loop in side switch
```

## Code:

### do_while & while loop.c
``` c
#include<stdio.h>
int main()
{
    do{
        printf("I am from do..while");
    }while(0);
    
    //entry condition verification
    while(0)
    {
        printf("I am from while");
    }
} 

/* Output
    I am from do..while
*/
```

### elseif.c
``` c
#include<stdio.h>

int main() {
    int choice,a,b;

    printf("1 -> Addition\n2 -> Difference\n3 ->Multiplication\n4 -> Division\n");
    printf("Enter your Choice : ");
    scanf("%d",&choice);
    printf("Enter the values of a & b : ");
    scanf("%d%d",&a,&b);

    if(choice==1) {
        printf("Addition of a & b = %d",a+b);
    }
    else if(choice==2) {
        printf("Difference of a & b = %d",a-b);
    }
    else if(choice==3) {
        printf("Multiplicatio of a & b = %d",a*b);
    }
    else if(choice==4) {
        if(b!=0) {
            printf("Division of a & b = %d",a/b);
        }
        else {
            printf("Error: Division by zero is not allowed");
        }
    }
    else {
        printf("Error : You Enter Wrong Value");
    }

}

/*  Output:
    1 -> Addition
    2 -> Difference
    3 ->Multiplication
    4 -> Division
    Enter your Choice : 1
    Enter the values of a & b : 10
    20
    Addition of a & b = 30
*/
```

### for_loop.c
``` c
#include<stdio.h>

int main() {
    int a=1;
    int range;
    printf("Enter no of time execute : ");
    scanf("%d",&range);
    for(a=1;a<=range;a=a+1) {
        printf("value: %d\n",a*5);
    }
}

/* Output:
    Enter no of time execute : 5
    value: 5
    value: 10
    value: 15
    value: 20
    value: 25
*/
```

### ifelse_parent&child.c
``` c
#include<stdio.h>
int main()
{
    int a;
    printf("Enter a value: ");
    scanf("%d",&a);
    if(a>0 && a<=10)
    {
            printf("a is within 0 to 10");
    }
    else
    {
            printf("a is not within range 0 to 10");
    }
    if(a<0)
    {
    printf("a is negative");      
    }

}

/* Output:
    Enter a value: 5
    a is within 0 to 10
*/
```

### switchcase.c
``` c
#include<stdio.h>

int main() {
    char choice;
    int a,b;
    printf("+ -> Addition\n- -> Difference\n* ->Multiplication\n/ -> Division\n");
    printf("Enter your Choice : ");
    scanf("%c",&choice);
    printf("Enter the values of a & b : ");
    scanf("%d %d",&a,&b);
    switch(choice) {
        case '+':
            printf("Add of a & b = %d",a+b);
            break;
        case '-':
            printf("Sub of a & b = %d",a-b);
            break;
        case '*':
            printf("Multi of a & b = %d",a*b);
            break;
        case '/':
            printf("Div of a & b = %d",a/b);
            break;
        default:
            printf("Error: Division by zero is not allowed");
            break;    
    }
}

/*  Output:
    + -> Addition
    - -> Difference
    * ->Multiplication
    / -> Division
    Enter your Choice : /
    Enter the values of a & b : 10
    2
    Div of a & b = 5
*/
```

### while_loop.c
``` c
#include<stdio.h>
int main() {
    int a =1;
    while(a<=10) {
        printf("value: %d\n",a*10);
        a=a+1;
    }
}


/* Output:
    value: 10
    value: 20
    value: 30
    value: 40
    value: 50
    value: 60
    value: 70
    value: 80
    value: 90
    value: 100 
*/
```

### while_loop2.c
``` c
#include<stdio.h>
int main() {
    int a=1;
    int range;
    printf("Enter no of time execure : ");
    scanf("%d",&range);
    while(a<=range) {
        printf("value: %d\n",a*10);
        a=a+1;
    }
    printf("a = %d",a);
}


/* Output:
    Enter no of time execure : 10
    value: 10
    value: 20
    value: 30
    value: 40
    value: 50
    value: 60
    value: 70
    value: 80
    value: 90
    value: 100
    a = 11
*/
```

### while_loop3.c
``` c
#include<stdio.h>
int main() {
    int input;
    int digit;
    printf("Enter a number : ");
    scanf("%d",&input);
    while(input>0) {
        digit=input%10;
        printf("lsd : %d\n",digit);
        input=input/10;
        printf("Input:%d and Digit:%d\n",input,digit); //this for checking purpose
    }

}

/* Output
    Enter a number : 20
    lsd : 0
    Input:2 and Digit:0
    lsd : 2
    Input:0 and Digit:2
*/
```

### whileloop_inside_switch.c
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int x,y;
    int choice;
    while(1){
    printf("\n(1) => addition\n(2) => subtraction\n(3) => Exit");
    printf("Enter your choice(+ or -): ");
    scanf("%d",&choice);
    if(choice<3)
    {
        printf("Enter values for x & y: ");
        scanf("%d%d",&x,&y);
    }
    switch(choice)
    {
        case 1:
            printf("Add  x & y =%d\n",x+y);
            break;
        case 2:
            printf("diff x & y = %d\n",x-y);
            break;
        case 3:
            exit(1); // (or) return 0;  --> to exit switch
        default:
            printf("Error: choice can be + or -\n");
            break;
    }
    }
}

/*Output:
    (1) => addition
    (2) => subtraction
    (3) => ExitEnter your choice(+ or -): 1
    Enter values for x & y: 2
    4
    Add  x & y =6

    (1) => addition
    (2) => subtraction
    (3) => ExitEnter your choice(+ or -): 3
/*
```



___
---
***



# Day 4 - Array

## My_Notes:
```
* Arrays - Collection of similar types of element
    Reason for Array using 
        sum of 2 integers : int a,b; | a+b;
        sum of 20 integers : int a,b,c,d,e,f,g,h.....
        To avoid this uisng Array

* Array types - 1 Dimensional Array, 2 Dimensional Array, 3 Dimensional Array

* Array syntax - data_type Array_name[max_size];
    int a[10]; | char test[15];

* Static initilization in Array
    int a[5] = {11,12,13,14,15}; //index start from 0 by default | a[0]=11

* About Dynamic initilization

* About 1 Dimensional Array, 2 Dimensional Array, 3 Dimensional Array
    a[10][10];

* About Char Array - (Day1 class's Doubt)
```

## Code:

### 2d_dynamic-array.c 
``` c
/*
Looping with a[i][j]:
i = 0 → j = 0,1,2 → print 1 2 3
i = 1 → j = 0,1,2 → print 4 5 6
i = 2 → j = 0,1,2 → print 7 8 9

Looping with a[j][i]:
i = 0 → j = 0,1,2 → print a[0][0], a[1][0], a[2][0] → 1 4 7
i = 1 → j = 0,1,2 → print a[0][1], a[1][1], a[2][1] → 2 5 8
i = 2 → j = 0,1,2 → print a[0][2], a[1][2], a[2][2] → 3 6 9
*/

#include<stdio.h>
int main(){
    int a[3][3];
    int i,j;
    printf("Enter values for 3x3 matrix: ");
    for(i=0;i<3;i++) {
        for(j=0;j<3;j++)
            scanf("%d",&a[i][j]);
    }
    printf("\n Enter Input for matrix : \n");
    printf("Matrix A:\n");
    for(i=0;i<3;i++) {
        for(j=0;j<3;j++)
            printf("%d\t",a[i][j]);
            printf("\n"); 
        }
    
    printf("Transverse Matric of A:\n");
    for(i=0;i<3;i++) {
        for(j=0;j<3;j++)
            printf("%d\t",a[j][i]);
            printf("\n");
        }
}

/* Output:
    Enter values for 3x3 matrix: 1 2 3 4 5 6 7 8 9

    Enter Input for matrix : 
    Matrix A:
    1       2       3
    4       5       6
    7       8       9
    Transverse Matric of A:
    1       4       7
    2       5       8
    3       6       9

            (Or) 

    Enter values for 3x3 matrix: 1
    2
    3
    4
    5
    6
    7
    8
    9

    Enter Input for matrix : 
    Matrix A:
    1       2       3
    4       5       6
    7       8       9
    Transverse Matric of A:
    1       4       7
    2       5       8
    3       6       9
*/
```

### 2d_static-array.c
``` c
#include<stdio.h>
int main()
{
    int a[4][4] = {{10,11,12,13},{20,21,22,23},{10,11,12,13},{20,21,22,23}};
    int r,c;
    printf("The 2D array values :\n");
    for(r=0;r<4;r++)
    {
        for(c=0;c<4;c++)
                printf("%d\t",a[r][c]);
        printf("\n");
    }

} 

/* Output:
    The 2D array values :
    10      11      12      13
    20      21      22      23
    10      11      12      13
    20      21      22      23
*/
```

### arr1_static initialization.c
``` c
#include<stdio.h>
int main()
{
    //static initialization
    int a[5] = {10,1,2,35,6};
    int b[5] = {11,12,13,14,15};
    int i;
    printf("The values are : \n");
    for(i=0;i<5;i++) {
        printf("value[%d] = %d\n",i,a[i]);
        printf("value[%d] = %d\n",i,b[i]);
    }
}

/* Output:
The values are : 
value[0] = 10
value[0] = 11
value[1] = 1
value[1] = 12
value[2] = 2
value[2] = 13
value[3] = 35
value[3] = 14
value[4] = 6
value[4] = 15
*/
```

### arr2_Dynamic-initialization.c
``` c
#include<stdio.h>
int main()
{
    int x[50],i,max;
    printf("Enter the max no.of values to insert : ");
    scanf("%d",&max);
    printf("Enter the values : \n");
    for(i=0;i<max;i++)
        scanf("%d",&x[i]);
    printf("The given values are : \n");
    for(i=0;i<max;i++)
        printf("%d\t",x[i]);
}

/* Output:
    Enter the max no.of values to insert : 5
    Enter the values : 
    10
    20
    30
    40
    50
    The given values are : 
    10      20      30      40      50      
*/
```

### charArray.c
``` c
#include<stdio.h>
int main()
{
    char c[10];
    int i;
    printf("Enter the 5 chars : \n");
    for(i=0;i<5;i++) {
        scanf("%c",&c[i]);
    }
    c[i]='\0'; // It Marks End of string
    printf("given input is : %s",c);
}

/* Output:
    Enter the 5 chars : 
    kamal
    given input is : kamal
*/
```

### parent_child loop.c
``` c
#include<stdio.h>
int main()
{
    int i=3,j=2;
    for(i=0;i<3;i++)
    {
        printf("\n-------------------------\n");
        printf("I am from parent: %d\n",i);
        for(j=0;j<2;j++)
        {
            printf("I am from child: %d\n",j);
        }
        printf("\n----------------------------\n");
    }
}

/* Output:

    -------------------------
    I am from parent: 0
    I am from child: 0
    I am from child: 1

    ----------------------------

    -------------------------
    I am from parent: 1
    I am from child: 0
    I am from child: 1

    ----------------------------

    -------------------------
    I am from parent: 2
    I am from child: 0
    I am from child: 1

    ----------------------------
*/
```

### readString.c
``` c
#include<stdio.h>
int main()
{
    char s[10];
    printf("Enter your name: ");
    scanf("%s",s);
    printf("\nname : %s",s);
}

/* Output:
    Enter your name: leo

    name : leo
*/
```

### fullname.c
``` c
#include<stdio.h>
int main()
{
    char str[30];
    printf("Enter a fullname :");
    scanf("%[^\n]",str); // %[^\n] --> Format specifier is used with scanf to read a line of text including spaces and stop at a newline (\n)
    printf("Your name: %s",str);
}

/* Output:
    Your name: kabil yugan
*/
```



___
---
***



# Day 5 - User Defined Datatypes

## My_Notes:
```
* About int to string Convert by function sprintf
    sprintf has 3 arguments - sprintf(target_string_variable, source-variable_format_specifier, source_variavle)

* About string to int by atoi
     x = atoi(inp); //atoi - alaphabet to interger

* About Structure - It is used Create our own Datatypes 
    struct keyword
    why we use our own Datatypes: ex Point(x,y) | p1+p2 instead of ((x1+y1)+(x2+y2))

* DOT(.) Operator to access struct elements
    P1.x = 10 | P1.y = 100

* About Union => Similar to Structure | It is used in embedded systems
    In Union - Memory is constraint | it shares memoryand and which datatypes is largest that share memory to smallest
    Real world ex - I have biriyani(80 size),fried rice(70),veg poriyal(20)
                    But Plate size small so eat one by one only : 
                    eat biriyani next eat fried rice next veg poriyal OR eat biriyani with veg poriyal

                    In structure : eat all | In Union : eat one by one by size of plate

* Doubts Clear :
    (1) int a[] = {10,20,30,40,50} | b[] = {10,30,40,50} | How to find one element is missing in b?
        Simple way : sum(a)-sum(b) => 150-130 = 20
    (2) char a[] = {k,a,b,i,l} | b[] = {k,b,i,l} | How to find one element is missing in b?
        Similar to above answer but here find by ASCE value way 
```

## Code:

### stringToint.c
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    char inp[]="234";
    int x;
    x = atoi(inp); //atoi - alaphabet to interger
    x = x * 10; // conveted number to multiply
    printf("Converted data : %d",x);
}

/* Output:
    Converted data : 2340
*/
```

### intToString.c
``` c
#include<stdio.h>
#include<stdlib.h> //old complier need this headerfile
int main() {
    char buf[10]; // create char arrary[]
    int x;
    printf("Enter a value: ");
    scanf("%d",&x);
    sprintf(buf,"%d",x); // string print - print data to a string variable buff[10] 
    printf("x value in string: %s",buf);
}

/* Output:
    Enter a value: 12334
    x value in string: 12334
*/
```

### structure.c
``` c
#include<stdio.h>
struct Point{
    int x,y; //Struct element
}P3; //here also initilize variables

int main()
{
    struct Point P1,P2,P3;  //variables and here also initilize variables
    P1.x= 20;
    P1.y = 30;
    P2.x = 40;
    P2.y = 60;
    P3.x = P1.x + P2.x;
    P3.y = P1.y + P2.y;
    printf("P3 (x,y) : %d,%d",P3.x,P3.y);
}

/* Output:
    P3 (x,y) : 60,90
*/
```

### structure_carry.c
``` c
#include<stdio.h>
struct Point{
    int x,y;
};

int main()
{
    struct Point p[3];
    int i;
    for(i=0;i<3;i++) {
        printf("Enter x & y values: ");
        scanf("%d%d",&p[i].x,&p[i].y);
    }
    p[2].x = p[0].x + p[1].x;
    p[2].y = p[0].y + p[1].y;

    for(i=0;i<3;i++)
    {
        printf("P%d (x,y) is : %d,%d\n",i,p[i].x,p[i].y);
    }
    //printf("P[2] is (x,y) : %d, %d",p[2].x,p[2].y);
}

/* Output:
Enter x & y values: 1 2
Enter x & y values: 2 3
Enter x & y values: 4 5
P0 (x,y) is : 1,2
P1 (x,y) is : 2,3
P2 (x,y) is : 3,5 // Add of P1,P2
*/
```

### union.c
``` c
#include<stdio.h>
struct Dt1 {
    int x;
    char s[40];
};
union Dt2 {
    int x;
    char s[40];
};
int main()
{
    struct Dt1 sd1;
    union Dt2 ud2;
    printf("size of Dt1 (struct): %ld bytes\n",sizeof(sd1));
    printf("size of Dt2 (union): %ld bytes",sizeof(ud2));
}

/* Output:
    size of Dt1 (struct): 44 bytes //Struture - int 4 bytes + char 40 bytes = 44 bytes
    size of Dt2 (union): 40 bytes  //Union -int 4 bytes + char 40 bytes = it takes largest size char 40 bytes and it inside it allocate int 4 bytes
*/ 
```



___
---
***



# Day 6 - Pointers

## My_Notes:
```
* About Pointers
    - It is address of data | Accessing Physical address of data | variable is just lable 
    - int *P; -> pointer to int
      p=&a; // & abescent symbol is refernce operator
      P=&a; //Here we give "only starting address" of data to poniter variable P
      *P -> Content of Physical address
      P -> Physical address of Content
      ptr - address 
      *ptr - data
    - Physical memory - here RAM
```
    
## Code:

### pointer1.c
``` c
#include<stdio.h>
int main() {
    int a = 10;
    int *ptr;
    ptr = &a;
    printf("Data in ptr is %d\n",*ptr);
    printf("Address of a : %p\n",&a);
    printf("Address of a unsing ptr: %p\n",ptr); // %p => it is format specifier and it is used fot print memory addresess
    *ptr = *ptr * 20; //We modify data in physical address
    printf("Modified value of a %d\n",a);
    return 0;
}

/* Output:
    Data in ptr is 10
    Address of a : 0x7ffffe8c8064
    Address of a unsing ptr: 0x7ffffe8c8064
    Modified value of a 200
*/
```

### char_pointer.c
``` c
#include<stdio.h>
int main()
{
    char c[] = {'k','a','m','a','l'};
    char *ptr;
    int i;
    ptr = c;
    for(i=0;i<5;i++)
    {
        printf("%c char in %p \n",*ptr,ptr);
        ptr = ptr + 1;
    }
}

/*Output:
k char in 0x7ffff917760f 
a char in 0x7ffff9177610 
m char in 0x7ffff9177611 
a char in 0x7ffff9177612 
l char in 0x7ffff9177613 
*/
```

### pointer_arrary.c
``` c
#include<stdio.h>
int main()
{
    int a[] = {10,23,33,43};
    int *pt,i;
    pt = a; // pt=&a; In here you get error ,so & symbol not needed in array elements assign to pointer
    for (i=0;i<4;i++) {
        printf("%d data in address %p\n",*pt,pt); // *py[i],pt[i] - in here you get error , so use this *pt,pt | pt = pt + 1;
        pt = pt + 1;
    }
    return 0;
}

/* Output:
    10 data in address 0x7ffede6a16a0
    23 data in address 0x7ffede6a16a4
    33 data in address 0x7ffede6a16a8
    43 data in address 0x7ffede6a16ac
*/ 
```

### pointer_testing-intANDchar.c
``` c
#include<stdio.h>
int main() {
    int a = 10;
    char c = 'k';
    int *p;
    char *cp;
    p = &c; //In here we give char value to int pointer
    cp = &a; //In here we give int value to char pointer
    printf("Data in int pointer p : %c in address %p\n",*p,p);
    printf("Data in int pointer p : %d in address %p",*cp,cp);
    return 0;
}

/* Output:
    Data in int pointer p : k in address 0x7ffc19f9900b
    Data in int pointer p : 10 in address 0x7ffc19f9900
*/
```

### pointer_testing2-intANDchar.c
``` c
#include<stdio.h>
int main() {
    int a[] = {10,20};
    char c = 'k';
    int i;
    int *p;
    char *cp;
    p = &c; //In here we give char value to int pointer
    cp = &a; //In here we give int value to char pointer
    printf("Data in int pointer p : %c in address %p\n",*p,p);
    for(i=0;i<2;i++) {
        printf("Data in int pointer p : %d in address %p\n",*cp,cp);
        cp = (char*) ((int*) cp+1); //casts the char* pointer cp to an int* to move the pointer by 4 bytes (size of int), then casts it back to char* to continue processing byte-by-byte.
        //cp = cp + 4; // or use this for above line AND Don't use this because can't get 3rd index value
    }
    return 0;
}

/* Output:
    Data in int pointer p : k in address 0x7ffcfdce1e8f
    Data in int pointer p : 10 in address 0x7ffcfdce1e90
    Data in int pointer p : 20 in address 0x7ffcfdce1e94
*/
```



___
---
***



# Day 7 - Functions

## My_Notes:
```
* About Function
    Fuction - Block of code for doing particular task
    Modular Programming
    Reuse Code & Repeative code or same line of code move into block of code 
    Reduce size and length

* Function Model to Main() 
    Functions with inputs and returns value
    Functions with inputs and no returns value
    Functions without inputs and returns value
    Functions without inputs and no returns value

* Syntax for function declaration
    return_type function_name (inputs);

* Flow of Fuction : Top Down Programming approach
    Declaration particular
    main() inside call part
    after main() defintion part (define) function 

    Ex : 
        void display(); //Void => No Return Values
        main(){
            display;
        }
        void display(){
            printf("Hello");
        }

* Call by reference - Fuction is called by passing address of variables
    check programcallbyref.c

* For swapping - Call by reference is used
   - swap using temporal variable
        swap x,y 
        t=10,x=15,y=10
        t=x //t=15
        x=y //x=10
        y=t //y=15
        swapped x=10,y=15

    - without temp variable
        x=10,y=15
        x=x+y=>25
        y=x-y=>5
        x=x-y=>25-10=15
```

### Code:

### function1.c
``` c
//Top Down Programming
#include<stdio.h>
void display();
int main()
{
    display();
}
void display() //no inputs no return values
{
    printf("Hello World!...");
    
}


/* Bottom Up Programming
    #include<stdio.h>
    //no inputs no return values
    void display()
    {
        printf("Hello World!...");
        
    }
    int main()
    {
        display();
    }
*/

/* Output
    Hello World!...
*/
```

## function2.c
``` c
#include<stdio.h>
    //input but no return values from function
    //function definition
    void multi_table(int x)
    {
        int i;
        for(i=1;i<=15;i++)
        {
            printf("%d  x  %d  =  %d\n",i, x, i * x);
        }
    
    }
    int main()
    {
        int n;
        printf("Enter a value for multiplication table: ");
        scanf("%d",&n);
        multi_table(n);  // function call statement
    }

    /* Output:
        Enter a value for multiplication table: 5
        1  x  5  =  5
        2  x  5  =  10
        3  x  5  =  15
        4  x  5  =  20
        5  x  5  =  25
        6  x  5  =  30
        7  x  5  =  35
        8  x  5  =  40
        9  x  5  =  45
        10  x  5  =  50
        11  x  5  =  55
        12  x  5  =  60
        13  x  5  =  65
        14  x  5  =  70
        15  x  5  =  75
    */
```

### function3.c
``` c
//funtion has no inputs but return a value
#include<stdio.h>
int addition()
{
    int x,y;
    printf("Enter two values : ");
    scanf("%d%d",&x,&y);
    return x+y;
}
int main()
{
    //int res = addition();  //use down for reduce memory
    printf("Addition of two numbers: %d\n",addition());
}

/* Output
    Enter two values : 3
    4
    Addition of two numbers: 7
*/
```

### function4.c
``` c
//function gets input and return values
#include<stdio.h>
int z;  //global var
void mulitiplication(int x,int y)
{
// x & y are local variables
    z = x*y;
}
void addition(int x,int y)
{
    z = x + y;
}

int main()
{
    int a,b;
    printf("Enter two values: ");
    scanf("%d%d",&a,&b);
    mulitiplication(a,b);
    printf("Multiplication result: %d\n",z);
    addition(a,b);
    printf("Addition result: %d",z);
}

/* Output
    Enter two values: 5 10 
    Multiplication result: 50
*/
```

### call_by_ref.c 
``` c
#include<stdio.h>
void modify(int *p) //here No content & declation of pointer variable *p only
{
    *p = *p * 10; //*p -> content of x
    printf("address in p: %p\n",p);
}
int main()
{
    int a=10;
    modify(&a); //assign p=&a and here only address is going
    printf("\naddress of a: %p\n",&a);
    printf("\na = %d",a);
}

/* Output
    address in x: 0x7ffc19f7a7bc

    address of a: 0x7ffc19f7a7bc
*/
```

### swap_callByref.c
``` c
#include<stdio.h>
void swap(int *p,int *p1)
{
    int t;
    t = *p;
    printf("T = %d\n",t);
    *p = *p1;
    *p1 = t;
}
int main()
{
    int a=10,b=15;
    printf("Before swap : a = %d \t b = %d\n",a,b);
    swap(&a,&b);
    printf("After swap : a = %d \t b = %d\n",a,b);
}

/* Output
    Before swap : a = 10     b = 15
    T = 10
    After swap : a = 15      b = 10
*/
```



___
---
***



# Day 8 - Dynamic Memory Allocation

## My_Notes:
```
* (D7's Concept)
    * About Fuction_Array Program

    * About Array&Pointers in Function (Program - arrayANDpointerINfunction.c)
        *(p+i)  = *(p + i) * 10;
        p[i] = p[i] * 10;
        array = pointer are same in array (For indexing)

    * About Assignment - Password Checker  (Assig-passCheck.c)

* About DMA - Dynamic Memory Allocation
    - During Runtime Allocating Memory
    In static 
        int a[50]; | 30 elements <50 | => 20 elements Memory Waste
    In Dynamic 
        We go with Pointer
        Recuirement - Library Functions
            malloc(size) - here we give 1 argument that is size
            calloc(size,pointer) - here we give 2 argument that is size & Pointer
            realloc(size,pointer) - same as calloc()
            free() - Deallocate the Memory

* Differnce Between malloc and calloc (program - diffmc.c)
    In Theory calloc when no input given it initialize value of 0

* About realloc - rellocate the memory
```


## Code:

### func_array.c 
``` c
#include<stdio.h>
int size; // global var
void fun(int arr[])
{
    int i;
    for(i=0;i<size;i++)
        printf("%d\t",arr[i]);
}

int main()
{
    int a[30],i;
    printf("Enter the no.f of elements to process: ");
    scanf("%d",&size);
    printf("Enter the values: ");
    for(i=0;i<size;i++)
        scanf("%d",&a[i]);
    fun(a);
}

/* Output
    Enter the no.f of elements to process: 4
    Enter the values: 10 20 30 40 50 60
    10      20      30      40     
*/
```

### arrayANDpointerINfunction.c
``` c
    #include<stdio.h>
    int i;
    void updatearr(int *p)
    {
        //int i;
        printf("starting address: %p\n",p);
        for(i=0;i<4;i++)
        {
            *(p+i)  = *(p + i) * 10;
            //p[i] = p[i] * 10;
        }
    }
    int main()
    {
        int a[] = {1,2,3,4,5};
        //int i;
        printf("address of a = %p\n",&a[0]);
        updatearr(a);
        for(i=0;i<5;i++)
            printf("%d\t",a[i]);
    }

    /* Output
        address of a = 0x7ffd7e0cc2e0
        starting address: 0x7ffd7e0cc2e0
        10      20      30      40      5      
    */
```

### mallocp.c
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int *p;// int p[50] has large memory, here we save memory by Pointer to dynamically allocated array
    int noe,i;
    printf("Enter the no. of elements: ");
    scanf("%d",&noe);
    p = (int *) malloc(noe*sizeof(int)); // (int *): This is a typecast. malloc returns a void * (a generic pointer), and we need to tell the compiler that we want it to be treated as a pointer to integers (int *).
    printf("size of p = %ld\n",sizeof(*p));
    printf("Enter the values: ");
    for(i=0;i<noe;i++)
        scanf("%d",&p[i]);
    printf("values in array: \n");
    for(i=0;i<noe;i++)
        printf("%d\t",*(p+i));
    
}

/* Output
    Enter the no. of elements: 5
    size of p = 4
    Enter the values: 10 20 30 40 50 60
    values in array: 
    10      20      30      40      50
*/
```

### callocp.c 
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int *p;
    int noe,i;
    printf("Enter the no. of elements: ");
    scanf("%d",&noe);
    p = (int *) calloc(noe,sizeof(int));
    printf("Enter the values: ");
    for(i=0;i<noe;i++)
        scanf("%d",&p[i]);
    printf("values in array: \n");
    for(i=0;i<noe;i++)
        printf("%d\t",*(p+i));
    
}

/* Output
    Enter the no. of elements: 4
    Enter the values: 10
    30
    40
    50
    values in array: 
    10      30      40      50     
*/
```

### diffmc.c
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int *p,*p1;
    int i;
    p = (int *)malloc(8*sizeof(int));
    p1 = (int *)calloc(8,sizeof(int));

    printf("\nValues in malloc *p \n");
    for(i=0;i<8;i++)
        printf("%p\t",p[i]);

    p = (int *)realloc(p,10*sizeof(int));  // 8 to 10 by increase
    printf("\nAfter reallocation of malloc*p\n");
    for(i=0;i<10;i++)
        printf("%p\t",p[i]);
    free(p);

    printf("\nValues in calloc *p1\n");
    for(i=0;i<8;i++)
        printf("%p\t",p1[i]);
        printf("\n");
}

/* Output
    Values in malloc *p 
    (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)
    After reallocation of malloc*p
    (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)
    Values in calloc *p1
    (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)   (nil)
*/
```

### Assig-passCheck.c
``` c
#include <stdio.h>
#include <string.h>
#include <unistd.h>
#include <ctype.h>
#include <stdlib.h>

void passcheck();
int getpasswordvisiblility();
void getpassword();
int uppercase();
int lowercase();
int number();
int specialcharacter();
int Sequence();


//variable declartion
char password[100];
char passwordvisibleinput[100];
char warning[100];
int passwordvisible = 1;
int run=1;
int i;

//main function 
int main() {
printf("\n\n\t\tWelcome to the password checker\n\n\n");
while (run==1){
    strcpy(warning,"");
    if (getpasswordvisiblility()) {
    strcat(warning, "warning:\n\n");
    getpassword();
    passcheck();
    uppercase();
    
    
    }
    
}
    
} 

void passcheck(){
if(strlen(password) < 8) {
    printf("\n\n # ---- Very Weak\n\n");
    strcat(warning, "--> Password Length is lesser than 8\n");
}

else if (!uppercase() || !lowercase() || !number() || !specialcharacter())
printf("\n\n# ---- Weak\n\n");
else if (Sequence(1) || Sequence(0))
printf("\n\n# ---- Average\n\n");
else {
    printf("\n\n# ---- Very Strong\n\n");
    exit(1);
}
}


int getpasswordvisiblility(){
printf("visible the password in console ? (y/n): ");
scanf("%s",passwordvisibleinput);
if (strcmp(passwordvisibleinput,"y")==0){
    passwordvisible=1;
    return 1;
}
else if (strcmp(passwordvisibleinput,"n")==0){
    passwordvisible=0;
    return 1;
}
else
{
    printf("\n\ninvalid input\n\n");
    exit(0);
    

}  
    
}

void getpassword(){
if (passwordvisible){
    printf("enter the password :");
    scanf("%s",password);
}
else
{
    char *password = getpass("\nenter the password");
}

}
int uppercase(){
int upper=0;
for(int i=0; i<=strlen(password); i++){
    if(isupper(password[i])){
    upper=1;
    break;
    }

}
if(!upper){
    strcat(warning,"--> Upper case letteris missing\n");
}
}
int lowercase() {
int lower = 0;
for (int i=0; i <= strlen(password); i++) {
    if(islower(password[i])) {
    lower = 1;
    break;
    }
}
if(!lower)
strcat(warning, "--> Lower case letter is missing\n");
return lower;
}

int number(){
int num=0;
for ( i = 0; i <=strlen(password); i++)
{
    if(isdigit(password[i])){
    num=1;
    break;
    }
}
if(!num)
strcat(warning,"--> Number is missing\n");
return num;

}
int specialcharacter() {
int special_character= 0;
for (int i=0; i <= strlen(password); i++) {
    int ascii = (int)password[i];
    if(
        ( ascii >= 32 && ascii <= 47 ) ||
        ( ascii >= 58 && ascii <= 64 ) ||
        ( ascii >= 91 && ascii <= 96 ) ||
        ( ascii >= 123 && ascii <= 126 )) {
        special_character = 1;
        break;
        }
        }
        if(!special_character)
        strcat(warning, "--> Speical character is missing\n");
        return special_character;
}

int Sequence(int onlyDigit) {
int sequence2 = 0, sequence3 = 0, is_sequence = 0, old_number;
for (int i=1; i <= strlen(password); i++) {
    if(onlyDigit == isdigit(password[i]) || onlyDigit == 0) {
    if(sequence3) {
        is_sequence = 1;
        strcat(warning, "--> Avoid Sequence of Numbers or characters\n");
        break;
        }
        old_number = (int) password[i-1];
        if(old_number - (int)password[i] == 1 ||
        old_number - (int)password[i] == -1) {
            if(sequence2 == 1) {
            sequence3 = 1;
            }
            else {
                sequence2 = 1;
                }
        }
    }
    }
        return is_sequence;
}


/* Output


                Welcome to the password checker


visible the password in console ? (y/n): y
enter the password :leo


# ---- Very Weak

visible the password in console ? (y/n): y
enter the password :#Leo25


# ---- Very Weak

visible the password in console ? (y/n): y       
enter the password :#Leo25...


# ---- Very Strong
*/
```



___
---
***



# Day 9 - File Handling

## My_Notes:
```
* File Operations - Read & Writing files
    
* Requirements 
    - file to pointer (file pointer) 
         syntax : file *fp
    - open the file
        fopen(file_name,operation_mode)

* Operation Mode
    r - Read
    w - write
    a - append (update)
    r+ - read after write
    w+ - write after read
    a+ - a & r & w

* File Read : Read Logic
    - file doesn't exits
        if fp != null
            file exits
        else
            not exits

    - Read -> char by char
        ch = fgetc(fp); // fgetc - char by char read from file
        - repeat read char by char untill eof(end of file) by loop

* File write : write Logic
    - operation mode "w"
    - chr by char write => fputc(inp_char,fp); // writing inp_char --> fp
                           fputs - write by sring

* File Copy 
    Char by char model - it get same style 

* About CSV file  - comma sparated values
    create,write,read
```

## Code:

### fileread.c
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    FILE *fp; // FILE - it is a datatype
    fp = fopen("dummy.txt","r");
    char ch;
    if(fp==NULL)
    {
        printf("Error...File does not exit\n");
        exit(1);
    }
    else{
        while(1) //  while(1) - always conditon true 
        {
            ch = fgetc(fp);
            if(ch!=EOF)
                printf("%c",ch);
            else
                break;
        }
        fclose(fp);
    }
    
}

/*Output
    It seems like you're asking about the declaration of the FILE *fp; line in C. This line is used to declare a pointer to a FILE structure, which is defined in the standard C library <stdio.h>. 
    The FILE type is used to represent a file stream in C and allows you to perform operations like reading from or writing to files.
*/
```

### filewrite.c 
``` c
#include<stdio.h>
#include<stdlib.h>
int main()
{
    FILE *fp;
    int i;
    char c;
    fp = fopen("dummy2.txt","w+");
    char ch[30];
    int choice=1;
    while(1)
    {
        printf("do you want to continue (yes-1,no-0): ");
        scanf("%d",&choice); 
    if(choice==1)
    { 
            printf("Enter the string : ");
            scanf("%s",ch);
            fputs(ch,fp);
            fputc('\n',fp);         
    } 
    else{
        break;
    }
    }
    fseek(fp,0,SEEK_SET); // seekset start from 0 // use of fseek -> pointer was at last and we need to move to first by fseek 
    printf("The entered contents in the file: ");
    while(1)
    {
        c = fgetc(fp);
        if(c!=EOF)
            printf("%c",c);
        else    
            break;
    }
    fclose(fp);
}

/* Output
do you want to continue (yes-1,no-0): 1
Enter the string : hi
do you want to continue (yes-1,no-0): 1
Enter the string : hello
do you want to continue (yes-1,no-0): 0
The entered contents in the file: hi
hello

Ouput file : dummmy2.txt
hi
hello
*/
```

### file_copy.c 
``` c
#include<stdio.h>
int main()
{
    FILE *fp1,*fp2; //*fp1 - (source file) existing file ,*fp1 - new file 
    char c;
    fp1 = fopen("dummy3.txt","r");
    fp2 = fopen("dummy4.txt","w");
    while(1)
    {
        c = fgetc(fp1);
        if(c!=EOF)
            fputc(c,fp2);
        else    
            break;
    }
    printf("File contents copied successfully");
    fclose(fp1);
    fclose(fp2);
}

/*Output
    File contents copied successfully
*/


### csv_create.c
``` c
#include<stdio.h>
int main()
{
    FILE *fp;
    fp = fopen("dummy_mycsv.csv","w");
    int no=123;
    char name[] = "kamalraj";
    int exp = 18;
    fprintf(fp,"NO., NAME, EXP\n"); //fprintf() is a function used to write formatted output to a file
    fprintf(fp,"%d, %s, %d\n",no,name,exp);
    fclose(fp);
}

/* Output of dummy_mycsv.csv
    NO., NAME, EXP
    123, kamalraj, 18
*/
```



___
---
***