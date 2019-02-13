---
title: android studio个人常用插件推荐
date: 2019-01-23 17:06:31
tags: android studio
categories: android studio
---

# 个人常用AS插件([参考一](https://note.youdao.com/)，[参考二](https://note.youdao.com/)，[参考三](https://note.youdao.com/)，经常用的也就几个，看top就可以了，太多浪费时间)：

- **代码规范工具：Alibaba Java Coding Guidelines 和 sonar lint**
- **智能提速：Codota (需要账号登录)**
- **Gradle Killer 中断gradle编辑器**
- **ADB WIFI :无需root就能wifi调试**
- **LayoutCreator:类似butterknife，自动编写findbyid**
- **GsonFormat和GsonOrXmlFormat:自动生成实体类**
- **[Settings Repository:as设置专用](https://github.com/whosyourka/my_as_setting) : android studio自带，首先配置repository地址，然后就可以合并本地，覆盖本地，覆盖远程配置的操作了。内容为：**
    - 文件夹内容：**keymap的多个配置，Editor->Live Templates配置，Editor->inspections配置，Editor->File and Code Templates配置 ，Editor->Color Scheme配置（字体大小颜色之类的），Editor->Code Style配置，window外貌配置**
    - 文件内容：暂不了解，了解的请提示一下。
- **.ignore：上传忽略文件设置**
- **MVPHelper:一款Intellj IDEA 和Android Studio的插件，可以为MVP生成接口以及实现类，解放双手**
- **ECTranslation：翻译插件**
- **genymotion:模拟编辑器**
- **adb idea:adb部分常用功能**


## 不常用（后续可能会用到）

- Gradle View :查看gradle的依赖
- Licecap:gif录制 
- SingletonTest:6种单例模式
- AndroidProguardPlugin：自动编辑混淆文件(暂时没有插件)(扩展)
- dexcount gradle plugin和Android Methods Count：统计apk函数数量
- Material Theme UI:添加Material主题到你的AS
- CodeGlance：快速浏览代码专用，右边缩略图
- Lifecycle Sorter：专为强迫症使用。生命周期归纳
- folding plugin:专为强迫症使用。文件分组专用
- jimu Mirror：类似instantRun，需要特殊配置
- JRebel for Android:快速进行启动apk
- CheatSheet：快捷键显示
- Android Code Generator 由xml快速生成Activity，Fragment，Adapter，Menu
- Fastdex Plugin 快速启动apk（原理跟instant run类似）
- JavaDoc:添加注释(扩展)，sdk专用控件
- Gradle Dependencies Helper：gradle编写补全插件
  件，

## 资源相关：

- Android Holo Colors Generator 通过自定义Holo主题颜色生成对应的Drawable和布局文件
- strings xml tools:字符串处理
- android selector chapek:转换状态图片成seletor.xml
- Android Styler：根据xml文件生成style文件的插件
- AndroidPixelDimenGenerator：Android Studio自动生成dimen.xml文件插件
- AndroidLocalizationer 可用于将项目中的 string 资源自动翻译为其他语言的 Android Studio/IntelliJ IDEA 插件

## 第三方相关

- otto intellij plugin  otto事件导航工具。
- eventbus intellij plugin  eventbus导航插件
- dagger intellij plugin  dagger可视化辅助工具