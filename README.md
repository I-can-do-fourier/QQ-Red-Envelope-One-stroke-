# QQ-Red-Envelope-One-stroke-

## 一、项目介绍
   **该项目针对qq的一笔画红包，对自定义的一笔画红包进行路径自动识别(对一笔画截图进行处理，设计路径算法)，实现快捷抢红包。
在实现过程中，使用opencv作为基础框架，利用java调用opencv进行图形处理，并使用jni对程序进行优化和加速。**
## 二、实现流程
#### 1.在java端对一笔画截图进行处理，找到图中的所有节点和节点之间的连接关系，生成gragh数据结构
#### 2.寻找适当算法，在java端对上一步生成的graph进行运算，得到一笔画路径
#### 3.使用jni，将图像处理部分移植到c++。用java调用生成的dll，加速程序。
## 三、具体实现
### 1. 图像预处理
**预处理的步骤为:高斯滤波->生成灰度图->缩放->阈值分割->canny变换**
#### canny变换：生成轮廓图，为后面的hough变换做准备。
![image](https://github.com/I-can-do-fourier/QQ-Red-Envelope-One-stroke-/tree/master/image/canny.jpg)


