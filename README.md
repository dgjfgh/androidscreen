# AndroidScreen 说明文档
 www.dqqdo.com


1 说明

Android screen是一个基于Java 开发的工具，目的是帮助android开发者生成多屏幕适配的配置文件，减少开发难度。

2 原理

原理：利用 android的自动匹配机制，将相同的 数值，比如@dimen_dimen100dp. 解释为在不同设备平台上不同数值。 但是当前程序可以通过换算，可以保证，你所设置的绝对值，相对于你的效果图，和解析之后的最终数值相对于实际效果图是一样的。

3 使用

使用步骤： 
1 和你们美工商量清楚，你们的效果图尺寸 
2 让你们美工把数值标注清楚。 
3 使用本项目的可执行jar文件，选择参数为你们美工告诉你的效果图尺寸，建议全选所有适配机型，然后一键生成资源文件。将资源文件拷贝至res目录下。 
4 在项目的xml布局文件中使用本项目自定义的数值单位。

这里写图片描述

4 代码说明

 首先  不用dp,   距离单位自己定义，这一步，不怎么需要改动，只需要将你之前是 20dp的地方更改为@dimens/dimen_20_dip.


 然后，自己将自己的单位解析为具体的px,不用dp.这一步如果自己写的话，工作量很大，我写了个小工具，可以一键生成，只需要把程序生成的资源文件，拷贝到res文件夹下 就可以使用了。

 最后，android系统自己去找相应资源目录下的  dimens.xml文件，从而获取最合适的值。这一步，不需要你的参与。
这里的内容很多，简单介绍不清楚。具体参考这里:

http://blog.csdn.net/i7788/article/details/44937277

5 相关源码

项目主页：https://code.csdn.net/zmobs/androidscreen

git地址：git://code.csdn.net/zmobs/androidscreen.git

csdn 下载地址:http://download.csdn.net/detail/zmobs/8815337  




