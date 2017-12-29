---
plugins:
  - mathjax
---

# 单透镜设计优化

## 0. 设计步骤

系统的使用要求确定设计目标和参数--模型，实用pwm进行优化

## 1. 设计要求

* 入瞳直径40mm
* F数为10
* 半视场为$$5^\circ$$
- 使用波长0.587$$\mu$$_m_
- BK7玻璃
- 光阑位于第一个面
- 设计目标均方根半径在近轴想面上最小
- 无其他限制

![](/assets/TEL(O$U2A5SSVAF`@HDN6HK.png)

## 2. 具体设计步骤
1. System->general->Aperture设置入瞳直径40
1. System->Filed设置视场

   子午方向上正向视场，即Y-filed，取三个视场
   0，0.707$$\omega$$，以及$$\omega$$
1. System->Wavelengths设置波长
1. 设置透镜参数如图
![](/assets/D5}R)U(WXS8CN}M{_VUCJUF.png)

从上到下分别是物面光阑面像面![](/assets/C621F7JU7INP1TA(LW1HTUU.png)

然后通过设置2界面的F数使自动设置2的曲率半径

![](/assets/QUS`96QV%H()}Q7J$9QTN$I.png)
设置后
![](/assets/JTXUG_YPO9$TKAGZU1_D9$I.png)

   
   




