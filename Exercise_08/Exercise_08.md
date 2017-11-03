# 第八次作业

# 1.Abstract    
In this report, the Lorentz model is applied to grasp a basic understanding of fluid mechanics, especially Rayleigh-Benard problem. Besides, phase-space plot, Poincare section are investigated.  

# 2.Background    
Lorentz was studying the basic equations of fluid mechanics, which are known as the Navier-Stokes equations and which can be regarded as Newton’s law written in a form appropriate to a fluid. The specific situation he considered was the Rayleigh-Benard problem, which concerns a fluide in a container whose top and bottom surfaces are held at different temperatures. Indeed, he grossly simplified the problem as he reached to the so-called Lorentz equations, or equivalently, the Lorentz model, which provided a major contribution to the modern field of physics.  

# 3.Methodology and Solution
**The Lorentz equations (the Lorentz model)**  
<img src="http://chart.googleapis.com/chart?cht=tx&chl=%5C%5C%5Cfrac%7Bdx%7D%7Bdt%7D%3D%5Csigma%20(y-x)%0A%5C%5C%5Cfrac%7Bdy%7D%7Bdt%7D%3D-xz%2Brx-y%0A%5C%5C%5Cfrac%7Bdz%7D%7Bdt%7D%3Dxy-bz" style="border:none;" />  
The Lorentz variables <img src="http://chart.googleapis.com/chart?cht=tx&chl=x%2C%20y%2C%20z" style="border:none;" /> are derived from the temperature, density and velocity variables in the original Navier-Stokes equations, and the parameters <img src="http://chart.googleapis.com/chart?cht=tx&chl=%5Csigma%20%2C%20r%2C%20b" style="border:none;" /> are measures of the temperature difference across the fluid and other fluid parameters. 

**Euler Method**  
Euler-Cromer method is designed for second-order differential equations, so it is not directly applicable to the Lorentz model.  
Here, the Euler algorithm can actually be used to treat the Lorentz problem.  
<img src="http://chart.googleapis.com/chart?cht=tx&chl=%5C%5Cx_%7Bi%2B1%7D%3Dx_i%2B%5Csigma%20(y_i-x_i)dt%0A%5C%5Cy_%7Bi%2B1%7D%3Dy_i%2B(-x_iz_i%2Brx_i-y_i)dt%0A%5C%5Cz_%7Bi%2B1%7D%3Dz_i%2B(x_iy_i-bz_i)dt%0A" style="border:none;" />    

**Parameters in the Lorentz Model**  
There are three parameters in the Lorentz equations <img src="http://chart.googleapis.com/chart?cht=tx&chl=%5Csigma%2Cb%2Cr" style="border:none;" />, and the behavior one finds depends on their values.  
In this report, the custom is followed and <img src="http://chart.googleapis.com/chart?cht=tx&chl=%5Csigma%3D10%2Cb%3D8%2F3" style="border:none;" /> is used. The parameter <img src="http://chart.googleapis.com/chart?cht=tx&chl=r" style="border:none;" /> is a measure of the temperature difference between the top and the bottom of the fluid. In fact, <img src="http://chart.googleapis.com/chart?cht=tx&chl=r" style="border:none;" /> plays the role analogous to the drive amplitude.

# 4.Code  
Code for [Fig.1.1-2:y/z VS time&2.1-2.3phase-space plot&2.4:3Dplot](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/10.1.py)  
Code for [animation to change r](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/10.1change_r.py)  
Code for [animation of trajectory to keep r=25](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/10.2keep_r%3D25.py)  
Code for [Poincare Section](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/10.3poincare.py)  

# 5.Running and Analysis
## 5.1 Lorentz Variables versus Time 
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure_1.png)  
This is the result of variation of the Lorentz variables <img src="http://chart.googleapis.com/chart?cht=tx&chl=y,z" style="border:none;" /> as a function of time.  The calculation is performed using the Euler method with a time step <img src="http://chart.googleapis.com/chart?cht=tx&chl=dt%3D0.0001" style="border:none;" /> and other parameters set as <img src="http://chart.googleapis.com/chart?cht=tx&chl=%5Csigma%3D10%2Cb%3D8%2F3" style="border:none;" />. The initial conditions are <img src="http://chart.googleapis.com/chart?cht=tx&chl=x_0%3D1%2Cy_0%3D0%2Cz_0%3D0" style="border:none;" />.  
As for <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D5%2C10%2C15" style="border:none;" />,  the behaviors are similar: there is an initial transient, and after it decays away, <img src="http://chart.googleapis.com/chart?cht=tx&chl=y,z" style="border:none;" /> are constant independent of time.  The transient takes longer as <img src="http://chart.googleapis.com/chart?cht=tx&chl=r" style="border:none;" /> increases. These cases correspond to steady convective in the original fluid, analogous to the regular nonchaotic motion of the pendulum.  
As for <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D25" style="border:none;" />, the initial transient is roughly periodic, but it gives way to irregular. This corresponds to the chaotic condition.  
To have a clearer picture of this transition from steady convective to chaotic behavior, a GIF is made by changing the value of <img src="http://chart.googleapis.com/chart?cht=tx&chl=r" style="border:none;" />.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure1.change_r.gif)  
as can be seen from the above, the transition takes place somewhere near <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D25" style="border:none;" />.  

## 5.2 Chaotic Behavior for <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D25" style="border:none;" />
First, we consider the phase-space plot for the Lorents model. Now that we have three variables in Lorentz model, projection of the trajectory can be considered.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure_2.1.png)  
This  is the phase-space plot for Lorentz model with <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D25" style="border:none;" />. The other parameters are set as <img src="http://chart.googleapis.com/chart?cht=tx&chl=x_0%3D1%2Cy_0%3D0%2Cz_0%3D0%2C%5Csigma%3D10%2Cb%3D8%2F3%2Cdt%3D0.0001%2CT%3D50" style="border:none;" />. From left to right, the figures are y versus x, z versus x and z versus y respectively.  
To show it more directly, a 3D image is made to show the trajectory.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure_2.4.png)  
Besides, the trajectory can be shown in a GIF so the motion is exhibited more clearly.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/keep_r%3D25.gif)  

## 5.3 Poincare Section and Regularity  
Since the Fig2.1, 2.2, 2.3 certainly give some hints of an underlying regularity, we can explore it by plotting the Poincare section. Because there are 3 Lorentz variables, it is natural to consider two-dimensional slices through the trajectory.  
In this section, the parameters are set as <img src="http://chart.googleapis.com/chart?cht=tx&chl=x_0%3D1%2Cy_0%3D0%2Cz_0%3D0%2C%5Csigma%3D10%2Cb%3D8%2F3%2Cdt%3D0.0001" style="border:none;" /> and the plot is drawn up to <img src="http://chart.googleapis.com/chart?cht=tx&chl=T%3D200" style="border:none;" />.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure_3.1.png)

The figure above is the Poincare section for <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D25" style="border:none;" />. The left if the intersection with <img src="http://chart.googleapis.com/chart?cht=tx&chl=x%3D0" style="border:none;" /> while the right is <img src="http://chart.googleapis.com/chart?cht=tx&chl=y%3D0" style="border:none;" />.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure_3.3.png)
These figures are also for <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D25" style="border:none;" />. However, they are the intersection of the trajectory with the plane <img src="http://chart.googleapis.com/chart?cht=tx&chl=x%3D2" style="border:none;" />, <img src="http://chart.googleapis.com/chart?cht=tx&chl=x%3D-2" style="border:none;" />, <img src="http://chart.googleapis.com/chart?cht=tx&chl=y%3D2" style="border:none;" /> and <img src="http://chart.googleapis.com/chart?cht=tx&chl=y%3D-2" style="border:none;" /> respectively.  
We can see from these figures that evev though the behavior is strongly chaotic, there is a very high degree of regularity in the phase-space trejectory.  
Change the value of <img src="http://chart.googleapis.com/chart?cht=tx&chl=r" style="border:none;" /> to <img src="http://chart.googleapis.com/chart?cht=tx&chl=r%3D35" style="border:none;" />, we have the figure below.  
![](https://github.com/JunyiShangguan/computationalphysics_N2013301020076/blob/master/ex10_ch3.26/figure_3.7.png)  


# 6.Acknowledgemen and Reference  
-  [数学公式生成器](http://www.ruanyifeng.com/webapp/formula.html)
-  Computational Physics, Nicholas J. Giordano & Hisao Nakanishi  
-  感谢余婧柯学姐的指导和帮助
