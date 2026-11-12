---
title: "A whiteboard for the Raptors"
date: 2026-11-02
summary: "I built a site for the 2nd/3rd grade basketball team I coach, with drills and practice plans that each live in their own small file."
---

I’m coaching a 2nd/3rd grade co-ed team with Coach Toci this season, and we needed one place for rules, the roster, the schedule, and our plans. So I built basketball.pfinn.org. It looks like a coach’s whiteboard in the school’s green and blue, and it turns into a chalkboard in dark mode.

- **Content collections** are an Astro feature. Every drill, game plan, and practice plan is its own little file. Astro turns each one into a page and builds the lists for me.
- **Data files** hold the roster and schedule. Changing a practice time means editing one line, not hunting through a page.
- **Privacy came first.** Kids appear only as a first name and last initial. No photos, no last names, no notes about players. The site also asks search engines not to list it.

## Things that tripped me up

- A page template that makes one page per item has to keep its square brackets, like `[id].astro`. When I lost the brackets, the build failed.
- Each drill has to use one of the skills from a fixed list. A typo in the skill name stopped the whole build.
- GitHub can’t upload an empty folder. I had to build the folder on my Mac with files inside, then drag the whole thing in.
- After I rolled back a bad deploy, Vercel quietly stopped putting new builds live. The fix was clicking Undo Rollback.
