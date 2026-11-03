---
title: "Math games for Sutton"
date: 2026-11-02
summary: "Sutton’s spelling site grew into Sutton’s Games, with a landing page and math games built from the strategy sheets her class sent home."
---

Sutton’s class sent home four sheets on addition and subtraction strategies, and I wondered if they were enough to build a math game like the spelling one. They were. By the end of the night, sutton.pfinn.org had a landing page where she picks Spelling or Math, and the math side has a game for every strategy on the sheets, with two-digit and three-digit numbers.

- **Folders became web addresses.** On a plain HTML site, a folder named `math` with an `index.html` inside shows up at `/math/`. So I moved the spelling games into a `spelling` folder, added a `math` folder, and put a new landing page at the top. Same repo, same Vercel project, no new DNS records.
- **One game per strategy.** Break apart, number line, in chunks, base ten blocks, compensation, and the standard model. Each problem goes step by step the way the sheets show it, so she practices the method, not just the answer.
- **The numbers make themselves.** Unlike spelling, there’s no weekly file to update. The game creates new problems every round and follows a few rules so each strategy’s steps make sense.
- **Her stars are shared.** Spelling and math add to the same star count, and the landing page shows it. Moving the spelling games into a folder didn’t lose any stars, because the browser saves them by website address.
- **Three digits came next.** Once two digits worked, we added a “How big are the numbers?” choice, using the second set of sheets for hundreds.

## Things that tripped me up

- **Week buttons that added instead of switched.** Tapping a different week on the spelling page added it to This week instead of switching to it, so getting back took two taps. Now one tap picks just that week.
- **An invisible answer box.** On the number line, Sutton finished her jumps and tapped numbers, but nothing appeared. The buttons worked; the box was just never drawn. Base ten blocks had the same problem. The automatic test missed it because it typed answers without checking the screen, so now it checks that too.
- **An upload that didn’t take.** After the fix, Base ten blocks still looked broken. Uploading again fixed it. Next time, I’ll check the commit time next to the file on GitHub, inside the right folder, before assuming the code is wrong.
- **Files now live in folders.** Weekly spelling words go in the `spelling` folder and math changes go in the `math` folder. On GitHub, open the folder first, then Add file > Upload files.
