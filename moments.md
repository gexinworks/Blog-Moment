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
