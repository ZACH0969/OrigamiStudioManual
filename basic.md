# 1. 基本逻辑

Origami 的最基本元素是 Patch，直译是补丁、小块，使用时就像是组合不同功能的乐高积木。Origami 有数量庞大的 Patch 库，但实际常用的核心 Patch 不到 20 个。所以不用担心，只要掌握简单的 Patch 和对应快捷键就能高效地制作原型。

Origami 的基本理念，就是快速实现最小可用的原型，然后根据需要在基础上堆叠各种补丁。

## 2. 四种Patch

### 1\) 操作类

常用的 Interaction Patch，能够监测对图层的点击事件，输出Down和Tap两个逻辑状态。

![](/assets/Jietu20170413-172852.jpg)

### 2\) 转换类

Switch 控件能通过左侧的输入切换开和关，右侧输出当前的状态。

![](/assets/Jietu20170413-173728.jpg)

Transition 能将 0 和 1 转变成任意开始值和结束值，如图中的 Patch ：

输入 0 就输出 0；

输入 1 就输出100；

输入 0.5 就输出 50。

![](/assets/Jietu20170413-174154.jpg)

### 3\) 动画类

PopAnimation 可能是大多数人接触 Origami 的原因，它能实现弹性的效果。

![](/assets/popanimation.png)

### 4\) 图层类

在 Origami Studio 内，图层主要是展示在右侧的图层列表内。可以通过单击 Layer 参数名的方式创建对应的 Patch，如图就是一个矩形 Layer 对应缩放参数形成的控件。与 QC 比较大的区别就在于此。

![](/assets/ractangle.png)

## 3. 示例：

1. 启动 Origami Studio 新建一个项目，然后点击窗口右上角的加号，输入Rectangle 按return即可添加一个矩形。
2. 选中图层列表中的矩形图层，窗口右上角会出现矩形图层对应的参数。点击 Scale 参数名，在窗口会新增一个蓝色的 Patch。
3. 按command+return呼出搜索控件库的对话框，输入 Interaction 按return，窗口即出现transition控件。同理再添加 Popanimation 和 Transition 控件。此时应当如图，如果连线不正确可以按照图上所示将对应参数连接。
   ![](/assets/connect.png)
4. 将interaction 的 Layer 参数改为矩形的图层名，将Transition的参数改为 Start= 1；end = 0.4
5. 点击矩形试试，你应该得到一个有弹性的矩形按钮。



