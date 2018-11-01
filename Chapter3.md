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
