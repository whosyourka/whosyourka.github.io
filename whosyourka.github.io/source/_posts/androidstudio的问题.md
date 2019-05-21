---
title: android studio问题
date: 2019-02-13
tags: android studio
categories: android studio
---



1.as配置：卡死原因

- 不能翻墙，请使用lantern
- 配置阿里的gradle源

2.编译异常

> Error:Execution failed for task ':processDebugResources'. com.android.ide.common.process.ProcessException: Failed to execute aapt

问题是android10的jar问题，或者是版本build工具问题

3.错误The APK file xxxx Error while Installing APK
有可能是build Variants的问题

4.Cannot find System Java Compiler. Ensure that you have installed a JDK (not just a JRE) and configured your JAVA_HOME system variable to point to the according director.
配置jdk环境

5.Error:All flavors must now belong to a named flavor dimension. 

gradle升级问题：Learn more at <https://d.android.com/r/tools/flavorDimensions-missing-error-message.html> 见[github](https://github.com/googlecodelabs/android-testing/issues/85)

6.Android Studio快捷键失效的问题 ：qq，微信，有道翻译，输入法热键 冲突