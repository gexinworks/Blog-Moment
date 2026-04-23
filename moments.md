---
date: 2026-04-23 22:34
mood: 💭
tags: [Thoughts]
---
今天在客户现场交流，越来越觉得现在的信息系统应该是给Agent用的，如今钉钉、飞书、微信、Qoder、QoderWork，都有了Cli，争相变为Agent的工具，并且这个现象在发散，我想所有的系统都应该提供Cli，例如OA Cli、高德Cli、支付宝Cli(当然现在有API就能够快速封装Cli)等，变成Agent的工具，然后有一个超级Agent入口，一个超级Agent就能调用所有的常用工具，告诉它：我到公司了，帮我打个卡；明天8点要开故障复盘会，定个会议上；公司的卫生纸快用完了，采购一些；它应该秒懂这些信息并且执行落地。那么如果要实现这样的场景，应该如何做呢？


---
date: 2026-04-23 21:41
mood: 💭
tags: [Thoughts]
---
今天开了区域的MaaS战役会，终于不那么焦虑了，也知道大致要怎么做了；上班挺好的，越来越觉得离职去字节是个没有想清楚的事情，也觉得在字节裸辞是一个没想清楚的事情，没有想到闲下来会很无聊，不知道做什么，真的为退休生活做准备的话，应该是知道闲下来做什么、保持较低的物欲、持续保持健康的身体，如果能够做到这几点，那就随时可以闲下来了。

---
date: 2026-04-22 22:05
mood: 💭
tags: [Thoughts, Work]
---
今天有些焦虑，不知道Token运营应该怎么做了，事实上也不知道对于政企事业部来说做token运营是否是一条正确的路。

---
date: 2026-04-20 23:10
mood: 📚
tags: [Thoughts, Work]
---
回想了一下今天的KO会议，喊口号的环节还挺老登的，想说其实可以取消这个环节，可是政企事业部在会议上的存在感也仅仅就是会前采访、喊口号、1号位发言，哈哈哈，存在感好低


---
date: 2026-04-17 09:30
mood: 💡
tags: [CSS, TIL]
---
刚发现 CSS `@starting-style` 可以给 `display: none` 到 `display: block` 的切换添加过渡动画。再也不需要 JS hack 了！

---
date: 2026-04-16 21:15
mood: 📚
tags: [Reading, Systems]
---
读完了 *Designing Data-Intensive Applications*，关于分布式事务的那章刷新了我的认知。Two-phase commit 的问题远比我想象的多。

推荐给所有做后端的同学。

---
date: 2026-04-15 14:20
mood: 🤝
tags: [SQL, Work]
---
今天 pair programming 的时候，同事用一个 **递归 CTE** 解决了树形结构查询，SQL 写得太漂亮了。有时候数据库比应用层更适合处理递归。

---
date: 2026-04-14 11:00
mood: 🦀
tags: [Rust]
---
Rust 的 `?` 操作符让错误处理变得如此优雅。从 Go 的 `if err != nil` 切过来，感觉呼吸都顺畅了。

---
date: 2026-04-13 16:45
mood: 💭
tags: [Engineering, Thoughts]
---
一个关于代码审查的想法：**好的 PR 描述比好的代码更重要。** 代码可以重构，但如果 reviewer 不理解你的意图，再好的实现也会被误解。

---
date: 2026-04-12 08:30
mood: 🏃
tags: [JavaScript, Debug]
---
早起跑步的时候想明白了一个 bug 的根因 —— 竟然是时区问题。`new Date()` 在不同环境下的行为差异真的是个经典坑。

---
date: 2026-04-10 20:00
mood: ⚡
tags: [Tools, JavaScript]
---
试用了 Bun 作为 Node.js 的替代品跑测试套件，速度提升了 **3.8 倍**。虽然生态还不够成熟，但性能确实惊艳。

---
date: 2026-04-08 13:10
mood: 📝
tags: [Quotes]
---
"Make it work, make it right, make it fast." —— Kent Beck

每次想过早优化的时候，都要提醒自己这句话。
