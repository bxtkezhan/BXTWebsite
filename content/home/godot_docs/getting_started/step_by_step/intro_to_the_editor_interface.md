---
title: "介绍Godot Editor"
date: 2018-06-04T14:26:56+08:00
draft: false

image: img/home/godot_docs/docs_logo.png
---

This tutorial will run you through Godot’s interface. We’re going to look at the Project Manager, docks, workspaces and everything you need to know to get started with the engine.
<!--more-->

### Project manager

When you launch Godot, the first window you’ll see is the Project Manager. It lets you create, remove, import or play game projects.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_01.png)

n the top-right corner you’ll find a drop-down menu to change the editor’s language.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_02.png)

From the `Templates` tab you can download open source project templates and demos to help you get started faster.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_03.png)

### Create or import a project

To create a new project, click the `New Project` button on the right. Give it a name and choose an empty folder on your computer to save it.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_04.png)

Click the Browse button to open Godot’s file browser and pick a location or type the folder’s path in the Project Path field.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_05.png)

When you see the green tick on the right, it means the engine detects an empty folder and you may click `Create`. Godot will create the project for you and open it in the editor.

The next time you’ll open Godot, you’ll see your new project in the list. Double click on it to open it in the editor.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_06.png)

You can import existing projects in a similar way, using the Import button. Locate the folder that contains the project or the `project.godot` file to import and edit it.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_08.png)

When the folder path is correct you’ll see a green checkmark.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_project_manager_09.png)

### Your first look at Godot’s editor

Welcome to Godot! With your project open you should see the editor’s interface with the 3d viewport active. You can change the current workspace at the top of the interface. Click on 2d to switch to the 2d workspace.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_01.png)

Now you should see this interface, with empty docks on the right side.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_interface_overview.png)

At the top, from left to right, you can see the **main menus**, the **workspaces**, and the **playtest buttons**.

On the left side you have the **FileSystem dock**, where you’ll manage your project files and assets.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_dock_filesystem.png)

On the right side you’ll find the **Scene dock** that lists the active scene’s content and the **Inspector** in the bottom right corner.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_dock_inspector.png)

In the center you have the **Toolbar** at the top, where you’ll find tools to move, scale or lock your scene’s objects. It changes as you jump to different workspaces.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_02_toolbar.png)

The **Bottom Panel** is the host for the debug console, the animation editor, the audio mixer… They are wide and can take precious space. That’s why they’re folded by default.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_03_animation_player.png)

### The workspaces

You can see four workspace buttons at the top: 2D, 3D, Script and AssetLib.

You’ll use the **2D workspace** for all types of games. On top of 2D games that is where you’ll build your interfaces. Press F1 to access it. 

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_04_2d_workspace.png)

In the **3D workspace**, you can work with meshes, lights, and design levels for 3D games. Press F2 to access it.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_05_3d_workspace.png)

Notice the text [perspective] under the toolbar, it is a button that opens a list of options related to the 3D viewport.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_06_3d_workspace.png)

The **Script** workspace is a complete code editor with a debugger, rich auto-completion, and built-in code reference. Press F3 to access it, and F4 to search the reference.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_06_script_workspace_expanded.png)

Finally the **AssetLib** is a library of Free add-ons, scripts and assets to use in your projects.

### Modify the interface

Godot’s interface lives in a single window. You cannot split it across multiple screens although you can work with an external code editor like Atom or Visual Studio for instance.

### Move and resize docks

Click and drag on the edge of any dock or panel to resize it horizontally or vertically.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_07.png)

Click the three-dotted icon at the top of any dock to change its location.

![](http://docs.godotengine.org/en/3.0/_images/editor_ui_intro_editor_08.png)

Go to the `Editor` menu and `Editor Settings` to fine-tune the look and feel of the editor.
