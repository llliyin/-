## 第三章

### varible变量

- variable是有状态的张量
- 变量在真正开始执行之前，都是需要开始初始化的
- 变量是在回话中进行初始化，赋值或者更新的
- 在模型训练过程中，中途需要调整文件的时候，可以通过th.train.saver将一些变量，信息保存到checkpoint（存储文件）文件中
- 从数据流图中取出数据需要使用session.run()来进行执行，向数据流图中填充数据是使用占位符来进行填充
- 数据流图本身是一个具有计算拓扑和内部结构的壳，在用户向数据流图在填充数据前，图中没有进行真正的计算

```python
import tensorflow as tf

#创建变量
w = th.Variable(<initial-value>,name=<optional-name)  #第二个参数：数据类型

#将变量作为操作输入
y = tf.matmul(w,...another variable or tensor...)
z = tf.sigmoid(w+y)

# 使用 assign 或assign_xxx 方法重新给变量赋值（更新值或者赋值都可以通过assign来进行）
w.assign(w + 1.0)
w.assign_add(1.0)

```





