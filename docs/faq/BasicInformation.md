---
tags:
  - 常见问题
---

# MOD常见问题：基本信息

## 如何安装 MOD？ {: .subHeader}

简单地点击 Steam 创意工坊页面上的“**订阅**”按钮即可，这会自动下载并安装 MOD。只需要安装完毕后重启你的游戏，你安装的 MOD 就会被列在主界面的“模组”菜单中，并且可以将其启用/禁用。

## 为什么我订阅的 MOD 在 “mods” 菜单中不可见？ {: .subHeader}

如果您即使在 Steam 创意工坊上订阅了 MOD，MOD 在 mods 文件夹中也不可见，这可能是由以下原因引起的：

1. 你不拥有胎衣和胎衣+。所有 Steam 创意工坊的 MOD 都需要安装这两个 DLC 才能正常工作。

2. 游戏没有正确安装 MOD。尝试卸载该 MOD，启动游戏并且等待它开始播放开头动画/进入标题画面，然后关闭游戏，再次安装 MOD，然后再重启游戏。如果还是没用，尝试重启 Steam。

3. （仅适用于胎衣+）您的 Windows/Mac 用户名包含不属于标准英文字母表的字符。由于游戏无法正确解析这些内容，因此无法找到 mods 文件夹。为了解决此问题，您必须在计算机上创建一个名称仅包含英文字符的新用户。

## 我启用了一个 MOD，现在我的游戏崩溃了。我该怎么解决这个问题？ {: .subHeader}

您可以尝试浏览 [log.txt文件](#my-mod-or-a-mod-i-downloaded-is-causing-errors-where-is-the-logtxt-file-located) 看看有没有什么有趣的东西。然而，在绝大多数情况下，当游戏崩溃时，日志不会显示任何有用的信息。

另一种方法，你可以通过逐个禁用你的 MOD 来找到问题，直到你找到导致崩溃的确切的某个 MOD。然后，你可以将其报告给 MOD 的开发者，或者尝试自己手动修复代码。

请注意，无论何时启用或禁用 MOD，都应完全关闭并重新打开游戏（因为当您通过游戏内菜单启用/禁用 MOD 时，游戏无法正确加载资源）。

## MOD 禁用成就吗？ {: .subHeader}

**MOD 不禁用成就**，但至少需要你的存档先不开启 MOD 和控制台击杀一次妈妈（即深牢II的头目）。在挑战或者每日挑战中击杀妈妈不算。

## 我使用 MOD 需要安装所有 DLC 吗？ {: .subHeader}

要使用 MOD，你必须至少安装游戏本体（重生），第一个 DLC（胎衣），以及第二个 DLC（胎衣+）。

第三个 DLC（忏悔）并不强制要求，但因为其具有新的 MOD 特性，推荐安装。许多新的 MOD 都不与之前的胎衣+兼容。

## 重生/胎衣的 MOD 能在胎衣+/忏悔上玩吗？ {: .subHeader}

看你的 MOD 是什么，但是大部分情况下都不行。

## <span id="my-mod-or-a-mod-i-downloaded-is-causing-errors-where-is-the-logtxt-file-located">我制作的，或者我下载的 MOD 发生了错误。log.txt 文件在哪里？</span> {: .subHeader}

如果 Lua 解释器在代码中遇到错误，它会将其写入游戏的 log.txt 文件。作为玩家，您可以将此文件提供给 MOD 的开发人员；作为 MOD 开发人员，您可以使用它来查明导致错误的行。

默认情况下，该文件处于：

```
文档\My Games\Binding of Isaac Repentance\log.txt
```

打开这个文件并仔细搜索与 Lua 相关的错误。（Ctrl+F 查找单词 “error” 是一个好方法。）这通常会告诉你写错的代码的行号。

## log.txt 文件的内容什么时候会被清除？ {: .subHeader}

每次你打开游戏的时候，所有 log.txt 文件的内容都会被清除。因此，如果你在 bug 产生后需要从日志中得到信息，请确保你没有重启游戏。

## 配置文件在哪儿？（options.ini） {: .subHeader}

默认情况下，options.ini 文件位于：

```
文档\My Games\Binding of Isaac Repentance\options.ini
```

## 我可以雇佣/委托谁为我编写以撒 MOD？ {: .subHeader}

你可以雇佣或委托社区的一些成员。有关具体建议，您可以在一些以撒相关群聊中询问。