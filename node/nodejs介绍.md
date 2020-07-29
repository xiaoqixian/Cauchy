---
author: lunar
date: Wed 29 Jul 2020 03:25:13 PM CST
---

### **什么是node.js**

node.js是一个基于chrome V8引擎的JavaScript**运行环境**。node.js使用一个**事件驱动、阻塞式I/O**的模型，使其轻量又高效。node.js的包管理工具npm是全球最大的开源库生态系统。

在 Node.js 里运行 JavaScript，跟在 Chrome 里运行 JavaScript 有什么不同？

二者采用的是同样的 JS 引擎。在 Node.js 里写 JS，和在前端写 JS，几乎没有不同。在写法上的区别在于：Node.js 没有浏览器、页面标签相关的 API，但是新增了一些 Node.js 相关的 API。通俗来说，对于开发者而言，在前端写 JS 是用于控制浏览器；而 Node.js 环境写 JS 可以控制整个计算机。

我们知道，JavaScript 的组成分为三个部分：

-   ECMAScript

-   DOM：标签元素相关的API

-   BOM：浏览器相关的API

ECMAScript 是 JS 的语法；DOM 和 BOM 浏览器端为 JS 提供的 API。

而 Node.js 的组成分为：

-   **ECMAScript**。ECMAScript 的所有语法在 Node 环境中都可以使用。

-   **Node 环境**提供的一些**附加 API**(包括文件、网络等相关的 API)。

Node.js内部采用chrome的V8引擎，作为JavaScript语言解释器；同时结合自行开发的libuv库，扩展了JavaScript在后端的能力（比如I/O操作，文件读写，操作数据库等）。使得JavaScript既可以在前端操作DOM，又可以在后端调用操作系统资源，是目前最简单的全栈语言。
