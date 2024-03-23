# Matlab-Magnify
Add magnifying glass to fig.


## Source
https://ww2.mathworks.cn/matlabcentral/fileexchange/5961-magnify

## modification
I just modified the code, add the function: Separately adjust the magnification scale for the X and Y directions.

## useage
### 用法1：随时查看放大图
当图像有些细节看不清楚，可以在Fig里面加一个放大镜
![[Pasted image 20240323100259.png]]
当按下按钮时，在鼠标 位置下创建一个放大框。
按下`+/-`增大/减小X方向放大倍数
按下`[/]`增大/减小X方向放大倍数
按下`>/<`增加/减小方框大小
按住`Ctrl`，同时单击以在图上留下放大倍数。

```
x = 0:1e-2:10;
y = x.*x.*sin(x);
f1 = figure;
p1 = plot(x,y);
magnify
```

### 用法2：Plot in Plot
在figure图中，将鼠标停在想要放大的区域处，点击鼠标右键不要松开手，此时鼠标点击处出现类似放大镜的方框（可以一直按住右键并移动鼠标改变区域位置），并通过`<>`键缩小或扩大方框范围，通过`-+`键减小或增加局部缩放比例，得到自己想要的小图后即可松开鼠标右键。若想得到多个小图，重复上述操作即可。（这一过程通常叫做固化）
通过figure菜单栏中的`工具→编辑绘图`选项或选中`工具栏中的白色箭头`来调节小图位置，也可单独在小图中编辑图形的坐标轴、线形、颜色等。



