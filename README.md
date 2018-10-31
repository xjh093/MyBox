# MyBox
What's in my github? 我的仓库有些什么？仓库列表，仓库项目，仓库介绍

# 目录
- JHViewCorner - 一行代码搞定圆角
- JHFrameLayout - 一款轻量级的自动布局框架
- JHInputLimit - 一套友好的输入限制方案
- JHCollectionViewFlowLayout - 自定义CollectionView横向排版
- JHNumberKeyboardView - 自定义数字键盘
- JHAlertView - 一款黑白配色的HUD之沙漏效果
---

# 项目

## JHViewCorner - 一行代码搞定圆角
- 地址:

https://github.com/xjh093/JHViewCorner


- 简介:

Set view's corner with one code! 

一行代码完成视图的圆角设置。

原理：采用遮罩的形式，覆盖在视图上。

目前有两种遮罩：圆角遮罩，心形遮罩。

支持视图某个位置的圆角处理，比如只想把左上角处理成圆角。

支持 `UITableViewCell` 的点击高亮处理。

支持生成多个遮罩，处理不同情况下，显示不同的效果。

注意：遮罩的颜色应该与视图所在的父视图一致。

性能：在某些机型上，能达到 60 FPS!

---

## JHFrameLayout - 一款轻量级的自动布局框架
- 地址:

https://github.com/xjh093/JHFrameLayout

- 简介

链式语法，布局容器视图

布局时间对比：

`Frame` vs `JHFrameLayout` vs `MyFlowLayout`

![image](https://github.com/xjh093/JHFrameLayout/blob/master/image1.png)

- 示例：

```
- (void)loadView{

    self.view = [[JHFrameLayoutView alloc] initWithFrame:[UIScreen mainScreen].bounds];

    UIView *view1 = [[UIView alloc] init];
    view1.backgroundColor = [UIColor grayColor];
    [self.view addSubview:view1];
    
    view1.jhLayout
    .topOffsetBottomOfView(10, self.navigationController.navigationBar, NO)
    .leftIs(10)
    .bottomOffsetMiddleOfView(-50, self.view, YES)
    .rightOffsetMiddleOfView(-5, self.view, YES);
}
```

---

## JHInputLimit - 一套友好的输入限制方案
- 地址：

https://github.com/xjh093/JHInputLimit

- 简介

对'UITextField' and 'UITextView'的输入进行限制

三种限制：
- 长度限制
- 类型限制
- 自定义字符限制

三种限制可以组合使用。

- 示例：
```
    _textView.jh_inputLimit.length = 9;
    _textView.jh_inputLimit.type = JHInputLimitType_Alphabet | JHInputLimitType_Digital | JHInputLimitType_MyCharacters;
    _textView.jh_inputLimit.myCharacter = [NSSet setWithArray:@[@"!",@","]];
```

---

## JHCollectionViewFlowLayout - 自定义CollectionView横向排版
- 地址：

https://github.com/xjh093/JHCollectionViewFlowLayout

- 简介

系统的横向排版

是从上到下，从左往右排版

想要从左到右，从上到下的排版

那就需要自定义了

为什么不来看看这个？

---

## 自定义数字键盘
- 地址：

https://github.com/xjh093/JHNumberKeyboardView

- 简介

作为 textField 与 textView 的 inputView 使用

可以限制输入长度

适配横坚屏

适配iPhoneX

![image](https://github.com/xjh093/JHNumberKeyboardView/blob/master/Screen%20Shot%202017-10-17%20at%2017.49.36.png)

---

## JHAlertView - 一款黑白配色的HUD之沙漏效果
- 地址：

https://github.com/xjh093/JHAlertView

- 简介

采用遮罩方式实现的一款HUD

沙漏效果

![image](https://github.com/xjh093/JHAlertView/blob/master/image/image3.gif)
![image](https://github.com/xjh093/JHAlertView/blob/master/image/image5.gif)

---





