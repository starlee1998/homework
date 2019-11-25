```
#
#加载程序包
library(ggplot2)
library(ggrepel)
library(ggthemes)

#我的数据
year <- c(1990,1991,1992,1993,1994,1995,1996,1997,1998,1999,2000,2001,2002,2003,2004,2005)
The_United_States <- c(2.04,2.00,2.04,2.04,2.04,2.00,1.95,2.00,2.04,2.09,2.04,2.00,2.04,2.04,2.13,2.09)
South_Korea <- c(1.96,2.13,1.72,1.42,1.30,1.06,1.10,1.04,0.96,0.98,0.99,1.02,1.05,1.06,1.04,1.00)
Japan <- c(1.12 ,1.13 ,1.12 ,1.12 ,1.13 ,1.14 ,1.15 ,1.15 ,1.16 ,1.16 ,1.19 ,1.18 ,1.17 ,1.16 ,1.15 ,1.13)
Taipei <- c(1.23 ,1.33 ,1.43 ,1.49 ,1.48 ,1.46 ,1.59 ,1.57 ,1.64 ,1.48 ,1.37 ,1.09 ,1.00 ,0.94 ,0.96 ,1.01)
df <- data.frame(x = c(1995,1993,2000,2000), y = c(1.06,2.04,1.19,1.37), family = c("South Korea starts","The US starts","Japan starts","Taipei starts"))
dd <- data.frame(year,The_United_States,South_Korea,Japan,Taipei)

#绘图
ggplot(df)+

#先画四条线及上面的点
geom_line(data = dd,aes(x = year,y = The_United_States,colour = "The United States"),size=0.5)+
geom_point(data = dd,aes(x = year,y = The_United_States,colour = "The United States"),size=0.75)+
geom_line(data = dd,aes(x = year,y = South_Korea,colour = "South Korea"),size=0.5)+
geom_point(data = dd,aes(x = year,y = South_Korea,colour = "South Korea"),size=0.75)+
geom_line(data = dd,aes(x = year,y = Japan,colour = "Japan"),size=0.5)+
geom_point(data = dd,aes(x = year,y = Japan,colour = "Japan"),size=0.75)+
geom_line(data = dd,aes(x = year,y = Taipei,colour = "Taipei"),size=0.5)+
geom_point(data = dd,aes(x = year,y = Taipei,colour = "Taipei"),size=0.75)+

#添加四个说明标签
geom_text_repel(aes(x,y,label = family, family = "times",fontface = "italic"),size = 3,box.padding=unit(2.5, "lines"),point.padding=unit(0.1, "lines"), segment.colour = "grey50")+

#加上外围标签、标题
labs(x = "year",y = "waste per capita",colour = "Country",title = "Waste per capita in four countries",caption = "Source: Annual Statistical Report of four countries")+ 

#套用主题包
theme_economist() + 
scale_color_economist()+

#根据自己需要再次调整主题
theme(legend.position="right",legend.text=element_text(family = "times",size=10),plot.title = element_text(lineheight=.5, face="bold"),title = element_text(family = "times"))
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        