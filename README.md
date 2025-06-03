# ESKF-External-Force-Estimation

基于ESKF的四旋翼外力估计

## 一、KF

### 1. 基础知识

卡尔曼滤波(Kalman Filter, KF)的基础思想是要从**模型预测**和**传感器观测**中权衡，获得一个**最优估计**。

KF只能应用于**线性系统**，因为需要满足：**高斯噪声经过线性变换仍是高斯分布，用均值和方差描述**。因此可以设计**最小均方误差**的最优指标。

KF基于以下的离散系统模型：

![](https://latex.codecogs.com/png.latex?x_%7Bk%2B1%7D%20%3D%20F_%7Bx%7D%20%5Ccdot%20x_%7Bk%7D%20%2B%20F_%7Bn%7D%20%5Ccdot%20%28u_%7Bk%7D%20%2B%20%5Ceta_%7Bk%7D%29)
  
![2](https://latex.codecogs.com/png.latex?z_%7Bk%7D%20%3D%20H%20%5Ccdot%20x_%7Bk%7D%20%2B%20%5Cnu_%7Bk%7D)

### 2. 预测

![3](https://latex.codecogs.com/png.latex?x_%7Bk%2B1%7D%5E%7B-%7D%20%3D%20F_%7Bx%7D%20%5Ccdot%20x_%7Bk%7D%20%2B%20F_%7Bn%7D%20%5Ccdot%20u_%7Bk%7D)

![4](https://latex.codecogs.com/png.latex?P_%7Bk%2B1%7D%20%3D%20F_%7Bx%7D%20%5Ccdot%20P_%7Bk%7D%20%5Ccdot%20F_%7Bx%7D%5ET%20%2B%20F_%7Bn%7D%20%5Ccdot%20Q%20%5Ccdot%20F_%7Bn%7D%5ET)




