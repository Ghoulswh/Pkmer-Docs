---
uid: 2023082011361342
title: Obsidian 插件：【Readme】Source Scanner
tags: ['obsidian插件', 'readme']
description: 从源代码中提取注释并将其放置在md文件中的扫描器
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：【Readme】Source Scanner

> [!Note] 插件名片
> - 插件名称：Source Scanner
> - 插件作者：Gerrie Myburgh
> - 插件说明：从源代码中提取注释并将其放置在md文件中的扫描器
> - 插件分类：['obsidian插件', 'readme']
> - 项目地址：[点我访问](https://github.com/gerrie-myburgh/source-scanner)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?source-scanner)

## 概述

从源代码中提取注释并将其放置在md文件中的扫描器



> [!tip] 原文出处
> 
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/gerrie-myburgh/source-scanner/master/README.md)
> 

---

## Readme(翻译）

下面是 [[source-scanner]] 插件的自述翻译


# 源代码扫描器

将源代码中的注释提取为笔记。该插件仅适用于Obsidian桌面应用程序。
插件试图解决的问题是，使用敏捷方法论的开发人员存在文档问题。敏捷并不意味着没有文档，而是只需要必要的文档。为了使开发人员能够最大程度地减少工作量，以展示如何满足和解决业务需求，需要使用工具。

从开发人员的角度来看，最简单的解决方案是将业务需求的解决方案记录在代码本身中。最理想的地方是在源代码的块和行注释中进行此操作。然后，您需要的是将这些注释提取为注释，并将注释与用户需求相关联的工具。用户需求将以用户故事的形式出现，也是以注释的形式存在。
## Git 依赖

该插件依赖于 git 来检查当前分支是否是要扫描的分支。为了实现这一点，您需要添加以下 git 钩子脚本：post-checkout。如果您想要欺骗代码扫描器，让其认为正在扫描的代码正在使用版本控制，则需要在项目的根目录中创建一个 current-branch.txt 文件，并将分支的名称放入该文件中。该分支名称的值必须与插件设置中定义的名称相同。

以下是 Linux 上的一个 git 钩子脚本示例。

```agsl
#!/bin/bash
git branch --show-current > current-branch.txt
```
这个插件的使用案例如下：

0. 这个插件仅限于像Java、Scala、C、C++、TypeScript和JavaScript这样具有块注释和行注释的源语言。
1. 扫描源代码文件，将注释写入当前指定的文档库中的注释中。这些注释可以包含Markdown文本。
2. 将注释与敏捷用户故事相关联。
3. 创建一个标记表，其中包含标记出现的注释的位置。
## 在源代码中扫描的注释类型

插件从源文件中提取以下类型的注释，并将其写入markdown注释```/** ... */```和```//bus ...```。 
这个想法是只提取与解决业务规则相关的注释。其他类型的注释，如```/* ... */```和```// ....``` 
被忽略，因为它们被认为是解释实现中的其他技术要点的注释。

以下是一个被提取的块注释示例：

```agsl
  /**
   * ## onload()
   * 加载插件并设置命令
   * 1. 添加一个命令来触发解决方案文件的创建。在运行命令之前确保所有配置都已完成
   * 2. 添加一个功能按钮命令来切换扫描“开启”或“关闭”。在启动扫描之前确保已配置扫描器。
   */
```

在指定的文档存储库中，相关注释将呈现如下。
# onload()
加载插件并设置命令

1. 添加一个命令来触发解决方案文件的创建。在运行命令之前确保所有配置都已完成。
2. 添加一个功能按钮命令，用于切换扫描“开启”或“关闭”。在启动扫描之前确保扫描仪已配置好。
### 注释文件命名约定

扫描器必须配置以告诉它源代码在文件系统中的位置。一旦完成这一步骤并且扫描器被打开，那么注释的名称将是被扫描的类的完全限定名称后面加上".md"。这是一个注释名称的示例：

**crosscut.CrossCuttingConcerns.md**

在这种情况下，被扫描的文件可能是：

**crosscut/CrossCuttingConcerns.scala**
与用户故事的笔记相关性

现在可以通过选择菜单选项来将生成的文档笔记与用户故事相关联：

**创建解决方案文件**

这将创建将用户故事笔记与文档笔记链接起来的映射笔记。
### 用户故事。

将用户故事提供给开发人员，他/她可以从这些初始故事中创建子故事。通过在源代码注释中使用标记，您可以针对故事的解决方案创建横切关注点。

注释的标记形式如下：

```agsl
( |\t)\^([a-zA-Z0-9]+\-)*[a-zA-Z0-9]+\-[0-9]+
```

一个例子是：^story1-00。一旦这些标记被放置在源代码注释中，系统就可以在注释和故事之间创建映射。解决方案文件将如下所示：

![[stories/update-payment-limits/summary of requirement#^summary]]

![[utils.Lexer.md#^story1-00]]

![[Main.md#^story1-02]]
创建一个标记表

一旦标记被放置在源文件中，那么对于想要生成解决方案注释和故事注释的人来说，它们基本上是无法找到的。为了更容易看到哪个标记在哪个注释中以及它们的顺序，提供了功能来生成所有标记的列表，以及它们所在的注释文件名。

这样可以更容易地根据需要更新源代码中的标记。一个这样的映射表的示例是

|标记|文档|
|------|--------|
|story1-00|[[utils.Lexer.md#^story1-00]]|
|story1-02|[[Main.md#^story1-02]]|
|story2-00|[[Main.md#^story2-00]]|
## 可在插件设置中设置的用户变量

 * 应用程序路径：要扫描的应用程序文件的文件路径。
 * 要扫描的Git分支：要扫描的Git分支。如果这不是当前分支，则扫描器将不会扫描这些已签出的文件以查找注释。
 * 文档路径：注释注释应放置的路径。
 * 应用程序扩展名：源文件的扩展名类型，例如对于Java，.java等。
 * SleepLength：扫描源文件之间的持续时间（以毫秒为单位）。
 * 按大小分组：扫描源文件时，会分批进行。按大小分组是批处理大小。
 * 用户故事文件夹：存放用户故事注释的文件夹
 * 解决方案文件夹：生成解决方案注释的文件夹
 * 标记映射：如果用户不想使用默认的故事名称来定义标记，则可以定义标记到新注释名称之间的映射关系
 * 标记路径：标记表注释的路径和名称。

设置中正确的值示例。

![img.png](img.png)



