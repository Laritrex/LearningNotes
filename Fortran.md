# Fortran 学习笔记

*主要为了学习老师给的CFD代码*

**先按阅读代码的时间顺序来记录**

## REAL 浮点数与数组

1. `REAL(KIND(2.D0)) VaribleName1, VaribleName2, ......` **声明双精度浮点数变量**

2. `REAL(KIND(1.D0)), ALLOCATABLE :: VaribleName1, VaribleName2, ......` **声明双精度数组变量**   调用时再写`deallocatable`

3. `MODULE MODGLOB` **模块编写，便于在模块开头声明好所有变量**，使用模块时，应输入`USE MODULE`

4. `PROGRAM MAIN`  
