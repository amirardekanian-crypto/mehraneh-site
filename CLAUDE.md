# Working notes: Mehraneh Zohourian's site

Read **`MAP.md`** first: it says where everything is. This site is Mehraneh Zohourian's (tennis and padel coach,
Mashhad). It is a separate project from Amir Ardekani's coaching site and shares no files, folders or code with it.

- **Ship straight to `main`** (Amir's way of working): GitHub Pages deploys it. Push `main` by itself.
- **Voice:** colloquial, warm Farsi, the way Mehraneh talks to a student. Short sentences, no hype. Persian numerals.
- **Only claim what she has confirmed.** Results, years and prices come from Mehraneh or Amir. No invented reviews,
  no padel results (she has played padel for 2 years; the padel side leads with her tennis record).
- **Both sports, one layout:** a change to shared HTML shows on both. Use `data-only="tennis"` / `"padel"` for
  anything that differs, and `SPORTS` for strings and media.
- **Two copies to keep in step:** `PHONE`/`WHATSAPP` and the venues list exist in both `index.html` and `form.html`.
- **Keep `CNAME`.** Deleting it takes the custom domain off the site.
- **`form.html` stays `noindex`; `index.html` is indexable.** Don't put a draft badge or `noindex` back on the home page.
- **Photos:** new pictures go in `media/` with a new filename (never overwrite a published one: browsers cache them).
  Resize to about 1000-1300 px on the long side, JPEG, under about 250 KB. Check who is in a photo before it goes up.
- **Check before pushing:** serve the folder locally (`python -m http.server`) and look at both `#tennis` and `#padel`,
  at phone width too (RTL: the photo strip starts at the right edge).
- **Python on Amir's PC is `python`** (`python3` is the Microsoft Store stub).
