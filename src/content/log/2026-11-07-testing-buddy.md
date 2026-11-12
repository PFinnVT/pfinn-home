---
title: "Testing Buddy, and my first database"
date: 2026-11-07
summary: "I added a digital pet to Sutton’s games that earns presents for right answers, and it saves to a real database."
---

Sutton likes the spelling and math games, but she loves taking care of things. So I built Testing Buddy: she picks a buddy, names it, and earns presents (hats, toys, snacks, wall colors) by answering questions. Each turn flips a coin between math and spelling and borrows a real game from the site, so it always uses this week’s words.

- **A database** keeps each buddy safe in one place. Her iPad keeps a copy, but the database has the real one, so nothing is lost if the iPad is.
- **Save codes** (three silly words and a number) bring a buddy back on any device. No names, emails, or logins.
- **Server functions** are small bits of code that run on Vercel, not in the browser. They’re the only part allowed to talk to the database.
- **Fair counting** took real thought. Anything she gets on her own counts, even after wrong tries. If the game showed her the answer, it doesn’t.

## Things that tripped me up

- When connecting Neon in Vercel, typing a custom prefix gave the database setting a predictable name. Without it, the name was a guess.
- Settings like passwords only take effect after a new deploy. I changed one and wondered why nothing happened.
- An app saved to an iPad’s Home Screen keeps its own storage, separate from Safari. I had to set her buddy up from the icon she actually taps.
