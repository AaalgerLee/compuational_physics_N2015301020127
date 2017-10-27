
# **第九次作业**



## *摘要*
	investigate the driven nonlinear pendulum, using the Euler-Cromer method. 
	also reproduce the Poincaré section in Figure 3.9 of the textbook.
	construct the Poincaré sections for the cases mentioned in 3.12..
  use Python to design the programs, which can realize the purpose of this assignment. 
   

---

## *背景介绍*
 - The case that we will be discussing is pendulum when dissipation, an external driving force and nonlinearity is present. 
 - Poincaré section is a good way to analysis the behavior of the motion of a complex system. We can use it to judge whether the system is periodic, quasi-periodic or chaotic.
 - According to the equation of motion, we can get the calculation subroutine using Euler-Cromer method. Nevertheless, we need to be careful that θ belongs to [-π,π].



### 2. Ideas
 - We can write out the equations of motion for the driven nonlinear pendulum according to Newton's second law and the textbook: <br>
![](http://latex.codecogs.com/gif.latex?%5Cfrac%7Bd%5E%7B2%7D%5Ctheta%7D%7Bdt%5E%7B2%7D%7D%3D-%5Cfrac%7Bg%7D%7Bl%7D%5Csin%5Ctheta-q%5Cfrac%7Bd%5Ctheta%7D%7Bdt%7D&plus;F_%7BD%7D%5Csin%5Cleft%20%28%5COmega_%7BD%7Dt%5Cright%29) <br> 
 - Then we can convert it into two first order ordinary differential equations: <br> ![](http://latex.codecogs.com/gif.latex?%5C%5C%5Cfrac%7Bd%5Comega%7D%7Bdt%7D%3D-%5Cfrac%7Bg%7D%7Bl%7D%5Csin%5Ctheta-q%5Cfrac%7Bd%5Ctheta%7D%7Bdt%7D&plus;F_%7BD%7D%5Csin%5Cleft%20%28%5COmega_%7BD%7Dt%5Cright%29%5C%5C%20%5Cfrac%7Bd%5Ctheta%7D%7Bdt%7D%3D%5Comega)
 -  Thus we get the calculation subroutine: <br> ![](http://latex.codecogs.com/gif.latex?%5C%5C%5Comega_%7Bi&plus;1%7D%3D%5Comega_%7Bi%7D-%5Cleft%20%5B%5Cfrac%7Bg%7D%7Bl%7D%5Csin%5Ctheta_%7Bi%7D&plus;q%5Comega_%7Bi%7D-F_%7BD%7D%5Csin%5Cleft%20%28%5COmega_%7BD%7Dt_%7Bi%7D%5Cright%29%5Cright%5Ddt%5C%5C%5Ctheta_%7Bi&plus;1%7D%3D%5Ctheta_%7Bi%7D&plus;%5Comega_%7Bi&plus;1%7Ddt%5C%5Ct_%7Bi&plus;1%7D%3Dt&plus;dt%5C%5C%5Ctheta_%7Bi%7D%5Cin%5Cleft%20%5B-%5Cpi%2C%5Cpi%5Cright%5D)
 - In this problem, we suppose the length of the pendulum as `9.8m`, the acceleration due to gravity as `9.8m/s^2`, which is the commonly adopted value.
 - We also take the parameter that measures the strength of damping as `0.5`, and the angular frequency of the driving force as `2/3s^-1`.


### 3. Programs
 - [Ex09-L1.py](https://github.com/2013301020135/computationalphysics_N2013301020135/blob/master/Chapter-3/Exercise-9/Ex09-L1.py)


### 4. Results
 - We run the program, and yield the Poincaré section for these required cases.
 - `Omega` as a function of `theta` for a driven nonlinear pendulum, at times that are in phase with the driving force: <br> ![Ex9-L1-1.png](https://raw.githubusercontent.com/2013301020135/computationalphysics_N2013301020135/master/Chapter-3/Exercise-9/Ex9-L1-1.png)
 - The Poincaré section for a driven nonlinear pendulum, at times `π/4` out-of-phase with the driving force: <br> ![Ex9-L1-2.png](https://raw.githubusercontent.com/2013301020135/computationalphysics_N2013301020135/master/Chapter-3/Exercise-9/Ex9-L1-2.png)
 - The Poincaré section at times corresponding to a maximum of the drive force: <br> ![Ex9-L1-3.png](https://raw.githubusercontent.com/2013301020135/computationalphysics_N2013301020135/master/Chapter-3/Exercise-9/Ex9-L1-3.png)
 
    
---

## *Conclusion*
 - As we can see from these graphs, the driven nonlinear pendulum has a chaotic characteristic.
 - Our Poincaré sections are more precise and vivid than the text book, and for the first case, my graph is almost the same as Figure 3.9 in the textbook.
    
---

## *Acknowledgment*
   The program part is based on the program of [2013301510086](https://github.com/newton2ndlaw/computationalphysics_N2013301510086/blob/master/Homework9/code3.12_3.md).



