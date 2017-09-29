## 第四次作业
 
### 一、摘要
本次作业内容为教材课后习题1.5：两种原子核各有几率衰变成另一种核，因此它们的衰变规律将由两个互相耦合的一阶线性微分方程描述。我采用课本上介绍的
欧拉方法来解决此问题，并用图像表示出了两种核数目随时间的变化规律。 

### 二、背景介绍
题目1.5课本习题1.5                                                                                                                   
Consider again  a decay problem with two types of nuclei A and B, but now suppose that nuclei of type A decay into ones of type B, while nuclei of type B decay into ones of type A. Strictly speaking, this is not a "decay" process, since it is possible for the type B nuclei to turn back into type A nuclei. A better analogy would be a resonance in which a system can tunnel or move back and forth between two states A and B which have equal energies. The correponding rate equation are   
　　　　　　　　　　　　　　　d N_A /dt = N_B/tau - N_A/tau  
　　　　　　　　　　　　　　　d N_B /dt = N_A/tau - N_B/tau  
where for simplicity we have assumed that the two types of decay are characterized by the same time constant, tau. Solve this system of equations for the numbers of nuclei, N_A and N_B, as functions of time. Consider different initial conditions, such as N_A=100, N_B=0, etc., and take tau =1s. Show that you numerical results are consistent with the idea that the system reaches a steady state in which N_A and N_B are constant. In such a steady state, the time dericatives dN_A/dt and dN_B/dt should vanish.

 ### 三、正文
书上采用欧拉法来处理微分方程，原理是将微分方程化为差分方程，并利用前一时刻的结果来计算后一时刻的结果，反复迭代即得到变量对时间的依赖关系。欧拉法要能求得比较精确的解，步长的选取是十分关键的。一般来说，选取原则是：步长必须小于系统中任意的特征参数(例如，本题中就是要小于衰变的特征时间)。

本次计算中，衰变特征时间tau=10，取步长分别为四种情况：5.0, 2.0， 1.0， 2.0，0.5, 由此分别计算出数值解并作图(如下左图)。另外，为更直观地表示出各情况数值计算的精度，分别计算了各情况数值解与解析结果的偏差(如右下图)。可以发现，在步长为时间常数的1/2时,数值解偏离正确值很大，在核数为1000左右的情况下，计算偏差能达到200；而当步长减小时，计算误差则也减小；当步长仅为时间常数的1/20时，数值偏差衰减到不足20，此时可以认为计算精度比较满意。                 
                                                                                                                                  
源代码：[source code](https://github.com/AaalgerLee/compuational_physics_N2015301020127/blob/master/Exercise_04/sourcecode4.py)     
数值结果：[戳这里](https://github.com/AaalgerLee/compuational_physics_N2015301020127/blob/master/Exercise_04/sourcetext4.txt)            
效果图：
![](https://github.com/AaalgerLee/compuational_physics_N2015301020127/blob/master/Exercise_04/4-1.png)
### 四、结论
通过这次作业的掌握了用python绘图的方法，并掌握了写程序去解决微分的方法。

### 五、致谢
感谢赵展艺同学的源代码
