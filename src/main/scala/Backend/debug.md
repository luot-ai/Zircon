## 0915
### 10:34
1. 完成了 ITER=32 下的测试：使用循环之后减少了ICACHE与STREAM对Memory的争用，虽然未实现分支预测错误恢复，但是该程序中该问题并不影响
2. cycle数=263 指令数=159
3. 跑了一下 普通程序在ITER=32下的测试：Total cycles: 644, Total insts: 147，暂未进行详尽分析


### 16:09

64word add：{Total cycles: 362, Total insts: 287}
normal：{Total cycles: 958, Total insts: 533}



### 18：48

1. 完成debug64 word，使两个stream交叠

### 9：30
2. 扩展使支持512word
3. profiling
   1. 需要run 10 times？：容量不命中
   2. 看普通程序慢的原因
   3. 增大linewidth?好像不公平
4. 前端指令
