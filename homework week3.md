# 调研目前免费的可视化图表工具

### 国内
- [镝数](https://dydata.io/appv2/#/pages/index/home)
- [BDP](https://me.bdp.cn/home.html)
- [fineBI](https://www.finebi.com/)


### 国外

- [Tableau](https://www.tableau.com/)
- [R shiny](http://shiny.rstudio.com/)
- [Datawrapper](https://www.datawrapper.de/)
- [observable](https://observablehq.com)
- [powerBI](https://powerbi.microsoft.com/zh-cn/get-started/)


___

# 用不同的可视化工具呈现同一个数据集

### 所选数据集

从[Top 10 Highest Grossing Films (1975-2018)](https://www.kaggle.com/bidyutchanda/top-10-highest-grossing-films-19752018/downloads/top-10-highest-grossing-films-19752018.zip/1)中截取了2011-2018年的数据，对其进行统计处理。

___
### 呈现

**1. TOP电影主题：动作冒险类电影最多**


这里选取的数据为`Main_Genre`、`Genre_2`、`Genre_3`，即TOP电影的三个类型标签

***工具一：镝数***

![](https://github.com/starlee1998/homework/blob/master/top%E7%94%B5%E5%BD%B1%E4%B8%BB%E9%A2%98.png)

***工具二：Tableau***

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%89%E4%B8%AA%E4%B8%BB%E8%A6%81%E6%A0%87%E7%AD%BE%E5%88%86%E5%B8%83%E6%83%85%E5%86%B52.png)

***工具三：BDP***

![](https://github.com/starlee1998/homework/blob/master/top%E7%94%B5%E5%BD%B1%E4%B8%BB%E9%A2%983.png)
     
     
    
___
**2. TOP电影的时长和分级：**

这一部分关注电影的主题与时长和分级的关系，选取的数据为`Main_Genre`、`length`、`rating`。

- 时长
   
以下时长均为平均时长
     
***工具一：镝数***

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%BB%E9%A2%98%E4%B8%8E%E6%97%B6%E9%95%BF1.png)

***工具二：Tableau***

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%BB%E9%A2%98%E4%B8%8E%E6%97%B6%E9%95%BF2.png)

***工具三：BDP***

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%BB%E9%A2%98%E4%B8%8E%E6%97%B6%E9%95%BF3.png)
     

- 分级

***工具一：镝数***

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%BB%E9%A2%98%E4%B8%8E%E5%88%86%E7%BA%A71.png)
     
***工具二：Tableau***

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%BB%E9%A2%98%E4%B8%8E%E5%88%86%E7%BA%A72.png)

***工具三：BDP***

`在网站中为交互式的图，鼠标放在上面就可以看到详细信息，所以网站没有给出图例，这样截图看起来有点看不懂`

![](https://github.com/starlee1998/homework/blob/master/%E4%B8%BB%E9%A2%98%E4%B8%8E%E5%88%86%E7%BA%A73.png)
     
     
___     
**3. 各公司Top电影表现比较**

票房、IMDB评分和年度排名都可以反应出电影的表现，因此选取`studio`、`worldwide gross`、`imdb rating`、`rank in year`进行对比，

***工具一：镝数***

![各公司Top电影的表现](https://github.com/starlee1998/homework/blob/master/%E4%B8%89%E9%A1%B9%E5%B9%B3%E5%9D%87%E5%80%BC.png)
     
***工具二：Tableau***

![各公司Top电影的表现](https://github.com/starlee1998/homework/blob/master/%E4%B8%89%E9%A1%B9%E5%B9%B3%E5%9D%87%E5%80%BC%202.png)
     
***工具三:BDP***

![各公司Top电影的表现](https://github.com/starlee1998/homework/blob/master/%E4%B8%89%E9%A1%B9%E5%B9%B3%E5%9D%87%E5%80%BC3.png)
     

——————
### 我的感想


     
