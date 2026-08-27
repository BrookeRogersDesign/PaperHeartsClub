# Paper Hearts Club — site

Live at **https://paperhearts.club** via GitHub Pages.
Repo: `github.com/BrookeRogersDesign/PaperHeartsClub` (branch `main`, served from repo root).

## Structure

Flat. Pages sits at the repo root, so every file here is public at
`paperhearts.club/<filename>`. There is no build step and no `assets/` folder —
HTML references images by bare filename (`src="Collage.png"`). Keep it that way;
moving a file into a subfolder breaks every page that points at it.

```
index.html      home — hero, collage + letter, FAQ, subscribe form, footer, stars
about.html      about
contact.html    contact
policies.html   shipping / returns / privacy
CNAME           paperhearts.club — never delete this
```

## Type

Adobe Fonts kit `ljp7fbz` (Proxima Nova + PD Americano), loaded from
`use.typekit.net`. `paperhearts.club`, `www.paperhearts.club` and
`brookerogersdesign.github.io` must all stay allow-listed in the Adobe web
project or the type silently falls back.

## Forms

- Homepage subscribe → Formspree `xpqvwjwp` (live)
- Contact page → no form. A "Send a Note" button opens `mailto:brooke@brookerogersdesign.com`
  with the subject pre-filled. `paperhearts.club` has no MX records, so a
  `@paperhearts.club` address would bounce — do not switch to one until mail is set up.

## Payments

Stripe payment link `buy.stripe.com/28EeVdaS2foxdY8480ejK01`, referenced from
every page's subscribe/join button.

## Publishing

From the project folder above this one:

```
./publish "what changed"
```

or by hand: `git add -A && git commit -m "…" && git push`.
Pages redeploys in under a minute. Hard-refresh (Cmd+Shift+R) to see it.
