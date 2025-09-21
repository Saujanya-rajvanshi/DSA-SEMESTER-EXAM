# DSA-SEMESTER-EXAM
this is my dsa semester codes

### array 
```c

#include <stdio.h>
#define MAX 5

void insert(int *ar, int p, int n);
void display (int *ar);
void del(int *ar,int p);
void rev(int *ar);
void search(int *ar,int n);

void main() {
    int ar [MAX] = {0};
    insert(ar, 0, 11);
    insert(ar, 1, 12);
    insert(ar, 2, 13);
    insert(ar, 3, 14);
    insert(ar, 4, 15);
    
    printf("Array after insertion:\n");
    display(ar);
    
    printf("Array after deletion:\n");
    del(ar,3);
    display(ar);
    
    insert(ar, 2, 13);
    
    printf("Array after reverse:\n");
    rev(ar);
    display(ar);
    
    int n;
    printf("What element do you want to search:\n");
    scanf("%d", &n);
    search(ar,n);
}

void insert(int *ar, int p, int n){
    for(int i = MAX-1; i > p; i--) {
        ar[i] = ar[i-1];
    }
    ar[p] = n;
}

void rev(int *ar){
    for(int i = 0; i < MAX/2 ; i++) {
        int t = ar[i];
        ar[i] = ar[MAX-1-i];
        ar[MAX-1-i] = t;
    }
}

void search(int *ar,int n){
    for(int i=0;i< MAX;i++){
        if(ar[i]==n){
            printf("Element %d found at position %d\n", n , i+1);
            return;
        }
    }
    printf("Element %d not found in the array\n", n);
}

void del(int *ar,int p){
    for(int i = p; i < MAX-1; i++) {
        ar[i-1] = ar[i];
    }
    ar[MAX-1] = 0;   // clear last element
}

void display(int *ar){
    for(int i = 0; i < MAX ; i++){
        printf("%d ",ar[i]);
    }
    printf("\n");
}

```
