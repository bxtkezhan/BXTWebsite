---
title: "简介"
date: 2018-05-30T16:16:30+08:00
draft: false

image: img/home/godot_docs/docs_logo.png
---

```
func _ready():
	$Label.text = "Hello world!"
```
<!--more-->

欢迎阅读Godot的官方文档，Godot是一款自由开放的2D、3D游戏引擎，对开发者友好，能够开发各个平台的项目，且没有使用限制。

本文将粗略的介绍Godot，让你明白应该如何开始。

### 关于Godot引擎

Godot是一款功能丰富的跨平台游戏引擎，能够通过统一的方式创建2D和3D游戏。它提供了全套的通用工具，让开发者可以把精力放在游戏主体开发上。另外，Godot的游戏可以非常方便的导出到多个常见的系统平台，例如Linux、MacOS、Windows、Android、IOS、HTML5。

Godot使用MIT开源协议，是完全自由开放的。由于没有附加的条件和费用，你可以自由将其用于商业开发，而无需开放源代码。开发团端是完全独立且由社区自发组建的，你完全可以去开发属于你自己的引擎。

为了更好的掌握这款引擎，我们建议你仔细阅读这文档，跟着教程一步步来操作。

### 关于文档

社区的人说他们会一直维护这篇文档（写作，修正，编辑，改版）。他们使用reStructuredText标记语言进行写作（KK这里使用Markdown´ ▽ ` )ﾉ）。

**注意**

> 你可以参考Github给出的文档，学习使用开放的issue去提交你的内容，这样你就可以弄一个自己母语版本的文档了，这会帮助Godot项目发展！


### 文档结构

 为了相对直观的进行描述，文档分为5个部分，每个部分都有自己的侧重：

- [饿爆他](../about) 部分主要用来做一些常识性的介绍，介绍了Godot项目，以及一些相关的协议。
- The Getting started section is the main raison d’être of this documentation, as it contains all the necessary information on using the engine to make games. It starts with the Step by step tutorial which should be the entry point for all new users.
- The Tutorials section, on the other hand, can be read as needed, in any order. It contains many feature-specific tutorials and documentations.
- The Development section is intended for advanced users and contributors to the engine development, with information on compiling the engine, developing C++ modules or editor plugins.
- The Community gives information related to contributing to the engine development and the life of its community, e.g. how to report bugs, help with the documentation, etc. It also points to various community channels like IRC and Discord and contains a list of recommended third-party tutorials outside of this documentation.
- Finally, the Class reference is the documentation of the Godot API, which is also available directly within the engine’s script editor. It is generated automatically from a file in the main source repository, therefore the generated files of the documentation are not meant to be modified. See Contribute to the Class Reference for details.

In addition to this documentation you may also want to take a look at the various Godot demo projects.

Have fun reading and making games with Godot Engine!
