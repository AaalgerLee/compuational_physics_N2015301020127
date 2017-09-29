## 第四次作业
 
### 一、摘要
本次作业内容为教材课后习题1.5：两种原子核各有几率衰变成另一种核，因此它们的衰变规律将由两个互相耦合的一阶线性微分方程描述。我采用课本上介绍的
欧拉方法来解决此问题，并用图像表示出了两种核数目随时间的变化规律。 

通过本次作业的练习，我终于基本掌握了用python绘图的方法，另外，也第一次通过自己写程序来解决微分。

### 二、背景介绍
题目1.5课本习题1.5\ 
Consider again  a decay problem with two types of nuclei A and B, but now suppose that nuclei of type A decay into ones of type B, while nuclei of type B decay into ones of type A. Strictly speaking, this is not a "decay" process, since it is possible for the type B nuclei to turn back into type A nuclei. A better analogy would be a resonance in which a system can tunnel or move back and forth between two states A and B which have equal energies. The correponding rate equation are   
　　　　　　　　　　　　　　　d N_A /dt = N_B/tau - N_A/tau  
　　　　　　　　　　　　　　　d N_B /dt = N_A/tau - N_B/tau  
where for simplicity we have assumed that the two types of decay are characterized by the same time constant, tau. Solve this system of equations for the numbers of nuclei, N_A and N_B, as functions of time. Consider different initial conditions, such as N_A=100, N_B=0, etc., and take tau =1s. Show that you numerical results are consistent with the idea that the system reaches a steady state in which N_A and N_B are constant. In such a steady state, the time dericatives dN_A/dt and dN_B/dt should vanish.
