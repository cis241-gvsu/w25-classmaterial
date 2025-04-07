# Minilab - 2D Arrays

## 2D Arrays - Stack

### Part 1

Suppose you place the following code inside of a `main` function
(assuming your program also includes the necessary header files):
```
double mat_stack[6][5];
printf("%p\n", mat_stack);
```

which creates a $6 \times 5$ 2D array of doubles named `mat_stack`.
Suppose when you compile and run it prints `0xffa280`.

### Part 2
Without programming to find the answer,
what would be the output of the following lines?
```
printf("%p\n", &(mat_stack[0][0]));
printf("%p\n", &(mat_stack[0][1]));
printf("%p\n", &(mat_stack[1][0]));
printf("%p\n", &(mat_stack[2][0]));
```
<br><br><br><br>

### Part 3
Without programming to find the answer,
what would be the output of the following lines?
```
printf("%p\n", &(mat_stack[0][0])+1);
printf("%p\n", &(mat_stack[1][0])+2);
printf("%p\n", &(mat_stack[1][0])+5);
```
<br><br><br><br>

### Part 4
Without programming to find the answer,
what would be the output of the following lines?
```
printf("%p\n", mat_stack + 1);
printf("%p\n", mat_stack + 2);
printf("%p\n", mat_stack + 6);
```
<br><br><br><br>

### Part 5
Without programming to find the answer,
what would be the output of the following lines?
```
printf("%p\n", mat_stack[1]);
printf("%p\n", *(mat_stack+1));
printf("%p\n", mat_stack[1]+2);
```
<br><br><br>


