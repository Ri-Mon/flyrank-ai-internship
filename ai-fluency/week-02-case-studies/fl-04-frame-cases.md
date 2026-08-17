# FL-04 — Frame It as Cases

- **Name:** Md. Mahmudul Hasan Rimon
- **Date:** August 10, 2026

---

## Voice Card

Confident, thoughtful, plain-spoken, honest, technical, explanatory, conversational.

---

## Case Study: Tuber (Video Streaming Site)

**Repo:** https://github.com/Ri-Mon/Tuber-Video-Streaming-Site

**The problem.**
I built Tuber as one of my early API projects — the goal was learning how to connect to an API, fetch data, and get it rendering on a page. Once it was working, though, I noticed something: without any sorting, everything just sat there together — popular content and barely-watched content side by side, no way to tell them apart at a glance. Say I opened it looking for music. I'd have to scroll past a bunch of low-view videos before finding the ones actually worth watching. Real YouTube handles this by default. Mine didn't, because I hadn't built that logic yet.

**What I did.**
The API already had videos tagged by category, so category separation was straightforward — I pulled that data and built the category buttons around it. Sorting by views was harder, mostly because it was my first time really working with an API, so I intentionally picked a clean, well-organized one to learn on rather than a messy real-world one. Along the way I ran into a genuinely frustrating bug: my sort button had a tooltip showing "highest to lowest" or "lowest to highest," but the tooltip and the actual sorting logic were running on two separate variables that I hadn't connected properly. So either the tooltip would update but the sort wouldn't, or the sort would work but the tooltip wouldn't reflect it. I asked AI for help, and it gave me something that technically worked — but it was more complicated than I could actually explain if someone asked me how it worked. I didn't want to ship code I couldn't stand behind, so I went back, worked through the logic myself, and eventually built a version I actually understood.

**What came of it.**
The sorting worked the way I wanted it to. I didn't just check it once on my dev machine and call it done — I tested it on my phone, opened it in incognito mode, and ran it in a different browser, just to make sure it wasn't only working in my one specific setup. If I rebuilt this today, I'd pull from a bigger dataset, let users customize their own filter criteria instead of just views, and honestly, I'd redo the UI — it looks pretty dated next to what YouTube looks like now.

---

## Bio

I build frontend experiences that make messy information easier to navigate. My work focuses on the decisions behind the interface — from working with real data to shaping how people find and explore what matters.

## Contact / CTA

If that sounds useful, let's talk. I explain better when I can walk you through my thinking.

---

## Before / After: Generic AI Line vs. Edited Version

**Before (generic, first-pass AI draft — "what I did" beat):**
> "The API already tagged videos by category, so I pulled that data directly and built the category buttons around it. Sorting was trickier — this was my first real API project, so I deliberately picked a clean dataset to learn fetch/sort patterns without extra noise. I ran into a real bug where the sort-order tooltip and the actual sort logic weren't wired to the same state, so one would work while the other broke. I got an AI-generated fix, but it was more complex than I could actually explain or defend — so instead of shipping code I didn't understand, I worked through the logic myself until I built something I could stand behind."

**Why it didn't work:** It compressed real reasoning into punchy, ad-copy pacing — fast cause-and-effect instead of actually walking through the thinking. It technically included the same facts, but it read like it was written to sound impressive fast, not to help someone understand what actually happened. That's the opposite of "thoughtful" and "explanatory" from my voice card.

**After (edited, in my voice):**
> "The API already had videos tagged by category, so category separation was straightforward — I pulled that data and built the category buttons around it. Sorting by views was harder, mostly because it was my first time really working with an API, so I intentionally picked a clean, well-organized one to learn on rather than a messy real-world one. Along the way I ran into a genuinely frustrating bug: my sort button had a tooltip showing 'highest to lowest' or 'lowest to highest,' but the tooltip and the actual sorting logic were running on two separate variables that I hadn't connected properly. So either the tooltip would update but the sort wouldn't, or the sort would work but the tooltip wouldn't reflect it. I asked AI for help, and it gave me something that technically worked — but it was more complicated than I could actually explain if someone asked me how it worked. I didn't want to ship code I couldn't stand behind, so I went back, worked through the logic myself, and eventually built a version I actually understood."
