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

Welcome to the official documentation of Godot Engine, the free and open source community-driven 2D and 3D game engine! Behind this mouthful, you will find a powerful yet user-friendly tool that you can use to develop any kind of game, for any platform and with no usage restriction whatsoever.

This page aims at giving a broad presentation of the engine and of the contents of this documentation, so that you know where to start if you are a beginner or where to look if you need info on a specific feature.

### About Godot Engine

A game engine is a complex tool, and it is therefore difficult to present Godot in a few words. Here’s however our PR presentation, which you are free to reuse if you need a quick writeup about Godot Engine.

Godot Engine is a feature-packed, cross-platform game engine to create 2D and 3D games from a unified interface. It provides a comprehensive set of common tools, so that users can focus on making games without having to reinvent the wheel. Games can be exported in one click to a number of platforms, including the major desktop platforms (Linux, macOS, Windows) as well as mobile (Android, iOS) and web-based (HTML5) platforms.

Godot is completely free and open source under the permissive MIT license. No strings attached, no royalties, nothing. Users’ games are theirs, down to the last line of engine code. Godot’s development is fully independent and community-driven, empowering users to help shape their engine to match their expectations. It is supported by the Software Freedom Conservancy not-for-profit.

For a more in-depth view of the engine, you are encouraged to read this documentation further, especially the Step by step tutorial.

### About the documentation

This documentation is continuously written, corrected, edited and revamped by members of the Godot Engine community. It is edited via text files in the reStructuredText markup language and then compiled into a static website/offline document using the open source Sphinx and ReadTheDocs tools.

**Note**

> You can contribute to Godot’s documentation by opening issue tickets or sending patches via pull requests on its GitHub source repository, or translating it into your language on Hosted Weblate.

All the contents are under the permissive Creative Commons Attribution 3.0 (CC-BY 3.0) license, with attribution to “Juan Linietsky, Ariel Manzur and the Godot Engine community”.

### Organisation of the documentation

- This documentation is organised in five sections with an impressively unbalanced distribution of contents – but the way it is split up should be relatively intuitive:
- The General section contains this introduction as well as information about the engine, its history, its licensing, authors, etc. It also contains the Frequently asked questions.
- The Getting started section is the main raison d’être of this documentation, as it contains all the necessary information on using the engine to make games. It starts with the Step by step tutorial which should be the entry point for all new users.
- The Tutorials section, on the other hand, can be read as needed, in any order. It contains many feature-specific tutorials and documentations.
- The Development section is intended for advanced users and contributors to the engine development, with information on compiling the engine, developing C++ modules or editor plugins.
- The Community gives information related to contributing to the engine development and the life of its community, e.g. how to report bugs, help with the documentation, etc. It also points to various community channels like IRC and Discord and contains a list of recommended third-party tutorials outside of this documentation.
- Finally, the Class reference is the documentation of the Godot API, which is also available directly within the engine’s script editor. It is generated automatically from a file in the main source repository, therefore the generated files of the documentation are not meant to be modified. See Contribute to the Class Reference for details.

In addition to this documentation you may also want to take a look at the various Godot demo projects.

Have fun reading and making games with Godot Engine!