## 第三章

### varible变量

- variable是有状态的张量
- 变量在真正开始执行之前，都是需要开始初始化的

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





