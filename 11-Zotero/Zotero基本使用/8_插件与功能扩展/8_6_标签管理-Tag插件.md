---
uid: 20230817143825
title: 8.6- 标签管理：Tag 插件
tags: [zotero]
description: 
author: winding,ShareStuff
type: other
draft: false
editable: false
modified: 20230817193115
---

# 8.6- 标签管理：Tag 插件

## [![109afa6f613a740e70186ec61249a91c_MD5](https://cdn.pkmer.cn/images/202308171546720.png!pkmer)](https://github.com/windingwind/zotero-tag/blob/master/addon/chrome/skin/default/zoterotag/favicon.png)Zotero Tag 插件介绍

主页与下载：[https://github.com/windingwind/zotero-tag](https://github.com/windingwind/zotero-tag)

_One add-on to rule Tags all._

用一个插件管理 Zotero 中的标签。

- 自定义动作（添加文献，关闭阅读器等）时自动添加已读、未读标签
- 标签批处理
- 自定义标签组与快捷键
- 批量导出标签为 CSV/从 CSV 批量导入标签

## 使用

安装插件后，可在库视图中选中数个条目，右键菜单选择管理标签，即可批量添加、移除、检查较少使用标签、导入导出标签。

[![b2549db57c2d46b7ea693d66f6216ffb_MD5](https://cdn.pkmer.cn/images/202308171546721.png!pkmer)](https://github.com/windingwind/zotero-tag/blob/master/imgs/readme-settings-rightclickmenu.png)

其他设置可在编辑 ->首选项找到。

## 设置

## 标签组规则

使用标签组规则来批量管理标签。为每个标签组分配指定动作: 条目添加时/条目打开时/条目关闭时……，并在动作触发时为对应条目添加/移除标签组；

使用半角逗号 ','(comma) 分隔标签组中的多个标签；在标签前加前缀 '~~' 以指明该标签的行为是移除，默认是添加;

**例:** 要为新添加的条目设置 /unread 标签，并在阅读完成（关闭 Zotero 阅读器）时移除未读标签，则：

| **标签** | **动作**             |
| -------- | -------------------- |
| /unread  | add on item add      |
| /unread  | remove on item close |

[![f3f6f070fb00eda2f798531a4eb57166_MD5](https://cdn.pkmer.cn/images/202308171546722.png!pkmer)](https://github.com/windingwind/zotero-tag/blob/master/imgs/readme-settings-rule.png)

## 快捷键

Alt+(1-9) 可分配给标签组。

[![d92c55070b5103625ef144fcef5ede4a_MD5](https://cdn.pkmer.cn/images/202308171546723.png!pkmer)](https://github.com/windingwind/zotero-tag/blob/master/imgs/readme-settings-shortcuts.png)

## 彩色标签

[Colorize Guide](https://github.com/windingwind/zotero-tag/blob/master/docs/tag-color.md)

## 星级

[Setting Guide](https://github.com/windingwind/zotero-tag/blob/master/docs/item-star.md)

[![21e6f082f9c6c08bca3fb10bf1d64573_MD5](https://cdn.pkmer.cn/images/202308171546724.png!pkmer)](https://user-images.githubusercontent.com/33902321/159643528-9eb77420-9c93-4244-b6e5-f9720af7698e.png)

## 高级能力

- 在库视图中右键点击条目或分类
- 点击 'Manage Tags/管理标签 '

[![67ba44c5106b9fe7182ac8b18f72ed50_MD5](https://cdn.pkmer.cn/images/202308171546725.png!pkmer)](https://github.com/windingwind/zotero-tag/blob/master/imgs/readme-manage-tags.png)

### 添加/移除标签

输入标签 (半角逗号 `,` 分隔) 并点击 OK.

### 检查较少使用的标签

单击“较少使用的标签”并输入阈值 N。所选分类中的标签将被计数，使用次数少于 N 次的标签将填入输入框和剪贴板 (半角逗号 `,` 分隔)。

### 导出标签

单击“导出标签”。如果您还想导出子分类中的所有标签，请选中“包含子分类”。

CSV 文件列为：标签名、计数、条目名称、条目 id。

### 导入标签

从 CSV 文件导入标签并将其应用于当前分类/库中的所有项目。

CSV 文件列必须为：

- 模式（+ 表示添加，- 表示删除，=表示替换）
- 目标标签。
- 匹配的标签 (半角逗号 `,` 分隔)，。如果一个项目具有这些标签中的一个，目标标签将被添加到其中（添加模式）/从中移除（移除模式）/相应地替换匹配的标签（替换模式）。如果匹配的标签为空，则将匹配所有项目。

不需要标题行。

CSV 文件内容示例：

```
+,/unread,/new
-,toremove,
=,BIM,building information modeling,Building Information Modeling (BIM)
=,this is comma($COMMA$),$COMMA$

```

每行的说明：

1. 带有标签 `/new` 的条目将被添加标签 `/unread`
2. 所有条目将移除 `toremove` 标签。
3. `building information modeling` 和 `Building Information Modeling (BIM)` 标签将被替换为 `BIM` 标签。
4. `,` 标签将替换为 `this is comma(,)`。在输入 CSV 文件中，标签中的半角逗号应替换为 `$COMMA$`。

下一篇 [[8_7_查询引用次数]]