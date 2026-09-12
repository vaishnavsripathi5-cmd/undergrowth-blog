# Undergrowth — wildlife field journal

A static blog (built with Eleventy) styled in the dark/amber "documentary" theme,
with a Decap CMS admin panel so you can write and publish new entries from a
simple form instead of editing code.

## What's in here

- `src/index.njk` — homepage, lists all posts automatically (newest first)
- `src/posts/*.md` — your blog posts (currently 3 sample entries — delete or keep as templates)
- `src/_includes/` — the page templates (base layout + single post layout)
- `src/css/style.css` — the design
- `src/admin/` — the Decap CMS write-a-post form

## One-time setup (about 15 minutes)

**1. Put this project on GitHub**
Create a new repository on GitHub and push this folder to it (drag-and-drop
upload works fine too if you're not familiar with git commands).

**2. Connect it to Netlify**
- Go to app.netlify.com → "Add new site" → "Import an existing project"
- Pick your GitHub repo
- Build command and publish directory are already set in `netlify.toml`,
  so you can just click Deploy

**3. Turn on Identity**
- In your new Netlify site, go to **Site configuration → Identity → Enable Identity**
- Under Registration, set it to **Invite only** (so random people can't sign up
  and post to your blog)

**4. Turn on Git Gateway**
- Still under Identity settings, scroll to **Services → Git Gateway → Enable Git Gateway**
  (this is what lets the CMS commit new posts to your GitHub repo on your behalf)

**5. Invite yourself**
- Identity tab → **Invite users** → enter your own email
- Check your inbox, click the invite link, set a password

## Writing a post from now on

1. Go to `https://your-site-name.netlify.app/admin/`
2. Log in with the password you just set
3. Click **New Journal Entries**
4. Fill in the title, date, location, a short excerpt, an optional cover photo, and the story
5. Click **Publish**

That's it — Decap CMS commits a new file to your repo, Netlify rebuilds the
site automatically, and your new entry appears on the homepage within about a
minute. No code editing required after today.

## Working on it locally (optional)

```
npm install
npm run serve
```

This runs the site on your own computer at `http://localhost:8080` so you can
preview changes before pushing them.
