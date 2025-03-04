---
uid: 2023080322180623
title: Obsidian 插件：【Readme】Fantasy Calendar
tags: ['日期相关', 'obsidian插件', 'readme']
description: 在 Obsidian 中使用 Fantsy Calendar。
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：Fantasy Calendar

> [!Note] 插件名片
> - 插件名称：Fantasy Calendar
> - 插件作者：Jeremy Valentine
> - 插件说明：在 Obsidian 中使用 Fantsy Calendar。
> - 插件分类：[' 日期相关 ', 'obsidian 插件 ', 'readme']
> - 项目地址：[点我访问](https://github.com/fantasycalendar/obsidian-fantasy-calendar)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?fantasy-calendar)

## 概述

在 Obsidian 中使用 Fantsy Calendar。

![Fantasy Calendar](https://cdn.pkmer.cn/covers/fantasy-calendar.PNG!pkmer)

> [!tip] 原文出处
>
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/fantasycalendar/obsidian-fantasy-calendar/master/README.md)
>

---

## Readme(翻译）

下面是 [[fantasy-calendar]] 插件的自述翻译

# 幻想日历

**现在是 [幻想日历](https://fantasy-calendar.com/) 家族的一部分！**

在 Obsidian 中创建幻想日历！

![](https://raw.githubusercontent.com/valentine195/obsidian-fantasy-calendar/master/assets/example.png)

<table>
<tbody>
<tr>
<td>

</td>
<td>

</td>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>
<tbody>
</table>

使用插件

插件将在启动时在右侧窗格中添加一个日历视图。如果工作区中没有日历视图，可以使用“打开幻想日历”或“打开大型幻想日历”命令添加一个。

> **:pencil: 第一次打开插件？**
>
> 插件不会预装任何日历。您必须自己创建它们！
>
> 有关更多信息，请参见 [创建日历](#creating-a-calendar) 和 [日历预设](#presets)。

> **:calendar: 在现实世界中使用插件？**
>
> 插件的公历日历 [预设](#presets) 是完全准确的！

### 命令

打开幻想日历

此命令将在侧边窗格中打开日历视图。

打开大型幻想日历

此命令将在中心窗格中打开一个日历视图。

#### 重新扫描事件

这将触发插件重新扫描所有日历的所有笔记中的事件。

这将触发插件重新扫描所选日历中的所有笔记，以查找事件。

### 大型和小型日历

根工作区中存在一个大型日历，而左侧或右侧窗格中存在一个小型日历。虽然有两个不同的命令，但是日历会自动检测它们在 Obsidian 中的位置 - 当您移动它们时，它们会相应地调整大小。

### 当前日期

可以通过右键单击某一天并选择“设为今天”来更改当前日期。此外，可以在日历设置菜单中更改当前日期，或者在插件设置中编辑日历来更改当前日期。

### 日历设置

在日历视图的右上角，会有一个“设置”按钮，点击后会打开一个菜单，其中包含一些常见的设置选项。

年视图

可以从此菜单打开或关闭日历的年视图。

#### 月亮

可以通过在菜单中选择选项来显示或隐藏月亮。

此外，在打开日历时还有一个“切换月亮”命令可用。

#### 查看日期

通过选择“查看日期”，可以打开任意日期。此外，还可以将日历的当前日期设置为该日期。

切换日历

插件将打开设置中设置的默认日历。可以通过从菜单中选择“切换日历”来切换任何给定视图的打开日历。

### 日视图

在小日历中，右键单击某一天会出现“打开日视图”的选项。这将在所查看的月份下方打开一个日视图窗格，显示该天的月亮状态和任何事件。

创建日历

可以在插件设置中创建和编辑日历。

### 预设

有几个常见的预设可应用于创建的日历，包括几个 TTRPG 设置和公历（或“真实”日历）。

### 基本信息

名称和描述

可以在此处输入日历的名称和描述。

#### 自动递增天数

该插件将尝试在每过去一天的真实时间中递增当前日历天数。

#### 当前日期

日历的当前日期在这里设置。

### 工作日

在这个部分可以创建和管理新的工作日。每个工作日必须有一个名称。

#### 溢出周

如果关闭，每个月都将从第一个工作日开始。否则，该月将从上个月最后一个工作日之后的工作日开始。

第一年的第一天将在这个星期几发生。

### 月份

在这个部分可以创建和管理新的月份。每个月份必须有一个名称和长度（天数）。

#### 闰月

月份也可以设置为闰月。闰月是一个不属于任何现有月份的单独一天。它们不对应任何星期几。

### 年份

在这个部分可以创建自定义年份。每个年份必须有一个名称。

如果创建了自定义年份，日历将仅限于指定的年份。

### 闰日

在这个部分可以创建和管理闰日。

闰日必须附加到一个月份，并给予一个条件。

#### 偏移量

在计算时，闰日的条件将会被偏移这么多年 - 例如，每 4 年出现一次闰日，偏移量为 1，则闰日将会出现在第 1 年、第 5 年、第 9 年...

#### 条件

闰年条件由三个部分组成 - 间隔、是否为“排他”条件以及在计算时是否忽略闰年的偏移量。

排他条件意味着当条件满足时，闰年**不会**适用。

在排他条件之后的非排他条件将覆盖排他条件。

#### 真实世界的例子

格里高利历的闰年有以下 3 个条件：

1. 间隔为 4，非排除，非偏移。
2. 间隔为 100，排除，非偏移。
3. 间隔为 400，非排除，非偏移。

这个闰年将每 4 年出现一次，但是**除非**年份能被 100 整除，否则不会出现，**除非**年份能被 400 整除。

### 闰年的闰日

闰日可以被设置为插入式的，这意味着它发生在月份的正常流程之外。这一周将被闰日打断，然后在下一个工作日继续，就好像闰日从未发生过一样。

设置闰日会增加两个新的设置：

1. 编号 - 如果设置为编号，闰日将按照正常的日期编号继续。
2. 在...之后 - 闰日将被添加到这一天之后的月份中。

### 事件

在这个部分可以创建和管理事件。

### 事件类别

可以在此部分创建和管理事件类别。

### 月亮

在这个部分可以创建和管理月亮。

#### 显示月亮

如果此设置打开，月亮将默认显示。在视图的日历设置菜单中，始终可以切换月亮的显示。

#### 月球创建

月球需要一个名称、周期和偏移量。此外，月球图形的表面和阴影颜色可以更改。

##### 周期

月亮将在每 `<cycle>` 天内完成一次完整的旋转。

月球周期的开始将被偏移这么多天。

事件

可以通过右键单击日期并选择“新建事件”或单击没有任何事件的日期来添加事件。

事件也可以通过编辑插件设置中的日历或通过笔记前置元数据自动创建。

在日视图或大型日历中单击事件标志将显示事件描述。

### 分类

事件可以分配给不同的分类（在插件设置中创建）。这将导致点和旗帜采用分类的颜色。

### 事件笔记

通过在事件创建模态框中添加笔记或通过自动创建前置元数据的方式，事件也可以链接到笔记。

当选择了一个笔记时，如果该笔记具有适用的前置元数据（如下所示），插件将询问您是否希望使用前置元数据来覆盖已输入的事件数据。

点击与笔记链接的事件时，将打开该笔记。

多天活动

通过在活动创建模态框中选择“添加结束日期”，可以使活动跨越多天。

### 事件间隔

您可以通过点击“添加间隔”按钮来设置事件的间隔。起始日期是必需的，但结束日期不是。

### 从前置元数据创建事件

目前支持以下前置元数据属性：

| 属性               | 描述                                                         |
| ----------------- | ------------------------------------------------------------ |
| `fc-date`         | 带有 `year`、`month` 和 `day` 参数的日期对象。                  |
| `fc-end`          | 带有 `year`、`month` 和 `day` 参数的日期对象。                  |
| `fc-category`     | 事件类别的名称。                                               |
| `fc-display-name` | 事件的可选显示名称。否则，将使用文件名。                       |

如果向事件添加具有上述前置元数据属性的注释，它将提示您解析这些属性；选择是将相应地设置事件属性。

#### 日期对象

日期对象**必须**采用以下格式（参数可以以任意顺序提供）：

```
---
fc-date:
  year: <数字>                                 # 可选。如果未提供，事件将每年发生一次。
  month: <月份名称> 或 <月份数字>    # 可选。如果未提供，事件将每月发生一次。
  day: <数字>
---
```

### 自动创建事件

此外，每个日历都可以使用前置标记自动创建事件。

您可以选择告诉插件仅在特定文件夹中监视新事件。如果将此设置留空，将在整个存储库中监视新事件。

自动事件创建使用 `fc-date` 和 `fc-category`，以及一个额外的属性：`fc-calendar`。

| 属性                            | 描述                                                                                       |
| ------------------------------- | ------------------------------------------------------------------------------------------ |
| [`fc-calendar`](#fc-calendar)   | 要将事件添加到的日历名称或日历名称数组。                                                   |
| [`fc-date`](#frontmatter-dates) | 日期字符串、日期对象或具有 `year`、`month` 和 `day` 参数的日期对象数组。                     |
| `fc-end`                        | 日期字符串、日期对象或具有 `year`、`month` 和 `day` 参数的日期对象数组。                     |
| `fc-category`                   | 事件类别的名称。                                                                           |
| `fc-display-name`               | 事件的可选显示名称。否则，将使用文件名。                                                   |

一旦打开此设置，日历将在指定的文件夹中查找应添加到自身的事件。找到后，它们将被添加 - **除非已经在日历上链接到该笔记的确切日期的事件。**

日历还将监视笔记的更改并相应地更新自身。**插件不应自动删除已创建的事件。一旦它们被添加，必须手动删除。**

#### fc-calendar

`fc-calendar` 字段用于指定事件将添加到哪个日历中。

该字段是可选的，如果没有与 `fc-date` 一起提供，插件将把事件添加到**默认日历**中。

##### 单一日历

可以将一个便签注册到一个单一的日历中，如下所示：

```
---
fc-calendar: 我的自定义日历
fc-date: 837-02-28                  # 837年第二个月的第28天。
fc-category: 事件类别1
---
```

多个日历

此外，您可以指定多个日历来创建事件，如下所示：

```md
---
fc-calendar: 
  - 我的自定义日历
  - 我的自定义日历2
fc-date:                        # 两个日历的相同日期。
  year: 837          
  month: 自定义月份   
  day: 17

**或者**

fc-date:                        # 每个日历的不同日期。
  - year: 837                   # 我的自定义日历的日期
    month: 自定义月份   
    day: 17
  - year: 92                    # 我的自定义日历2的日期
    month: 日历2的月份   
    day: 3

fc-category: 事件类别1
---
```

插件将按照指定日历的顺序分配日期。

#### 前置日期

前置日期可以通过两种方式提供 - 作为日期字符串或日期对象。

日期字符串必须按照设置中指定的格式进行格式化。

如果您需要事件重复（例如每年或每月一次），可以提供日期对象。日期对象必须提供的唯一值是日期，插件将为未提供的值重复事件。请注意，月份可以作为月份名称或月份数字（例如，2 代表二月）提供。

```
---
fc-date:        # 事件将在每年的每个月的第2天重复。
  day: 3
---

---
fc-date:        # 事件将在每年的第2个月的第3天重复。
  day: 3
  month: 2
---

---
fc-date:        # 事件将在2021年的每个月的第3天重复。
  day: 3
  year: 2021
---

---
fc-date:        # 事件将在2021年的二月的第3天重复。
  day: 3
  month: February
  year: 2021
---

```

打开 [解析笔记标题以获取日期](#parse-note-titles-for-dates) 将使此字段变为可选，如果标题中存在与 [date format](#date-format) 设置中指定的格式匹配的日期。

#### 事件显示名称

默认情况下，日历视图会根据事件文件名自动创建事件，并以文件名为标题显示。要覆盖此行为，请使用 `fc-display-name` 前置元数据字段。

给定文件 `forecast.md`，可以按如下方式覆盖事件的名称：

```
---
fc-calendar: My Custom Calendar
fc-date: 1491-14-30
fc-category: Natural Events
fc-display-name: Weather        # 日历将显示“Weather”作为标题，而不是“forecast”。
---

**早上**: 多云
**白天**: 晴朗
**晚上**: 末日风暴

```

## 插件 API

该插件具有一个 API，可用于获取您创建的日历的信息。这使您可以轻松地在 DataviewJS 中使用来自您的日历的数据！

完整的 API 可以在 [这里](./src/@types/api.d.ts) 找到。

### 访问 API

插件 API 可以在全局 window 对象上作为 `FantasyCalendarAPI` 访问。

```js
const day = FantasyCalendarAPI.getDay({ year: 2022, month: 11, day: 25 });
```

## 设置

默认日历

新打开的视图将在打开时显示指定的日历。

### 显示事件预览

与笔记相关联的事件将打开一个笔记预览（注意：需要启用核心页面预览插件）。

### 解析笔记标题以获取日期

打开此设置，允许插件解析笔记标题以获取日期，以便自动创建事件，而不仅仅是查找 `fc-date`。

### 日期格式

此设置允许您覆盖日期字符串的预期日期格式。默认日期格式是 UTC 格式的日期，`YYYY-MM-DD`。

请注意，提供的字符数不允许您指定更少的数字。插件将事件添加到**指定的确切日期**。

### 要监视的文件夹

该插件只会监视指定的文件夹以自动创建事件。此设置适用于所有日历。

### 默认配置目录

此设置允许您更改插件写入数据的目录。

从精彩的 [Fantasy-Calendar](https://app.fantasy-calendar.com) 应用程序导入一个日历。

### 日历

在这里可以创建和管理幻想日历。

## 路线图

- [ ] 在大型日历年视图中实现无限滚动
- [ ] 通过拖放笔记到某一天上创建事件
- [ ] 在日历上进行事件筛选

# 安装

插件已经提交到社区插件商店，并正在等待批准。

与此同时，可以通过 [Obsidian BRAT插件](https://github.com/TfTHacker/obsidian42-brat) 进行安装。

<!-- 从Obsidian v0.9.8开始，您可以通过以下步骤在Obsidian中激活此插件：

- 打开设置 > 第三方插件
- 确保安全模式处于关闭状态
- 点击浏览社区插件
- 搜索此插件
- 点击安装
- 安装完成后，关闭社区插件窗口并激活新安装的插件 -->

## 来自 GitHub

- 从 GitHub 存储库的 Releases 部分下载最新版本。**这不应该是插件的源代码，而是 `main.js`、`manifest.json` 和 `styles.css` 文件。**
- 将插件文件夹从 zip 文件中提取到您的 vault 的插件文件夹中：`<vault>/.obsidian/plugins/`
  - 注意：在某些机器上，`.obsidian` 文件夹可能是隐藏的。在 MacOS 上，您可以按下 `Command+Shift+Dot` 来在 Finder 中显示该文件夹。
- 重新加载 Obsidian
- 如果提示安全模式，您可以禁用安全模式并启用插件。否则，请前往设置，第三方插件，确保安全模式关闭，并从那里启用插件。

您可以按照相同的步骤来更新插件。

### 从源代码构建

安装插件后，您可以使用 `npm` 从源代码构建新的 `main.js` 和 `styles.css` 文件。

- 在终端中打开源代码目录并运行 `npm install`。
- 运行 `npm run build` 将在源代码目录内构建 `main.js` 和 `styles.css` 文件。
- 在您的存储库插件文件夹中导航到 `fantasy-calendar` 文件夹，并用新生成的文件替换 `main.js` 和 `styles.css` 文件。
- 重新加载 Obsidian 以使用新文件。这可以通过 [Obsidian的热重载插件](https://github.com/pjeby/hot-reload) 自动完成。

如果您首先设置了 `.env` 文件，您还可以使用 `npm run dev` 命令进行更简化的工作流程。

- 打开源代码目录并创建一个名为 `.env` 的文件。
- 在文件中添加以下行：

```
OUTDIR="/您的存储库/.obsidian/plugins/fantasy-calendar的绝对路径"
```

- 在源代码目录中运行 `npm run dev`。这将构建 `main.js` 和 `styles.css` 文件，并将它们放在您在 `.env` 文件中指定的文件夹中。
- `dev` 脚本将在您保存更改时自动重新构建这些文件。

# 警告

该插件没有稳定性保证，可能会导致数据丢失的错误。

请确保您有自动备份。

# TTRPG 插件

如果您正在使用 Obsidian 来运行/计划 TTRPG，您可能会发现我的其他插件很有用：

- [Obsidian Leaflet](https://github.com/valentine195/obsidian-leaflet-plugin) - 在 Obsidian.md 笔记中添加交互式地图
- [Dice Roller](https://github.com/valentine195/obsidian-dice-roller) - 为您的笔记添加一点随机性！
- [5e Statblocks](https://github.com/valentine195/obsidian-5e-statblocks/) - 在笔记中创建 5e 风格的状态块
- [Initiative Tracker](https://github.com/valentine195/obsidian-initiative-tracker) - 在 Obsidian 中跟踪 TTRPG 的先攻顺序





