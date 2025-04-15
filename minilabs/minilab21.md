## Memory Leaks / Code Tracing
Consider the following code:
```
#include <stdio.h>
#include <stdlib.h>

typedef struct Point{
    int f1;
    int f2;
} Point;

int* bar(int **, int);
int* foo(Point *, int);

int* bar(int **p, int n) {

    int *ip = (int *) malloc(sizeof(int)*2);
    
    // line 16

    for(int i=0; i<n; i+=2) {
        ip[0] += p[0][i];
        ip[1] += p[1][i+1];
        // line 21
    }
    // line 23
    return ip;
    // line 25
}

int* foo(Point *p, int n) {
    int **ip = (int **) malloc(sizeof(int *)*2);
    int *p1 = (int *) malloc(sizeof(int)*n);
    int *p2 = (int *) malloc(sizeof(int)*n);
    // line 32
    ip[0] = p1;
    ip[1] = p2;
    // line 35
    for (int i=0; i<n; i++) {
        *(p1 + i) = p->f1;
        *p2 = (*p).f2;
        // line 39
        p2++;
        // line 41
        p++;
        // line 43
    }
    // line 45
    p1 = bar(ip, n);
    
    // line 48
    
    return p1;
    // line 51
}

int main(void) {
    int n = 10;
    // line 56
    Point *p = (Point *) malloc(sizeof(Point)*n);
    // line 58
    for (int i=0; i<n; i++) {
        p[i].f1 = 2*i;
        p[i].f2 = 2*i+1;
        // line 62
    }
    // line 64
    int *ip = foo(p, n);
    // line 66
    printf("ip[0] = %d\nip[1] = %d\n", ip[0], ip[1]);
    // line 68
    return 0;
    // line 70
}
// line 72
```


### Question 2
Does this code rely on undefined behavior?
If yes, where and how would you fix it?
If no, what is the output of the above code?
<pre>







</pre>

### Question 2
How would you fix the memory leak in the above code?
<br><br><br>

