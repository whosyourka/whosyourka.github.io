---
title: android studio个人常用配置
date: 2019-01-23 17:09:37
tags: android studio
categories: android studio
---

# 我的基本重要的设置部分：

- **Setting->IDE setting->editor->appearance, 右侧页面中勾选 show line numbers项 和 show whitespace**。
- **File Encodings 修改utf-8**
- **设置光标悬停时提示文档注释：File | Settings | Editor | General ——> 勾选 Show quick doc on mouse Delay…**
- 
- **Edit > File and Code Templates > include > File Header 设置头部注释（包括kotlin和java）**
- **模板配置 Live Templates（书写） 和 新建个人自定义activity等的模板（new->edit file templates）**
- 
- edit > font 设置字体 14
- appearance&bhehavior > Appearance 设置字体 14
- 设置 system settings 的reopen last project on startup 项目关闭后下次重启会自动打开

## 项目加速：

gradle.properties设置：

```
  #（最大允许分配的堆内存，按需分配） 和（最大允许分配的非堆内存，按需分配）
  org.gradle.jvmargs=-Xmx4096m -XX:MaxPermSize=1028m -XX:+HeapDumpOnOutOfMemoryError -Dfile.encoding=UTF-8
  #（开启守护线程）  
  gradle.properties添加 org.gradle.daemon=true 
  #（开启并行编译）  
  gradle.properties添加 org.gradle.parallel=true  
```

andorid.dexOptions设置：

```
  preDexLibraries true
  javaMaxHeapSize "3g" 根据上面的jvm进行设置至多比jvm少1g，设置 dex 操作的最大内存分配池大小
  dexInProcess = true 
  maxProcessCount 8 设置可以并行启动的 DEX 进程的最大数量。
```

gradle编译时间日志输出：

```
  public class BuildTimeListener implements TaskExecutionListener, BuildListener {
    private Clock clock
    private times = []

    @Override
    void beforeExecute(Task task) {
        clock = new org.gradle.util.Clock()
    }

    @Override
    void afterExecute(Task task, TaskState taskState) {
        def ms = clock.timeInMs
        times.add([ms, task.path])

        //task.project.logger.warn "${task.path} spend ${ms}ms"
    }

    @Override
    void buildFinished(BuildResult result) {
        println "Task spend time:"
        for (time in times) {
            if (time[0] >= 50) {
                printf "%7sms  %s\n", time
            }
        }
    }
    @Override
    void buildStarted(Gradle gradle) {}
    @Override
    void projectsEvaluated(Gradle gradle) {}
    @Override
    void projectsLoaded(Gradle gradle) {}
    @Override
    void settingsEvaluated(Settings settings) {}
}

project.gradle.addListener(new BuildTimeListener())
```
