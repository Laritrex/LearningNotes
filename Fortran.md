# Fortran 学习笔记

*主要为了学习老师给的CFD代码*

**先按阅读代码的时间顺序来记录**

## REAL 浮点数与数组、主程序

1. `REAL(KIND(2.D0)) VaribleName1, VaribleName2, ......` **声明双精度浮点数变量**

2. `REAL(KIND(1.D0)), ALLOCATABLE :: VaribleName1, VaribleName2, ......` **声明双精度数组变量**   调用时再写`deallocatable`

3. `MODULE MODGLOB` **模块编写，便于在模块开头声明好所有变量**，使用模块时，应输入`USE MODULE`

4. `PROGRAM MAIN` : 主程序

5. `IMPLICIT REAL(KIND(1.D0)) (A-H,O-Z)`: 强制变量类型

6. `DACOS(-1.D0)`: 用反余弦函数计算pi值

7. `SPFAR = 50000.D0`: 远场静压为50000Pa
远场密度1.22
根据远场状态（超声速、亚声速无激波、亚声速有激波），给定马赫数和攻角（*具体给定三种状态的条件*）

8. CFL数给定0.2，

## 读入网格

1. `OPEN(61, FORM='UNFORMATTED',FILE='inmesh.xyz')`: 打开网格文件
`READ(61) NOUSE`: 过滤第一行信息
`READ(61) IT, JT`: 第二行为行列网格编号
`ALLOCATE( X(IT,JT), Y(IT,JT) )`: 分配网格节点坐标数组




