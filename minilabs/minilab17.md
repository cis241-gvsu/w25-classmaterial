# Minilab - Review

The purpose of this minilab is to give practice with
memory in C

Consider the following code:
```
1.  #include <stdio.h>
2.  #include <stdlib.h>
3.  
4.  void foo(float *p1, float *p2) {
5.      printf("*p1 in foo = %f, *p2 in foo = %f\n", *p1, *p2);
6.      float a = 10.3;
7.      float *pf = p1;
8.      p2 = p1;
9.      p1 = &a;
10.     *p1 = 3.1;
11.     pf += 1;
12.     *p2 = 2.2;
13. }
14. 
15. 
16. int main(void) {
17.     char *p1, *p2, *p3;
18.     float *p4, *p5, *p6, *p7, *p8, *p9;
19.     int n = 10;
20.     float f = 12.4;
21.     char c = 'z';
22. 
23.     p1 = &c;
24.     p2 = (char *) malloc(sizeof(char)*n);
25.     for (int i=0; i<n; i++) {
26.         p2[i] = 'A' + i;
27.     }
28.     
29.     *(p2 + 3) = 'y';
30.     p3 = p2;
31.     p2 += 3;
32.     printf("*p2 = %c\n", *p2);
33.     p3 = (char *) malloc(sizeof(char));
34.     p2 = p3;
35.     *p3 = c;
36.     printf("*p2 = %c\n", *p2);
37. 
38.     p4 = &f;
39.     p5 = (float *) malloc(sizeof(float));
40.     *p5 = 4.4;
41.     p6 = p4;
42.     p7 = p5;
43.     foo(p7, p6);
44.     printf("*p7 in main = %f, *p6 in main = %f\n", *p7, *p6);
45.     *p5 = 5.5;
46.     p8 = p6;
47.     p6 = p7;
48.     foo(p8, p6);
49. 
50.     return 0;
51. }
```

## Question 1
What is the output of this code?
<br><br><br><br>


## Question 2
For each of the following, is it on the stack or the heap?
* The pointer `p1`
* The memory `p1` points to?
* The pointer `p2`
* The memory `p2` points to?
* The char `c`?

<br><br><br><br>


## Question 3
Suppose you add a print statement between lines 24 and 25,
specifically
```
printf(p2 = %p\n", p2)
```
and it prints `0x354`.
What is `p2 + 8`?
<br><br><br>
<br><br>

## Question 4
This code leaks memory.  How would you fix it?
<br><br><br>
<br><br>
