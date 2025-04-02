## Test 3 Practice

Consider the following code:
```
1.  #include <stdio.h>
2.  #include <stdlib.h>
3.
4.  void bar(int **p1, int n, int *p2) {
5.      int temp = n/2;
6.
7.      *p1 = (int *) malloc(sizeof(int)*n);
8.
9.      int *new = (int *) malloc(sizeof(int)*temp);
10.
11.     for (int i=0; i<temp; i++) {
12.         new[i] = i;
13.         (*p1)[i] = i;
14.         (*p1)[i+temp] = 2*i;
15.     }
16. 
18.     p2 = p1;
19. 
20.     return new;
21.
22. }
23.
24. int main(void) {
25.     int *pa;
26.     int *pb;
27. 
28.     int val = 0;
29. 
30.     pb = bar(&pa, 10, pb);
31.     
32.     for(int i=0; i<5; i++) {
33.         val -= pb[i];
34.         val -= pa[i];
35.     }
36.
37.     printf("val = %d\n", val);
38. 
39.     return 0;
40. 
41. }
```

## Question 1
For each of the following, identify whether they are on the stack or the heap:
* `pa` (the pointer itself)
* `pb` (the pointer itself)
* `val`
* the memory `pa` points to (after the function is called)
* the memory `pb` points to (after the function is called)
* `temp`
* `p1` (the pointer itself)
* `p2` (the pointer itself)
* the memory `p1` points to
* `new` (the pointer itself)
* the memory `new` points to
* the memory `p2` points to when we first enter the function
* the memory `p2` points to before returning from the function
* `p2` (the pointer itself)


## Question 2
What is the output of this code?
<br><br><br>

## Question 3
How would you fix the memory leaks in this code?
<br><br><br>

## Question 4
Suppose on line 31 you print `pa` as a pointer and get the memory address
`0x390`.
What would `pa + 7` be?
