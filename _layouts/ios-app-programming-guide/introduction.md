#About iOS App Programming

想开发ios应用的童鞋，从这篇文章开始吧。这里会阐述ios应用的基础架构，以及应用代码和ios代码集成的方式。另外会就app设计规划阶段提供一些实用的建议，至于其他更具体的问题，也会提供链接。这篇文档不只是适用于iPhone，而是所有的iOS设备，包括iPad, iPod touch。

#概览

设计一款产品就是做各种选择。你要明白自己将面临哪些选择，这些选择对产品的实现有什么影响。

## 从点子到规划
好点子是好应用的起点，但是好点子也要合理的规划。每个App都严重依赖某些设计模式，这些模式很大程度上影响了你的编码方式。所以在开始动手编码前，花点时间研究一下iOS为我们提供的环境。这叫磨刀不误砍柴工，免得你以后因为沮丧而放弃。

相关章节 App设计基础

## UIKit是App
一个iOS应用的核心架构是建立在UIKit上的。它为你提供了各种功能的对象，包括事件处理、屏幕展示、交互等等。明白它们扮演的角色，理解怎么修改它们以定制App的默认行为，这样才能掌握快速正确的编程方法。

相关章节 App核心对象

## App在前台和后台的行为必须不同
一个iOS设备可以同时跑多个应用，但只有一个前台应用, 有它才能给用户展示用户界面，接收用户的触屏操作。其他的应用只能乖乖地呆在后台，通常它们是睡眠的，但是有时也会做一些小动作。前台和后台的切换会在某些方面影响App的行为。

相关章节 App状态和多任务

## iCloud会影响App的数据模型和UI的设计
有了iCloud，不同的iOS设备和Mac OS X设备可以共享数据。一旦你决定使用iCloud，App的文件管理方式可能会有很大的改变。因为iCloud上的文件会有多个访问者，为了防止文件被损坏，所有的操作都必须同步。UI可能也要做一定程度的改变，但不是必需的，看你是怎么展现数据的咯。

相关章节 集成iCloud

## App需要一些特殊的文件资源
为了展示内容，大多数应用都会包含图片、声音以及其他类型的资源文件。但是也有一些资源文件是所有的应用都必须包含的，因为iOS要借助它们将App展现在用户面前，或者协调App和系统的交互。所以包含这些文件能整体提升用户体验。

相关章节 App相关的资源

## App启动时要恢复上次关闭时的状态
当App启动时，必须要恢复上次关闭时的状态。通常App什么时候关闭是由系统控制的，这是程序重新启动时展现的是默认画面。UIKit会帮助你保存应用上次的状态，这样就很容易恢复了，用户体验也很一致。

相关章节 状态保存和恢复

## App行为可定制化
虽然所有应用的核心架构都是一样的，
