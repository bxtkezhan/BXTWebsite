---
title: "常见问题"
date: 2018-05-30T16:27:30+08:00
draft: false

image: img/home/godot_docs/docs_logo.png
---

Godot是依据开源协议MIT发布的自由开源的软件
<!--more-->

这意味着你可以自由使用它。

简单来说:

- Godot的使用没有限制
- 你可以用它来开发商业或非商业的游戏或是任何行业的软件
- 你可以修改Godot，也可以以自己的名义发布它

关于MIT协议的更多内容可以点击[这里](https://tldrlegal.com/license/mit-license)了解

Godot的Logo和ICON也采用了统一的协议，但是需要注意一些第三方库是否使用同样的协议。

关于完整的内容可以通过[COPYRIGHT.txt](https://github.com/godotengine/godot/blob/master/COPYRIGHT.txt)以及[LICENSE.txt](https://github.com/godotengine/godot/blob/master/LICENSE.txt)和[LOGO_LICENSE.txt](https://github.com/godotengine/godot/blob/master/LOGO_LICENSE.md)进行了解。

也可以参看[Godot官方的协议介绍页面](https://godotengine.org/license)。

### Godot引擎支持的平台

**开发环境：**

- Windows
- Mac OS X
- X11 (Linux, \*BSD)

**游戏运行环境：**

- Windows (and UWP)
- Mac OS X
- X11 (Linux, \*BSD)
- Android
- iOS
- Web

32位和64位的二进制文件都被支持，默认情况下为64位。

一些用户也成功在其它平台下编译完成Godot，例如ARM架构基础的Linux（Raspberry Pi），所以你也可以找到其它平台的非官方版本。

详细内容可以查看[Compiling](../../development/compiling)这一章。

### Which languages are supported in Godot?

The officially supported languages for Godot are GDScript, Visual Scripting, C# and C++. See the subcategories for each language in the scripting section.

Note that C# and Visual Scripting support is comparatively young and GDScript still has some advantages as outlined below.

Support for new languages can be added by third parties using the GDNative / NativeScript / PluginScript facilities. (See question about plugins below.)

Work is currently underway, for example, on unofficial bindings for Godot to Python and Nim.

### GDScript? Why use a custom scripting language instead of my language of choice?

The short answer is that we think the additional complexity both on your side (when first learning Godot and GDScript) as well as our side (maintenance) is worth the more integrated and seamless experience over attracting additional users with more familiar programming languages that result in a worse experience. We understand if you would rather use another language in Godot (see list of supported options above), but we strongly encourage you to try it and see the benefits for yourself.

GDScript is designed to integrate from the ground to the way Godot works, more than any other language, and is simple and easy to learn. Takes at most a day or two to get comfortable and it’s easy to see the benefits once you do. Please do the effort to learn GDScript, you will not regret it.

Godot C++ API is also efficient and easy to use (the entire Godot editor is made with this API), and an excellent tool to optimize parts of a project, but trying to use it instead of GDScript for an entire game is, in most cases, a waste of time.

Yes, for more than a decade we tried in the past integrating several VMs (and even shipped games using them), such as Python, Squirrel and Lua (in fact we authored tolua++ in the past, one of the most popular C++ binders). None of them worked as well as GDScript does now.

More information about getting comfortable with GDScript or dynamically typed languages can be found in the GDScript: An introduction to dynamic languages tutorial.

For the more technically versed, proceed to the next item.

### I don’t believe you. What are the technical reasons for the item above?

The main reasons are:

1. No good thread support in most script VMs, and Godot uses threads (Lua, Python, Squirrel, JS, AS, etc.).
- No good class extending support in most script VMs, and adapting to the way Godot works is highly inefficient (Lua, Python, JS).
- Horrible interface for binding to C++, results in large amount of code, bugs, bottlenecks and general inefficiency (Lua, Python, Squirrel, JS, etc.)
- No native vector types (vector3, matrix4, etc.), resulting in highly reduced performance when using custom types (Lua, Python, Squirrel, JS, AS, etc.).
- Garbage collector results in stalls or unnecessarily large memory usage (Lua, Python, JS, AS, etc.).
- Difficulty to integrate with the code editor for providing code completion, live editing, etc. (all of them). This is well supported by GDScript.

GDScript was designed to solve the issues above, and performs well in all the above scenarios. Please learn GDScript and enjoy a smooth integration of scripting with the game engine (yes, it’s a rare but enjoyable situation when things just work). It’s worth it, give it a try!

### I want to extend Godot. What are my options for creating plugins?

For creating Godot Editor plugins look at EditorPlugins and tool scripts.

Additional languages could be added via PluginScript or the more low-level NativeScript.

If you want to add a certain native library, your best bet is GDNative and custom C++ modules.

Also see the official blog posts on these topics:

- A look at the GDNative architecture
- GDNative is here!

You can also take a look at the GDScript implementation, the Godot modules as well as the unofficial Python support for Godot.

### Why is FBX not supported for import?

FBX SDK has a restrictive license, that is incompatible with the open license provided by Godot.

That said, Godot’s Collada support is good, please use the OpenCollada exporter for maximum compatibility if you are using Maya or 3DS Max. If you are using Blender, take a look at our own Better Collada Exporter.

Also, glTF support was added in Godot 3.0.

FBX support could still be provided by third parties as a plugin. (See Plugins question above.)

### Will [Insert closed SDK such as PhysX, GameWorks, etc.] be supported in Godot?

No, the aim of Godot is to create a complete open source engine licensed under MIT, so you have complete control over every single piece of it. Open versions of functionality or features from such SDKs may be eventually added though.

That said, because it is open source, and modular, nothing prevents you or anyone else interested into adding those libraries as a module and ship your game using them, as either open or closed source. Everything is allowed.

To see how support for your SDK of choice could still be provided, look at the Plugins question above.

### How should assets be created to handle multiple resolutions and aspect ratios?

This question pops up often and it’s probably thanks to the misunderstanding created by Apple when they originally doubled the resolution of their devices. It made people think that having the same assets in different resolutions was a good idea, so many continued towards that path. That originally worked to a point and only for Apple devices, but then several Android and Apple devices with different resolutions and aspect ratios were created, with a very wide range of sizes and DPIs.

The most common and proper way to achieve this is to, instead, use a single base resolution for the game and only handle different screen aspects. This is mostly needed for 2D, as in 3D it’s just a matter of Camera XFov or YFov.

- Choose a single base resolution for your game. Even if there are devices that go up to 2K and devices that go down to 400p, regular hardware scaling in your device will take care of this at little or no performance cost. Most common choices are either near 1080p (1920x1080) or 720p (1280x720). Keep in mind the higher the resolution, the larger your assets, the more memory they will take and the longer the time it will take for loading.
- Use the stretch options in Godot, 2D stretching with keeping aspect works best. Check the Multiple resolutions tutorial on how to achieve this.
- Determine a minimum resolution and then decide if you want your game to stretch vertically or horizontally for different aspect ratios, or whether there is a minimum one and you want black bars to appear instead. This is also explained in the previous step.
- For user interfaces, use the anchoring to determine where controls should stay and move. If UIs are more complex, consider learning about Containers.

And that’s it! Your game should work in multiple resolutions.

If there is a desire to make your game also work on ancient devices with tiny screens (less than 300 pixels in width), you can use the export option to shrink images, and set that build to be used for certain screen sizes in the App Store or Google Play.

### I have a great idea that will make Godot better. What do you think?

Your idea will most certainly be ignored. Examples of stuff that is ignored by the developers:

- Let’s do this because it will make Godot better
- Let’s do this in Godot because another game engine does it
- Let’s remove this because I think it’s not needed
- Let’s remove clutter and bloat and make Godot look nicer
- Let’s add an alternative workflow for people who prefer it

Godot developers are always willing to talk to you and listen to your feedback very openly, to an extent rarely seen in open source projects, but they will care mostly about real issues you have while using Godot, not ideas solely based on personal belief. Developers are interested in (for example):

- Your experience using the software and the problems you have (we care about this much more than ideas on how to improve it).
- The features you would like to see implemented because you need them for your project.
- The concepts that were difficult to understand in order to learn the software.
- The parts of your workflow you would like to see optimized.
- Parts where you missed clear tutorials or where the documentation wasn’t up to par.

Once one of the above points is stated, we can work together on a solution and this is where your ideas and suggestions are most valuable and welcome, they need to be in context of a real issue.

As such, please don’t feel that your ideas for Godot are unwelcome. Instead, try to reformulate them as a problem first, so developers and the community have a base ground to discuss first.

Examples of how NOT to state problems generally and vaguely are:

- Certain feature is ugly
- Certain workflow is slow
- Certain feature needs optimization
- Certain aspect of the UI looks cluttered

Associating something with an adjective will not get you much attention and developers will most likely not understand you. Instead, try to reformulate your problem as a story such as:

- I try to move objects around but always end up picking the wrong one
- I tried to make a game like Battlefield but I’m not managing to understand how to get lighting to look the same.
- I always forget which script I was editing, and it takes me too many steps to go back to it.

This will allow you to convey what you are thinking much better and set a common ground for discussion. Please try your best to state your problems as stories to the developers and the community, before discussing any idea. Be specific and concrete.

Bonus points for bringing screenshots, concrete numbers, test cases or example projects (if applicable).

### How can I support Godot development or contribute?

See Ways to contribute.

### Who is working on Godot? How can I contact you?

See the corresponding page on the Godot website.
