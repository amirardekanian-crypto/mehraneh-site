# Mehraneh Zohourian: site map

The atlas for **mehranehzohourian.com**. Everything here is hers: it shares nothing with
Amir Ardekani's coaching site (`amirardekani.com`, repo `Website`). Start here, then open the file you need.

- **Live:** https://mehranehzohourian.com (`www.` redirects to it, HTTPS enforced)
- **Repo:** `amirardekanian-crypto/mehraneh-site`, GitHub Pages from `main`, folder `/`
- **Local folder:** `GitHub/mehraneh-site` (a sibling of `Website`, not inside it)
- **Language / direction:** Farsi, RTL. Two disciplines on one layout: **tennis** and **padel**.

## Files

| File | What it is |
|---|---|
| [`index.html`](index.html) | The whole site: one page, its CSS and JS inline. Sections below. |
| [`form.html`](form.html) | Booking form. The answers are built into a WhatsApp message to her. `?s=tennis` or `?s=padel` pre-picks the sport. `noindex`. |
| [`media/`](media/) | Every photo and the one video. Listed below. |
| [`CNAME`](CNAME) | `mehranehzohourian.com`. Do not delete: Pages reads the domain from it. |
| [`robots.txt`](robots.txt), [`sitemap.xml`](sitemap.xml) | Search files. Only `index.html` is listed; the form is blocked. |
| `README.md`, `MAP.md`, `CLAUDE.md`, `_config.yml` | Notes for whoever edits the site. `_config.yml` keeps these off the public site. |

## Where each piece of content lives (all in `index.html`)

| What you want to change | Where |
|---|---|
| Title, description, page colours, hero lead, about text, chips, record lead, footer line (**per sport**) | the `SPORTS` object in the script near the end: `SPORTS.tennis` and `SPORTS.padel`, strings under `t:` |
| Which photos fill the hero and the three About shots (**per sport**) | `SPORTS.<sport>.media` (`hero`, `s0`, `s1`, `s2`) |
| The tennis/padel gate (the first screen) | the `.gate` block near the top of `<body>`; its colours are `.gh-tennis` / `.gh-padel` |
| Stats strip (13 years, rank 1, …) | `<section class="stats">`. A stat with `data-only="tennis"` or `"padel"` shows for that sport only |
| **Record cards** (rank 1, rank 3 Asia, Asian ATF, West Asia 2nd, World Tour runner-up, national team) | `#record`, one `.cred` div each. Six cards fill a 3 x 2 grid |
| The padel-only "2 years of padel" paragraph | `#record`, `<p class="lead bridge" data-only="padel">` |
| Photo strip («لحظه‌هایی از مسیرم») | `#photos`, one `<figure class="moment">` per photo (image, then caption) |
| About text | `#about` (shared paragraphs) and `aboutP1` in `SPORTS` (per sport) |
| **Classes and prices** (toman) | `#classes`. Group class is tennis only: those cards have `data-only="tennis"` |
| Courts and clubs | `#venues` (copied in `form.html` too: change both) |
| How to start / steps | `#how` |
| FAQ | `#faq` |
| Contact and footer | `#contact` and the footer |
| Phone, WhatsApp, Instagram | the constants `PHONE`, `WHATSAPP`, `INSTAGRAM` at the top of the script. `PHONE` is repeated in `form.html`: **change both** |
| Colour skins | `html[data-skin="…"]` blocks in the CSS. Tennis uses `spruce`, padel uses `court`; the rest are spare palettes |

### How the two sports work
Everything structural is shared. A bare URL shows the gate; `/#tennis` and `/#padel` go straight in.
Anything marked `data-only="tennis"` or `data-only="padel"` is hidden for the other sport, and any text
tagged `data-t="key"` is filled from `SPORTS.<sport>.t`. Add a third discipline later with one more
entry in `SPORTS`.

## Media (`media/`)

| File | Shows | Used in |
|---|---|---|
| `court.mp4`, `court-poster.jpg` | Practice on clay (video + its still) | Hero, both sports |
| `serve.jpg` | A serve on clay | About shot 1, both sports |
| `trophy.jpg` | Runner-up trophy handover, ITF World Tennis Tour Juniors | About shot 2, both sports |
| `coach.jpg` | On court next to a coach | About shot 3, both sports |
| `runnerup-tour.jpg` | Runner-up trophy, tour banner behind her | Photo strip |
| `team-iran.jpg` | In the national-team kit | Photo strip |
| `airport-team.jpg` | Welcome at the airport with the national team (portraits cropped off the top) | Photo strip |
| `practice-clay.jpg` | Training on clay | Photo strip |
| `child-medal.jpg`, `child-medal-family.jpg` | As a child, with a medal | Photo strip |

There are no padel photos yet: the padel side reuses the tennis ones. Replace them under `SPORTS.padel.media`
when she has padel pictures.

## Facts the site states (confirmed by her / Amir)

- 13 years in tennis; **2 years of padel** (the padel side leads with tennis and claims no padel results).
- Rank 1 women in Iran · rank 3 Asia, U14 · first place, ATF Asian tour · **second place, West Asia** ·
  **runner-up, ITF World Tennis Tour Juniors** (U18, girls singles) · national team at 12, 14, 16 and senior.
- "Finalist" and "runner-up" at the World Tour are **one** result, shown once.
- City: Mashhad. Padel is two players at most, so padel has private and semi-private only (no group class).
- No testimonials: she has no students' reviews yet. Do not add invented ones.

## Domain and hosting (so you can fix it later)

- **Registrar:** Namecheap, free BasicDNS (no Premium DNS needed).
- **DNS (Advanced DNS):** four `A` records on `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
  `185.199.111.153`; one `CNAME` on `www` → `amirardekanian-crypto.github.io`.
- **Pages:** repo Settings → Pages → Deploy from branch `main` / root, custom domain `mehranehzohourian.com`,
  Enforce HTTPS ticked. The `CNAME` file in this repo must stay.
- **Deploy:** every push to `main` goes live in a minute or two. Hard-refresh to bypass the browser cache.
- **Old address:** `amirardekani.com/coach-site/` was her draft link; it is gone.

## Open items

- `form.html` has `W3F_KEY = ""`, so the form only opens WhatsApp. To also get an email, make a free
  key at web3forms.com with her email and paste it there.
- Optional: add the domain to Google Search Console and submit `sitemap.xml`; point her Instagram bio here.
- Padel photos, when they exist.
