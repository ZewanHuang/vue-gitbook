# 前言

## 前端和后端

用一个例子介绍一下前后端。假设现在访问教务系统，浏览器展示登录界面，我们输入学号和密码，点击登录，账号密码正确即可进入。这个过程都经历了什么呢？

首先，初始访问时，网页端会查询本地浏览器是否存有登录信息缓存，如果在不久前登录过，会记录用户信息，则这次访问将直接展示网页内容，无需登录。如果查无用户信息，或登录信息过期失效，则网页端跳转登录路由，显示登录界面。输入学号密码，点击登录按钮，此时网页端会向服务器发送登录请求，由服务器端查询数据库，验证账号密码是否正确，将结果返回网页端。网页端收到正确信号后，跳转至教务系统网页，收到错误信号则提示账号或密码错误。

这个访问的例子，我从前后端的角度解释，因此未提及DNS解析等其它的内容。在上面的描述中，网页端和服务器端可以理解为前端和后端，不难看出它们各自负责的任务：

* **前端：与浏览器联系，负责渲染页面内容，跳转路由，存取浏览器缓存，与后端（服务器端）交互**
* **后端：负责存取数据库信息，处理复杂数据，响应前端的请求**

## 关于 Vue

了解了前后端，再来说一说本教程讲的 Vue。

[Vue](https://vuejs.org/) 是编写前端项目的一个框架，官网的介绍如下：

> *Vue (读音 /vjuː/，类似于 view) 是一套用于构建用户界面的渐进式框架。与其它大型框架不同的是，Vue 被设计为可以自底向上逐层应用。Vue 的核心库只关注视图层，不仅易于上手，还便于与第三方库或既有项目整合。另一方面，当与现代化的工具链以及各种支持类库结合使用时，Vue 也完全能够为复杂的单页应用提供驱动。*

初学者不需要刻意理解这个官方解释，只需要知道，我们将借助 [Vue CLI](https://cli.vuejs.org/) 脚手架来搭建 Vue 项目框架，从而编写前端项目，完成在前面所讲述的前端任务。

## 关于本教程

在本教程中，你能学到或不能学到：

| Skill | Able/Unable |
| :-: | :-: |
| Vue 框架的基本介绍 | ✅ |
| Vue 开发的基础能力 | ✅ |
| 可以用来点睛的前端技巧 | ✅ |
| 最基础的 HTML/CSS/JS 代码 | ❌ |

**与其它网上教程不同的是，本作品尽可能手把手演示项目的创建和基本介绍，达到快速入门的效果。同时，在开发中我所用到的一些奇巧的插件或技巧，都会在这里记录。**

## License

本作品采用 [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) 进行许可。