#双交合透镜设计
##1、设计目标
-  edp 50mm
- 全视场(FFOV)10
- 使用F,d,C光。d为主光线
- F数为8
- 使用BK7/F2组合
- 使用合理的MF设置
- 最小边缘/中心厚度4mm,最大中心厚度18mm

##2、设计过程
###2.1设置EPD，Filed，Wavelengths
![](/assets/5.1.png)
选择select自动调出FDC三种色光
###2.2设置面数，备注，玻璃，F数限制
需要交合面
使用F数限制最后一个光学表面的曲率半径。
![](/assets/5.2.png)
设置变量
设置默认优化函数。
<mark>注意可以使用厚度限制。RMS是均方根的意思<mark>
![](/assets/5.3.png)
###2.3开始使用优化功能优化
并自动更新。
![](/assets/5.4.png)
<mark>每个图里面三个图的意思是三个不同的视场<mark>
ray fan中第一个是轴上视场，球差为主，下面的是边缘视场，在子午视场中心，不同色光的位置不同，有垂轴色差。慧差为主。均有色差

- analysis->miscellaneous->chromatic focus shift可以看到不同波长的光的焦距偏移程度。
![](/assets/5.5.png)

- miscellaneous->lateral color可以看垂轴色差
![](/assets/5.6.png)

####2.4.1锤形优化ctr+sht+H
- <mark>保存副本再继续进行优化<mark>

####2.4.2设置透镜第一个面的二次系数为变量
  - 分析-》均方根-》均方根视场，设置波长为poly only，数据为弥散斑。
  - 视窗-》克隆，锁定第一个窗口，新克隆出来的窗口会变化。
  - 优化更新
  - 窗口覆盖，进行对比。
  虽然轴上弥散斑变大，但整体有了很大改善。
![](/assets/5.7.png)
![](/assets/5.8.png)
####2.4.3自动寻找非球面，设置好面的范围。

###2.4双分离结构
- 2和3之间添加一个表面，重新使用默认优化函数
- 自动优化



