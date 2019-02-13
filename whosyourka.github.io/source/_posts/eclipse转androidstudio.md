---
title: eclipse转android studio
date: 2019-01-23 17:06:31
tags: android studio
categories: android studio
---

## eclipse转android studio，2者共用

- eclipse和android studio共用（AS直接导入eclipse可能只能用AS编程了）：eclipse首先要export出build文件出来，然后才可以引入到AS里面，这样就可以在as或者eclipse编程了，缺点引包还是需要自己下载等。

- 项目编码设置(旧项目有些是用GBK)


```
android.sourceSets { compileOptions { encoding "GBK" } }
tasks.withType(JavaCompile) { options.encoding = "GBK" }
```


- 其次是so文件，放在libs下的时候（推荐把jni下的c代码编译成so文件）

```
android.sourceSets.main{ jniLibs.srcDirs = ['libs'] } 
```


- android系统包低于自己公司定制的系统包，则

```
    provided  files('classlib/xxxxxx.jar')
  
    gradle.projectsEvaluated {
        tasks.withType(JavaCompile) {
            options.compilerArgs.add('-Xbootclasspath/p:C:\\home\\workplace\\lakalasdk\\classlib\\xxxxxx.jar')
        }
    }
```
