# 调研目前免费的可视化图表工具

### 国内
- [镝数](https://dydata.io/appv2/#/pages/index/home)
- [BDP](https://me.bdp.cn/home.html)
- [fineBI](https://www.finebi.com/)
- [图表秀](https://www.tubiaoxiu.com/index.html)



### 国外

- [Tableau](https://www.tableau.com/)
- [R shiny](http://shiny.rstudio.com/)
- [Datawrapper](https://www.datawrapper.de/)
- [observable](https://observablehq.com)
- [powerBI](https://powerbi.microsoft.com/zh-cn/get-started/)
- [Google 数据洞察](https://developers.google.cn/datastudio?hl=de)
- [Google Charts](http://www.google-chart.com/2013/04/)
- [Leaflet](https://leafletjs.com/)
- [RawGraphs](https://rawgraphs.io/)
- [knight lab time lines](http://timeline.knightlab.com/)
- [Chartist.js](http://gionkunz.github.io/chartist-js/)
- [ColorBrewer](http://colorbrewer2.org/#type=sequential&scheme=BuGn&n=3)
- [D3.js](https://d3js.org/)
- [Plotly](https://plot.ly/python/)
- [Polymaps](http://polymaps.org/)
- [Dygraphs](http://dygraphs.com/)
- [GanttPro](https://ganttpro.com/)




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

`BDP只能做两层的桑基图，所以选择了每部电影的前面两个主题`

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

`在网站中为交互式的图，鼠标放在上面就可以看到详细信息，所以网站没有给出图例，这样截图看起来有点看不懂。里圈是主题分类，外圈是各个主题下的级别分类。`

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
     


### 最后，我用图表秀做了一个比较整幅的作品

[2011-2018 : top-10-highest-grossing-films](https://www.tubiaoxiu.com/p/s/78a5c69652825aaf.html)

___

### 我的感想

- 我发现目前的可视化工具可以分成两类，一类是比较傻瓜的，类似于美图秀秀的东西，里面有图表模板，只需要把自己的数据导入就可以得到图表，但是这样得到的图表都是最基础的图形，很难有创新。另一类是工具需要编程能力的，可创造的空间比较大，可以做出更复杂好看的图，看完之后感觉对于我这样的编程小白来说，要学习的东西有好多……

- 我做作业的时候使用的是镝数、tableau和BDP，其中我认为BDP是最好用的。镝数不好用的地方在于它不能计算，很多时候要自己先在Excel里统计出一个新的数据表，然后再导入进去；tableau和BDP都具有一定的计算功能，但是与tableau相比，BDP界面更加友好，功能比较简单，比较容易上手，tableau可以实现更多的功能。此外，我发现BDP有一个bug，如果对已经上传过的Excel表进行更新，保存之后重新上传，BDP网页中的数据并不会更新，只有把改好的Excel表名字修改一下再上传，网页才会更新。

- 我发现每种图表都有它的适用范围，有些图表好看但是不一定适合呈现我想呈现的数据，在制作之前需要弄清楚每种图表的意思，然后再合理选择。


     
