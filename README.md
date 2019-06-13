# CapsNet

## Layer

Conv1：输入（None，28，28，1），经过卷积层（卷积核大小9，步长1，个数256），输出（None，20，20，256）

PrimaryCap：输入（None，20，20，256），经过卷积层转换为胶囊（卷积核大小9，步长2，个数32\*8，8可以认为是胶囊包含的向量长度），输出将（None，6，6，256）转换为（None，6\*\*6\*32，8）。（此步无路由）

CapsuleLayer：输入（None，6\*\*6\*32，8），经过胶囊网络，输出为（None，10，16）。（此步有路由）

## CapsNet-Keras

https://github.com/XifengGuo/CapsNet-Keras

PrimaryCap：没有动态路由算法，将输入（None, width, height, channels）转换为输出（None, num\_capsule, dim\_capsule）。

CapsuleLayer：执行动态路由算法，将输入（None, input\_num\_capsule, input\_dim\_capsule）转换为输出（None, num\_capsule, dim\_capsule）。

## CapsNet-Tensorflow

https://github.com/naturomics/CapsNet-Tensorflow

CapsLayer：定义PrimaryCaps\_layer（没有动态路由算法）和DigitCaps\_layer（执行动态路由算法）。

## CapsNet-Pytorch

https://github.com/gram-ai/capsule-networks

primary\_capsules：没有动态路由算法。

digit\_capsules：执行动态路由算法。

https://github.com/XifengGuo/CapsNet-Pytorch 可作为参考。

