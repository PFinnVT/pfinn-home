---
title: Built a private design site for Aly
date: 2026-10-30
summary: Started Aly’s Design Book at aly.pfinn.org, with invite-only logins and Google sign-in.
---

Aly loves interior design, so I’m building her a place to save ideas and get suggestions that fit her taste and our rooms. Tonight I built the frame:

- **GitHub and Vercel** again, but this time Astro runs in server mode, so each page can check who’s signed in.
- **Namecheap** points `aly.pfinn.org` at Vercel, plus five more records for the login service.
- **Clerk** handles accounts. It’s invite-only, so only people I approve can join.
- **Google Cloud** lets people sign in with their Google account.
- **Privacy and Terms** pages, because Google asks for them before it lets an app go public.

The look comes from our kitchen: painted white cabinets, the navy island, brass pulls, rattan stools, and the fretwork pattern from our dining chairs.

Things that tripped me up:

- Clerk has a practice mode (Development) and a real mode (Production). They have separate keys and separate accounts, so I had to make my account again after switching.
- Secret keys only show once. Paste them straight into Vercel.
- Clerk picked `pfinn.org` instead of `aly.pfinn.org`, and its Change domain form kept giving an error in Chrome. It worked in Safari.
- The sign-in box was blank. Chrome’s console (Cmd+Option+J) showed it was loading from the old Clerk address. Variables that start with `PUBLIC_` get baked in when the site builds, so after changing one I have to redeploy, and check that the new deployment is the live one.
- The security certificate takes a few minutes to arrive after the DNS records check out.

Next up: inviting Aly, then boards for saving photos and links.
