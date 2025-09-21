# DSA-SEMESTER-EXAM
this is my dsa semester codes

### array 
```c
#include <stdio.h>
#define MAX 5

void insert(int *ar, int p, int n);
void display (int *ar);

void main() {
    int ar [MAX];
    insert(ar, 0, 11);
    insert(ar, 1, 12);
    insert(ar, 2, 13);
    insert(ar, 3, 14);
    insert(ar, 4, 15);
    
    printf("Array after insertion:\n");
    display(ar);
}

void insert(int *ar, int p, int n){
    for(int i= MAX-1; i > p; i--) {
        ar[i] = ar[i-1];
    }
    ar[p] = n;
}

void display(int *ar){
    for(int i = 0;i < MAX ; i++){
        printf("%d",ar[i]);
        printf("\n");
    }
}
```
