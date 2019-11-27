## 关于垃圾的两张图

# 图一：脱钩指数

- 原图一
![](https://github.com/starlee1998/homework/blob/master/%E5%9B%BE%E4%B8%80.png)


- 代码
```R

#图一代码

#加载程序包
library(ggplot2) #绘图
library(ggrepel) #防止标签重叠
library(ggthemes) #套用主题包
library(RColorBrewer) #套用调色包
library(tidyr) #下面的unit函数来自这个包

#我的数据
dd <- read.csv("pic1_data.csv")
df <- data.frame(
  x = year[7:11],
  y = Decoupling_index[7:11],
  family = c("-0.28","0.11","0.08","0.21","0.02")
  )

#绘图
ggplot()+

#先画两个条形图，再画线图和上面的点
  geom_bar(
    data = dd,
    aes(x = year,y = GDP_regard_1999_data_as_0.1,fill = "GDP(1999=0.1)"),
    stat ="identity",
    width=0.8,
    position='stack')+
  geom_bar(
    data = dd,
    aes(x = year,y = Garbage_clearance_regard_1999_data_as_0.1,fill = "Garbage Clearance(1999=0.1)"),
    stat ="identity",
    width=0.8,
    position='stack')+
  geom_line(
    data = dd,
    aes(x = year,y = Decoupling_index,colour = "Decoupling index"),
    colour = 'darkred',
    size=0.5)+
  geom_point(
    data = dd,
    aes(x = year,y = Decoupling_index,colour = "Decoupling index"),
    colour = 'darkred',
    size=0.8)+

  #加数据标签
  geom_text(
    data = df,
    aes(x=x,y=y,label = family, family = "times",fontface = "italic"),
    size = 2.6,
    nudge_y = -0.15,
    colour = "darkred")+

  #加上外围标签、标题
  labs(
    title="The Decoupling Index of Waste Production to GDP Growth",
    x = "Year",
    y = "Decoupling Index(DI)\nGDP and Garbage Clearance",
    fill = "",
    caption = "Source: China Statistics Yearbooks,2000-2018",
    label = family)+

  #添加线图说明
  geom_text_repel(
    aes(x=2001.4,y=1,label = "Decoupling index", family = "times"),
    size = 3,
    colour = "darkred",
    box.padding=unit(0.5, "lines"),
    point.padding=unit(0.05, "lines"),
    segment.colour = "grey50")+

  #添加强调矩形
  annotate("rect",
    xmin = 2005.6,
    xmax = 2010.4,
    ymin = 0,
    ymax = 2.6,
    fill = "gray60",
    alpha = 0.4)+

  #添加强调矩形文字
  annotate("text",
    x=2008, 
    y=2.4, 
    label="The Eleventh Five-Year Plan",
    family = "times",
    size = 2.4)+

  #添加图片说明
  annotate("text", 
    x=2017, 
    y=2.6, 
    vjust = "top",
    hjust = "right",
    label="DI t=(ΔWt)/(ΔGt)\nDI>1,no decoupling\n0<DI<1,relative decoupling\nDI=0,absolutely decoupling",
    family = "times",
    size = 2.7)+

  #套用主题包
  theme_economist()+

  #套用颜色包
  scale_fill_brewer(palette="Paired")+

  #根据自己需要再次调整主题
  theme(
    plot.title = element_text(size = 12,lineheight = .5),
    legend.text = element_text(size = 10,family = "times"),
    legend.margin=unit(c(0.2,0,0.5,0),'cm'),
    plot.margin=unit(c(0.2,0,0.5,0),'cm'),
    title=element_text(family="times",size = 10),
    axis.text.x=element_text(family = "times",size=9),
    axis.text.y=element_text(family = "times",size=9))
```

- 新图一
![](https://github.com/starlee1998/homework/blob/master/pic1.png)


## 图二：人均垃圾产量

- 原图一
![](https://github.com/starlee1998/homework/blob/master/%E5%9B%BE%E4%BA%8C.png)

```R
#图二代码

#加载程序包
library(ggplot2) #绘图
library(ggrepel) #防止标签重叠
library(ggthemes) #套用主题包

#我的数据
dd <- read.csv("pic2_data.csv")
df <- data.frame(
  x = c(1995,1993,2000,2000),
  y = c(1.06,2.04,1.19,1.37), 
  family = c("South Korea starts","The US starts","Japan starts","Taipei starts")
  )


#绘图
ggplot(df)+

#先画四条线及上面的点
geom_line(
	data = dd,
	aes(x = year,y = The_United_States,colour = "The United States"),
	size=0.5)+
geom_point(
	data = dd,
	aes(x = year,y = The_United_States,colour = "The United States"),
	size=0.75)+
geom_line(data = dd,
	aes(x = year,y = South_Korea,colour = "South Korea"),
	size=0.5)+
geom_point(data = dd,
	aes(x = year,y = South_Korea,colour = "South Korea"),
	size=0.75)+
geom_line(
	data = dd,
	aes(x = year,y = Japan,colour = "Japan"),
	size=0.5)+
geom_point(
	data = dd,
	aes(x = year,y = Japan,colour = "Japan"),
	size=0.75)+
geom_line(
	data = dd,
	aes(x = year,y = Taipei,colour = "Taipei"),
	size=0.5)+
geom_point(
	data = dd,
	aes(x = year,y = Taipei,colour = "Taipei"),
	size=0.75)+

#添加四个说明标签
geom_text_repel(
	aes(x,y,label = family, family = "times",fontface = "italic"),
	size = 3,
	box.padding=unit(2.5, "lines"),
	point.padding=unit(0.1, "lines"), 
	segment.colour = "grey50")+

#加上外围标签、标题
labs(
	x = "year",
	y = "waste per capita",
	colour = "Country",
	title = "Waste per capita in four countries",
	caption = "Source: Annual Statistical Report of four countries")+ 

#套用主题包
theme_economist() + 
scale_color_economist()+

#根据自己需要再次调整主题
theme(
	legend.position="right",
	legend.text=element_text(family = "times",size=10),
	plot.title = element_text(lineheight=.5, face="bold"),
	title = element_text(family = "times"))
```

- 新图二
![](https://github.com/starlee1998/homework/blob/master/pic2.png)


## 我的困惑

1. ggplot2如何做双坐标轴（两个不同的Y轴）？我从网上查到几篇教程，但是没能套用成功
2. 像图一那段比较长的注释（解释脱钩指数那段话），我只找到了把它加在图里面的方法，但是这样会显得图很拥挤。是否有办法把它像标题之类的东西一样加在图外面？


## 我的感受
听老师上课讲觉得R画基础图挺简单的，但是自己动手之后，开始无法忍受基础图的丑陋，不断地想让它更好看（虽然最后的排版依旧有点奇怪，不过作为小白，我真的尽力了……）。这次作业做的不轻松，但是莫名觉得开心，做到后来甚至觉得挺好玩的（？），通过这次作业，我从什么都不会到具有了能够写出上面这样的图的思路（当然有些步骤需要查一下用什么单词，不过现在至少知道要查什么了）。写R大概跟游戏的成瘾机制是一样的，不断地通过一个个小关卡，持续地享受成就感。

每次上课都让我觉得自己有好多要学的东西，但是平常各种忙总是找不到时间，幸好有DDL压迫我，让我能够在DDL前塌下心来学一种东西、做好一件事情。这种感觉挺好的。
