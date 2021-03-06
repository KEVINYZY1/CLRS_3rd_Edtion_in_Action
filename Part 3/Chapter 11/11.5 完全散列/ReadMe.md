完全散列法
=======

算法概览
---------

**完全散列法** （Open Adderssing）是一种在关键字插入散列表之后没有变化的情况下，能在最坏情况下提供O(1)访存复杂度的散列策略。

这种策略使用两级的散列方法设计，在每级都使用全域散列法，使用两个不同的散列函数，先把关键字经过第一个散列函数（比如11.3.3节的全域散列）分配到一级散列表的槽中，

再使用另一个散列函数（随机使用几个不同的全域散列函数h，总能找到无冲突的）重新计算它在二级散列表的位置，二级散列表的大小需为散列到二级散列表的关键字数量的平方。

这种方法保证二级散列表上没有冲突，因此即使最坏情况下，访存复杂度也会低至O(1)。

算法性能
---------

最坏情况下时间复杂度：O(1)。