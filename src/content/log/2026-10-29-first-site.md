---
title: Moved my first site onto my own domain
date: 2026-10-29
summary: Took Sutton’s spelling site from Netlify to GitHub and Vercel, and gave it its own address.
---

The spelling site started as one file on Netlify. Today it moved:

- **GitHub** now holds the code and remembers every version.
- **Vercel** publishes it automatically whenever I commit a change.
- **Namecheap** points `sutton.pfinn.org` at Vercel with a CNAME record.

I split the word list into its own file, `words.js`, so weekly updates can't break the games. It now keeps every week, and Sutton can practice any mix of them.

Things that tripped me up: I looked at the wrong site when checking my first change, and the domain showed "Invalid Configuration" until I actually added the DNS record. File names matter too. `index(5).html` is not `index.html`.
