# Rähle Website — Setup Guide

This folder is your whole website: `index.html`, the `images/` folder, `content.json`
(all the editable text and photo paths), and an `admin/` folder that gives you a
simple editing panel — no code required after setup.

You only need to do this setup once. After that, editing text or swapping photos
takes about 30 seconds through a web form.

---

## Step 1 — Put this folder on GitHub

1. Go to [github.com](https://github.com) and create a free account if you don't have one.
2. Create a new repository (e.g. `rahle-website`). Keep it **Public** or **Private** — either works.
3. Upload every file in this folder to that repository, keeping the same structure
   (`index.html`, `content.json`, `admin/`, `images/` all at the top level — don't
   nest them inside another folder). The easiest way: on the repo page, click
   **"Add file" → "Upload files"** and drag everything in.

## Step 2 — Connect it to Netlify (free hosting)

1. Go to [netlify.com](https://www.netlify.com) and sign up (you can sign up with
   your GitHub account, which makes the next step automatic).
2. Click **"Add new site" → "Import an existing project"** and pick the
   `rahle-website` repo you just created.
3. Leave the build settings empty (no build command, publish directory `/`) and
   click **Deploy**. In under a minute you'll get a live URL like
   `random-name-123.netlify.app` — that's your site, live on the internet.

## Step 3 — Turn on the editing panel (Netlify Identity + Git Gateway)

1. In your new Netlify site, go to **Site configuration → Identity** and click
   **Enable Identity**.
2. Under Identity settings, set **Registration preference** to **Invite only**
   (so random people can't sign up and edit your site).
3. Still under Identity, go to **Services** and enable **Git Gateway**. This lets
   the editing panel save changes back to GitHub for you, automatically.
4. Go to **Identity → Invite users**, enter your own email, and accept the
   invite email that arrives (it'll ask you to set a password).

## Step 4 — Connect your domain

1. In Netlify, go to **Domain settings → Add a domain** and enter
   `www.rahlecars.com`.
2. Netlify will show you DNS records to add. Go to wherever you bought the
   domain (GoDaddy, Namecheap, etc.), open its DNS settings, and add the
   records Netlify gives you. This can take a few hours to fully propagate.

## Step 5 — Edit your site

Once steps 1–4 are done, go to `www.rahlecars.com/admin` (or your temporary
`.netlify.app/admin` URL before the domain connects), log in with the account
from Step 3, and you'll see a form with every piece of text and every photo on
the site. Change anything, click **Publish**, and the live site updates in
under a minute — no need to come back here for text or photo changes.

---

### What you can edit yourself
- All headlines, paragraphs, and captions
- All 8 photos (hero, the two "moment" photos, the badge detail, engine,
  chassis, parts, and the configurator photo)
- The 5 configurator color names
- The spec numbers (weight, chassis, engine options, etc.)

### What still needs a developer (me, or someone else)
- Layout or design changes (colors, fonts, section order)
- New sections or features (e.g. a second car model, real payment processing
  for the quote form)
- The quote form currently just displays a confirmation on-screen — connecting
  it to actually email you submissions needs a small backend (Formspree,
  Netlify Forms, etc.)
