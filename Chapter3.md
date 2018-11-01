3.9 data alignment
```cpp
//size of t: 12 bytes
struct t {
    int a;
    int b;
    char c;
};
//size of t: 9 bytes
struct __attribute__((packed)) t {
    int a;
    int b;
    char c;
};
```
3.44 64bit system  
A. struct Pl { int i; char c; int j; char d; } ; // size 16, alignment:4  
B. struct P2 {int i; char c; char d; long j; };  // size 16, alignment:8  
C. struct P3 { short w[3]; char c[3] } ; // size 10, alignment: 2  
D. struct P4 { short w[5]; char * c[3] } ; // size 40, alignement: 8  
E. struct P5 { struct P3 a[2]; struct P2 t }; //size 24 + 16 = 40 aligment: 8  
