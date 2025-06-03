# ESKF-External-Force-Estimation

基于ESKF的四旋翼外力估计

## 一、KF基础

卡尔曼滤波(Kalman Filter, KF)的基础思想是要从**模型预测**和**传感器观测**中权衡，获得一个**最优估计**。

KF只能应用于**线性系统**，因为需要满足：**高斯噪声经过线性变换仍是高斯分布，可以用均值和方差描述**。因此可以设计**最小均方误差**的最优指标。

KF基于以下的离散系统模型：

![1](https://latex.codecogs.com/png.image?\dpi{120}&space;x_{k+1}=F_{x}\cdot&space;x_{k}&plus;F_{u}\cdot(u_{k}&plus;\eta_{k}))
  
![2](https://latex.codecogs.com/png.image?\dpi{120}&space;z_{k}=H\cdot&space;x_{k}&plus;\nu_{k})

