# MyBox
What's in my github? 我的仓库有些什么？仓库列表，仓库项目，仓库介绍

# 目录
- JHViewCorner - 一行代码搞定圆角
- JHFrameLayout - 一款轻量级的自动布局框架
- JHInputLimit - 一套友好的输入限制方案
- JHCollectionViewFlowLayout - 自定义CollectionView横向排版
- JHNumberKeyboardView - 自定义数字键盘
- JHAlertView - 一款黑白配色的HUD之沙漏效果
- JHAddressPickView - 省市区选择器
- JHVerificationCodeView - 验证码输入
- JHIAPManager - 一行代码完成内购
- JHLinkedTextView - 富文本的点击事件
- JHNoDataEmptyView - 零行代码实现占位图
- JHRedDot - 小红点方案
- JHActioinSheet - 自定义的 action sheet，行数过多时可指定可见行数
- JHAnimatedImageView - 高性能的帧动画
- JHAudioManager - 应用启动播放短音频
- JHAutoLayout - 另一种自动布局方式
- JHCountdownButton - 倒计时按钮
- JHEmojiKeyboard - Emoji表情键盘
- JHFileDownloadManager - 文件下载 & 多文件下载 & 断点续传
- JHFMDBManager - 简单地封装了一下FMDB
- JHGradualProgressView - 渐变进度条
- JHGuidePageView - 一行代码搞定引导页
- JHHolderTextView - 有占位提示的TextView
- JHInputPayPWDView - 6位密码输入框
- JHLanguage - 两行代码搞定本地化多语言
- JHLaunchAD - 应用启动广告页
- JHNineImageView - 九宫格图片展示
- JHPhotoChangeManager - 拍照 or 从相册选择
- JHRequestDebugView - 请求调试窗口
- JHRSAEncoder - RSA加解密
- JHSlider - 动态展示当前进度
- JHSoundWaveView - 音波图，声波图
- JHThirdPartyPay - 微信支付宝支付工具类
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

![image](https://github.com/xjh093/JHCollectionViewFlowLayout/blob/master/custom.png)

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

# JHAddressPickView - 省市区选择器
- 地址：

https://github.com/xjh093/JHAddressPickView

- 简介

省市区选择器

省市二级选择

省市区三级选择

有完整的 code 码

- 示例

```

    _pickView = [[JHAddressPickView alloc] init];
    _pickView.hideWhenTapGrayView = YES;
    _pickView.columns = 2;    // 省市二级选择
    //_pickView.columns = 3;  // 省市区三级选择
    [_pickView showInView:self.view];
    
    // 选择结果
    
     {
       city = "北京市";
       cityCode = 110100;
       province = "北京";
       provinceCode = 110000;
    }
    
    {
      city = "北京市";
      cityCode = 110100;
      province = "北京";
      provinceCode = 110000;
      town = "东城区";
      townCode = 110101;
    }
```

![image](https://github.com/xjh093/MyBox/blob/master/JHAddressPickView1.png)

![image](https://github.com/xjh093/MyBox/blob/master/JHAddressPickView2.png)


---

# JHVerificationCodeView - 验证码输入
- 地址：
https://github.com/xjh093/JHVerificationCodeView

- 简介

看图

![image](https://github.com/xjh093/JHVerificationCodeView/blob/master/image.png)

---

# JHIAPManager - 一行代码完成内购
- 地址：
https://github.com/xjh093/JHIAPManager

- 简介

封装了内购流程

一行代码完成内购

有越狱逻辑判断

还有针对未完成的支付处理

```
AppDelaget.m

 - (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
 
    //内购监听-针对未完成支付
    [JHIAPManager iapManager].delegate = self;
    
    .....
 }
 
 - (void)jh_paymentSuccess:(SKPaymentTransaction *)transaction{
     //do something about buying
     //finish transaction
 }
```

---

# JHLinkedTextView - 富文本的点击事件
- 地址：
https://github.com/xjh093/JHLinkedTextView

- 简介

![image](https://github.com/xjh093/JHLinkedTextView/blob/master/image.png)

---

# JHNoDataEmptyView - 零行代码实现占位图
- 地址：
https://github.com/xjh093/JHNoDataEmptyViewForT-C

- 简介：

最开始是零行代码实现占位图

后来发现影响范围太广了

就设置了开关属性

可以自由开启

配合代理使用

可定制更好的占位图

---

# JHRedDot - 小红点方案
- 地址：
https://github.com/xjh093/JHRedDot

- 简介：

自动靠右

通过 JHRedDotConfig 配置更多属性

![image](https://github.com/xjh093/JHRedDot/blob/master/image/1.png)

![image](https://github.com/xjh093/JHRedDot/blob/master/image/2.png)

![image](https://github.com/xjh093/JHRedDot/blob/master/image/3.png)

![image](https://github.com/xjh093/JHRedDot/blob/master/image/4.png)

![image](https://github.com/xjh093/JHRedDot/blob/master/image/5.png)

---

# JHActioinSheet - 自定义的 action sheet，行数过多时可指定可见行数
- 地址：
https://github.com/xjh093/JHActioinSheet

- 简介

![image](https://github.com/xjh093/JHActioinSheet/blob/master/image.png)

---

# JHAnimatedImageView - 高性能的帧动画
- 地址：
https://github.com/xjh093/JHAnimatedImageView

- 简介

对比了 KKSequenceImageView、YYAnimatedImageView、JHAnimatedImageView、UIImageView

在播放帧动画时 内存 与 CPU 的使用率

---

# JHAudioManager - 应用启动播放短音频
- 地址：
https://github.com/xjh093/JHAudioManager

---

# JHAutoLayout - 另一种自动布局方式
- 地址：
https://github.com/xjh093/JHAutoLayout

- 简介

通过一个字符串来描述 view 的 frame

对字符串进行解析后设 view 的 frame

从而实现动态布局

因为是字符串

可以用 JSON 来描述

你懂的~

---

# JHCountdownButton - 倒计时按钮 
- 地址：
https://github.com/xjh093/JHCountdownButton

- 简介

看图一目了然

![image](https://github.com/xjh093/JHCountdownButton/blob/master/img/01.png)

![image](https://github.com/xjh093/JHCountdownButton/blob/master/img/02.png)

---

# JHEmojiKeyboard - Emoji表情键盘
- 地址：
https://github.com/xjh093/JHEmojiKeyboard

- 简介

Emoji表情键盘

有两套表情可以选择

---

# JHFileDownloadManager - 文件下载 & 多文件下载 & 断点续传
- 地址：
https://github.com/xjh093/JHFileDownloadManager

- 简介

```
    [[JHFileDownloadManager manager] jh_downFileWith:[NSURL URLWithString:URL] progress:^(float progress) {
        NSLog(@"%@",@(progress));
    } success:^(NSString *path) {
        // path : file in sandbox
        NSLog(@"下载完成 & download success!");
    } failer:^(NSError *error) {
        NSLog(@"下载失败 & download fialer!");
    }];
```

---

# JHFMDBManager - 简单地封装了一下FMDB

- 地址：
https://github.com/xjh093/JHFMDBManager

- 简介

真的是很简单

继承 JHFMDBManager

实现子类的 增删改查

请参考Demo

---

# JHGradualProgressView - 渐变进度条

- 地址：
https://github.com/xjh093/JHGradualProgressView

- 简介

![image](https://github.com/xjh093/JHGradualProgressView/blob/master/image.png)

边框颜色随颜色变化而变化

---

# JHGuidePageView - 一行代码搞定引导页

- 地址：
https://github.com/xjh093/JHGuidePageView

- 简介

最少传递一个图片数组即可

可传入一个跳转的自定义按钮

---

# JHHolderTextView - 有占位提示的TextView

- 地址：
https://github.com/xjh093/JHHolderTextView

- 简介

![image](https://github.com/xjh093/JHHolderTextView/blob/master/images.png)

---

# JHInputPayPWDView - 6位密码输入框

- 地址
https://github.com/xjh093/JHInputPayPWDView

- 简介

![image](https://github.com/xjh093/JHInputPayPWDView/blob/master/JHInputPayPWDView/Images/001.png)

---

# JHLanguage - 两行代码搞定本地化多语言

- 地址
https://github.com/xjh093/JHLanguage

- 简介

两行代码搞定本地化多语言

```
kJHSetLanguage(lan)
kJHLocalizedString(key,tab)
```
---

# JHLaunchAD - 应用启动广告页

- 地址
https://github.com/xjh093/JHLaunchAD

- 简介

![image](https://github.com/xjh093/JHLaunchAD/blob/master/Screen%20Shot%202017-09-30%20at%2010.28.43.png)

---

# JHNineImageView - 九宫格图片展示

- 地址
https://github.com/xjh093/JHNineImageView

- 简介

![image](https://github.com/xjh093/JHNineImageView/blob/master/PNG/Screen%20Shot%202018-04-09%20at%2018.04.20.png)

---

# JHPhotoChangeManager - 拍照 or 从相册选择

- 地址
https://github.com/xjh093/JHPhotoChangeManager

- 简介

![image](https://github.com/xjh093/JHPhotoChangeManager/blob/master/image/image.png)

---

# JHRequestDebugView - 请求调试窗口

- 地址：
https://github.com/xjh093/JHRequestDebugView

- 简介

摇一摇即可出现的请求调试窗口

有JSON格式化功能

包含历史请求列表

方便查看历史请求数据

---

# JHRSAEncoder - RSA加解密

- 地址
https://github.com/xjh093/JHRSAEncoder

- 简介

RSA encode with openssl

突破117的长度限制

---

# JHSlider - 动态展示当前进度

-地址
https://github.com/xjh093/JHSlider

-简介

![image](https://github.com/xjh093/JHSlider/blob/master/JHSlider.gif)

![image](https://github.com/xjh093/JHSlider/blob/master/JHSlider.png)

---

# JHSoundWaveView - 音波图，声波图

-地址
https://github.com/xjh093/JHSoundWaveView

- 简介

![image](https://github.com/xjh093/JHSoundWaveView/blob/master/Image/Nov-22-2018%2018-16-15.gif)

![image](https://github.com/xjh093/JHSoundWaveView/blob/master/Image/Nov-22-2018%2018-16-57.gif)

---

# JHThirdPartyPay - 微信支付宝支付工具类

- 地址
https://github.com/xjh093/JHThirdPartyPay

---








