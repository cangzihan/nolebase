---
tags:
  - 知识领域/个人知识管理
  - 知识领域/个人知识管理/PKM
  - 软件/Obsidian
  - 开发/前端/VitePress
  - 项目/Nólëbase
  - 个人知识管理/知识库
status: 尚未完成
---
# Nólëbase 和我们所使用的 Obsidian 以及 VitePress 所处的困境

::: warning
⚠️ 该文档尚未完成，仍在编写中...
:::

## 前言

距离 [[Nolebase|Nólëbase]] 从建立到现在已经过去了快 2 年多的时间了，[[Nolebase|Nólëbase]] 给我和小音 @LittleSound 带来了什么？

**我没有办法给出一个答案。** 再加上小音在 [[VitePress]] 项目中有过不好的经历，她现在使用的也很少了，很多地方的用户体验设计我不清楚是否做到位了，但是我知道这里面有非常多的问题亟待解决。这很多时候和 [[Nolebase|Nólëbase]] 底层所使用的 [[Obsidian]]，[[VitePress]]，以及我目前学习到的这些「知识库方法论」息息相关。

首先，对于我自己而言，时至今日我都并没有能够很好的养成一个「能记则记」的习惯，没有日记，没有周记，知识点也并没有形成成体系的诸如 [Zettelkasten](https://zh.wikipedia.org/zh-cn/%E5%8D%A1%E7%89%87%E7%9B%92%E7%AD%86%E8%A8%98%E6%B3%95)、[PARA](https://fortelabs.com/blog/para/)，或者现在比较新奇的 [[ACCESS 组织方法论]]。
Obsidian 的绝大多数知识，往往都是在我花费大量的时间解决了一个非常困难的 debug 难题而起，因为 debug 和排错的过程中所翻阅的众多的 [Google](https://google.com) 搜索结果条目、[StackOverflow](https://stackoverflow.com) 问答，以及 [GitHub](https://github.com) Issue 数目繁多，于是我会因为觉得「如果不记点什么，也许下一次解决问题的时候就会再次遇到重新跑一次这个信息检索的流程的苦大仇深的难题」，才会因此去写下长篇大论来记述我的操作，解决问题的过程和办法。

**但，这是正确的吗？**

起初，我只是极尽全力去避免我自己成为那种我经常会去吐槽很多 [GitHub](https://github.com) 开源社区的用户的模样：

> 经常会有很多人开了一个内容也许我想去解决的问题的、全世界唯一或者唯二的人，最后 [GitHub](https://github.com) Issue 里要么是因为长时间不活动，或者一句话也不说地情况下就直接把 Issue 关闭，留下在电脑显示器面前扶着自己的额头的我，陷入不知道应该如何继续的困境。我非常厌恶这样的社区用户，我不希望自己成为那种样子。

所以就有了上文提到的，就我自己所撰写的 [[Nolebase|Nólëbase]] 的绝大部分笔记而言，它们实际上都是由 Debug 和 Troubleshooting 驱动的笔记。这导致我现在认为绝大多数我在知识库中记录的信息，实际上可以理解为是 ~~用流水账的形式记述的我在知识边界上的遭遇 ~~ 。

站在此时此刻的角度来看的话，很多时候这样的笔记是能实实在在帮到我的，这种类型的笔记也确实会存在于很多个人或者团体的知识库中。

不过笔记也好，个人知识库也好，它们之所以存在，都是为了「防止你找不到你的记忆」，然后寄希望于通过成体系的记录和建设，通过这种无形的驱动力去实现所谓的「第二大脑」来方便你自己专注于你正在做的事情，或者通过闪卡（Flashcard）搭配间隔重复来实现知识的固化，即「温故而知新」，而非关注过多的每一个知识领域的知识细节，因而避免经常遗忘等等。

不过稍微有点跑题了，我写下这篇笔记想要讨论的问题，则是我应该如何寻找到一个适合我自己的方式来更好的让我和小音记录我们的学习，工作和生活，并让 [[Nolebase|Nólëbase]] 继续发光发热。

## 回到开始

在刚开始认真制作 [[Nolebase|Nólëbase]] 最初的知识库的时候，我基本上是在漫无目的地去记录一些当时会不断重复，或者多次详细地向小音讲解和描述的知识概念，比如哪个命令行工具怎么用的，或者像是 [Nginx](https://www.nginx.com/) 或者 Systemd 又是怎么配置的等等，然而在那个时间点上，我和小音所使用的笔记和知识库管理工具其实是现在即将消亡的「印象笔记」。不过这不代表印象笔记有什么问题，反而，印象笔记和 OneNote 都是在我的认知的时间长河里一样是在 [[Notion]] 出现前制作笔记的最佳工具，我和小音也确实在里面记录了不少的详尽知识，会利用它强大的扫描 App 去扫描我们需要备忘的实体文档，也会通过比较高昂的订阅费用去实现协作和共享。

比较可惜的是，由于没有相关的资料的收集和记录[^2]，我早就已经忘记为什么要搭配上 Typora 和 [[Obsidian]] 去使用和迁移到基于 Markdown 的知识库系统，也许是因为当时刚兴起了 [[Notion]] 和 [[Obsidian]] 这样更加优秀和易于拓展，不太会被锁定在一个生态里的原因。在印象里，即便是我当时已经在 [[Notion]] 中记录了若干的笔记，实践了不少基于 [[Notion]] 的敏捷开发管理和个人任务管理，小音在我的指导下去使用之后也依然不太习惯 [[Notion]]，也许是因为当时 [[Obsidian]] 和 [[Notion]] 一样很热门，所以就有了这样的转变。

## 最初的问题

在最早通过 [[Obsidian]] 去进行知识笔记的整理的时候我就发现了一个问题，这个问题就是：[[Notion]] 即便会很卡、没有实时的光标去一起协作，会要求网络连接，但是由于 [[Notion]] 是线上的，它如果直接和 [[Obsidian]] 相比的话有很多共享和知识索引方面上的优势：

1. [[Notion]] 是一个线上服务，[[Notion]] 的分享功允许你将精致的页面和文档通过公开的链接分享给别人；
2. [[Notion]] 支持的内链也很强大，你可以通过链接到别人的知识页面和各种不同的组件来组合创造更多的知识内容；
3. [[Notion]] 创建的公开内容可以被搜索引擎所抓取，更好的分享和反馈给了全世界；

对应到 [[Obsidian]] 的话，这些问题就是：

1. [[Obsidian]] 分享很困难，在非常早期的时候我都只能通过分享不能使用双链的 Markdown 原文件给别人来实现知识共享，而在当时只有 [[Obsidian]] 官方的付费 Obsidian Publish 服务和几个开源的简陋到没有文档的前端静态页面项目才能实现部分功能，何况即便是实现了，也不能把 [[Obsidian]] 的插件带到可以预览的 HTML 里面，换句话说，这个分享和渲染之后的 HTML 的功能是残缺不全的；
2. [[Obsidian]] 无法很好的和外部的知识库进行协作，也许别人也会有建立自己的知识库，但是我只能通过找别人要别人的知识库 Markdown 原文件，或者如果对方有公开的分享的话，可以复制粘贴链接到笔记中进行引用；
3. 就像第一条说的那样，只有 [[Obsidian]] 官方的付费 Obsidian Publish 服务和几个开源项目能实现部分的功能；

回到正题，巧合的是，我在刚开始使用 [[Nolebase|Nólëbase]] 之前的一段时间在 [[Notion]] 创立了「点子库」这样专门用来收集我想要做的事情和项目的 meta 项目[^1]，当然，上面提到的这些改进点也加入到了点子库中，并且自从 2021 年就存在在那里直到现在。

![](assets/obsidian-vitepress-and-nolebase-problems-ideas-vault-01.png.png)

但这些点子并非加入到点子库之后就能够直接被实现和完成，对于「[[Obsidian]] 集成 [Hexo](https://hexo.io)/[Hugo](https://gohugo.io/)/[Gatsby](https://www.gatsbyjs.com/) 支持网页生成」这样的点子和想法在当今的 2023 年也依然不是很好解决，不过感谢小音 @LittleSound 在 2022 年底的建议和行动，借助于 [[VitePress]] 这样超快速的先进静态页面生成器，[[Nolebase|Nólëbase]] 现在能够很方便的进行分享和拓展了，当然除此以外也有很多别的工具和生态能够利用起来，你感兴趣的话，也可以去看看：

1. 基于 [Nuxt 3](https://nuxt.com/) 的文档生成器 [Docus](https://docus.dev/)
2. 现在最新最热的 [Astro](https://astro.build/)

那么，[[Obsidian]] 搭配 [[VitePress]] 解决了哪些问题呢？

## 解决了，但又没解决

[[VitePress]] 能够转换 Markdown 撰写的文档到 HTML，能自己添加 Vite 插件和 Vue 组件，这很好，已经比我当时 2021 年调研的时候别人实现的和采用的方案好很多了。

平时撰写文档的时候也可以随心所欲的在 [UnoCSS](https://unocss.dev/) 的支持下很轻松地在文档中添加各种各样的特化的组件去丰富内容，比如：

1. 混排图文时的图片自适应大小，或者图片的居中
2. 添加用于演示自己的 Code Snippet 的组件
3. 优化阅读体验（RX）

> 那哪些地方没解决呢？

[[VitePress]] 使用的 Markdown 语法拓展与 [[Obsidian]] 和 [GitHub](https://github.com) 并不相同，后两者也都不相同，这意味着：

1. 你在 [[Obsidian]] 看 [[VitePress]] 的文档会出现无法渲染和支持的情况，反之亦然，但你总不能写两份语法对吧，那样的话到了 [[VitePress]] 又不能很好的支持了；
2. 很多像是脚注，标签，导航的组件样式在 [[Obsidian]] 和 [[VitePress]] 中并不相同，你可能会在两个不同的地方看到两种 UI 实现；
3. 很多 [[Obsidian]] 的插件是基于文件系统和动态编辑的，在浏览器中使用的用 [[VitePress]] 渲染的内容在遇到某些插件的时候是不兼容的。

不过这些问题在 Obsidian Publish 中解决了吗？答案是不能。Obsidian Publish 甚至是会忽略支持插件的，这使得情况会变的更糟，用了也等于没用，对于 [[VitePress]] 而言也是解决了等于没解决。

我试图通过在 Nólëbase 中撰写大量的插件来解决这个问题，但事实是它并不好解决，借鉴于 VueUse，UnoCSS，Vite 和 Vue 文档的插件穿插在文档项目中难以维护，然后就可能会遇到你不得不为了更新脚本和插件而整个推送文档项目的情况，他们耦合在了一起，十分不方便。

## 怎么办呢

要解决这个问题很难，我必须把 [[Obsidian]] 和 [[VitePress]] 的样式和插件实现统一才行，我因此创建了 [[Nolebase 集成|Nólëbase 集成]] ，希望能够在较短的时间内解决这些问题。

[^1]:  借助于点子库这样的 Meta 项目，我会给朋友和伙伴们分享这些想法，一起探讨可行性和方案，甚至会发起项目去希望大家来参加。当然伙伴们也可以自由提交自己想做的事情和点子，虽然我现在 GitHub 中的许多 Golang 相关的开源库都是从点子库上发散而来的，但是实际上，也许是因为大家很忙碌吧，其他剩下的许多点子和想法其实到最终都没能很好的实现。只不过后来为了方便协作迁移到了 Confluence，结果更难用了。
[^2]: 这也是我一直以来感到非常惋惜的事，也就是「没能记录下很多关键时间点下的所思所想所经历」。
