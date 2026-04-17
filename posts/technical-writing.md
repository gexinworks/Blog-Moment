---
title: On Writing Clear Technical Prose
date: 2026-03-10
tags: [Writing, Creative, Tutorial]
---

Code is read more often than it's written. The same is true for technical documentation — yet we treat writing as an afterthought.

## The Curse of Knowledge

The biggest barrier to clear technical writing is **knowing too much**. Once you understand a concept deeply, it's nearly impossible to remember what it felt like *not* to understand it.

> "The single biggest problem in communication is the illusion that it has taken place." — George Bernard Shaw

## Five Rules for Better Technical Writing

### 1. Lead with the "Why"

Bad: *"The `useEffect` hook accepts a callback and a dependency array."*

Good: *"When your component needs to sync with an external system — fetching data, subscribing to events — `useEffect` is the tool for the job."*

### 2. One Idea Per Paragraph

Each paragraph should make exactly **one point**. If you're covering two ideas, split them.

### 3. Use Concrete Examples

Abstract explanations are forgettable. Concrete examples stick:

- **Abstract**: "Memoization caches function results"
- **Concrete**: "Calling `fib(40)` takes 1.2 seconds. With memoization, it takes 0.001 seconds."

### 4. Active Voice Over Passive

- **Passive**: "The request is validated by the middleware"
- **Active**: "The middleware validates the request"

### 5. Edit Ruthlessly

First drafts are for *thinking*. Second drafts are for *communicating*.

```markdown
# Editing checklist
- [ ] Can I cut any words without losing meaning?
- [ ] Is every technical term defined on first use?
- [ ] Would a junior developer understand this?
- [ ] Did I include a working code example?
- [ ] Does each section have a clear purpose?
```

## The Structure Template

Every technical article should follow this skeleton:

1. **Hook** — Why should the reader care?
2. **Context** — What do they need to know first?
3. **Core content** — The meat of the article
4. **Practical example** — Show, don't tell
5. **Summary** — Reinforce the key takeaway

---

*Write for the person you were six months ago.*
