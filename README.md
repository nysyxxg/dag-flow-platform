# dag-flow-platform
https://blog.csdn.net/a925907195/article/details/88258273
基于dag的多线程异步并行计算，环路检测以及绘图都已实现

主要流程：
1.	线程依赖dag注册。将多线程的依赖关系构造成dag图。
2.	环路检测，检测dag图是否有环，如果有环则报错并打印出环路。
3.	可以选择性打印出整个dag图，直观查看dag中线程依赖关系。
4.	构造hystrixCommand并根据依赖关系封装执行依赖。
5.	异步调度执行，等最后一个返回成功则执行完毕（或者超时）。
