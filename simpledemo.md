# 实现简单原型

过去 QC+Origami 的弊病之一即是创建页面跳转相对复杂，导致制作多页面 DEMO 时效率底下。不过 Origami Studio 中引入了 Screen 解决了这个问题，配合 Hit area 层即可制作简单的原型。

Screen 是 Layer，需要点击“+”添加。（在列表的较后位置可以找到）Screen 层可以理解为一个带转场动画的 Group 层，可收纳其他的层。输入Present/Dismiss 两个值能显示或隐藏层，默认的转场动画是 Push 从右侧滑入，也可以改成 None 不需要动画或 Modal 从底部滑入。

![](/assets/Origami-3-1-Screen.png)

Hit area 与其它层一样，可以添加各种交互动作。添加后在预览窗会出现一个半透明的红色矩形，可以修改 PositionX/Y/Z 与 SizeH/W 等。它的优势在于可以一键切换 Setup Mode ，显示或隐藏层。（点击右上角 Touch 按钮可添加 Interaction 组件）

![](/assets/Origami-3-2-HitArea.png)

示例：

1. 准备两个页面素材
   ![](/assets/Origami-3-3-mate.png)
2. 打开 Origami 新建工程，将两个页面拖入右侧图层列表。
3. 点击“+”添加层，1 个 Screen 和两个 Hit Area，如图排序。注意 Hit Area 与二级页面是 Screen 的子级。
   ![](/assets/Origami-3-4-list.png)
4. 调整 Hit Area 的 SizeW/H 与Position 参数，使预览如图。
   ![](/assets/Origami-3-5-view.png)
5. 给两个 Hit Area 添加 Interaction 组件。分别连接至Screen 层的 Present 与 Dismiss。如图
   ![](/assets/Origami-3-6-connect.png)

![](/assets/Origami-3-7-f2.gif)

