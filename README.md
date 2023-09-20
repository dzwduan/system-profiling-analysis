# system-profiling-analysis

## 整体思路

先完成，后完美；不要过早优化

## how to optimize matrix mul

1.   phyhon -> c++

2.   更换多重循环的嵌套顺序，利用cachegrind查看cache miss rate

3.   tiling分块，实现数据重用，需确定最优分块大小

4.   optimization flags 编译器 -O3 

5.   多核并行 cilk_for

6.   多级缓存分块，类似L1 L2 L3 cache

7.   递归分治

8.   向量硬件， clang -Ppass=vector  /  Intel AVX2

9.   预处理   矩阵转置  数据对齐  内存管理优化   处理递归边界

     

## 宾利优化规则

### 数据结构

1.   编码 ：将数值转化为所需位更少的表现形式，例如日期编码，struct标识
2.   增强 ：将更加信息添加到数据结构中，例如链表尾指针
3.   预计算：提前执行计算，防止影响关键任务
4.   编译器初始化
5.   缓存
6.   稀疏性



