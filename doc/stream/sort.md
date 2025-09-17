# stream开发整理

## TODO

### 1. 文档说明结果

### 2. 测试
1. 需要run 10 times？：使其容量不命中
2. 增大linewidth?好像不公平
   
### 3. 开发
1. coding
2. profiling效率
3. 环境更新xx

### 4. 设计

1. 分支预测失误恢复
2. 流计算指令有两种方案
   1. 扩展custom op
      1. 需要重新为运算指令在custom op之中编码运算(+ - 移位等)
   2. CSR方案()
      1. 编译如何支持？
      2. 用一个自定义寄存器可以吗？
3. 细化流指令流水级
   1. 在SE内拆分流水线：对应custom op
   2. 复用外部流水线：对应CSR方案：`step i`和`cal stream`之间的数据依赖很难解决

## 5. 路线


## 数据整理

### 64 word
custom：{Total cycles: 362, Total insts: 287}
normal：{Total cycles: 958, Total insts: 533}

### 512word
custom：{Total cycles: 1832, Total insts: 2080}
normal：{Total cycles: 6844, Total insts: 4120}