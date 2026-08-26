# How to put the new posts on your site

Uploading through github.com in a browser. Should take about ten minutes.

**Before you start:** download all four files from the chat to somewhere you'll
find them again — your Desktop is fine. Don't leave them in Claude's folder,
it empties itself.

- `vintage-sizing-guide.html`
- `y2k-accessories-guide.html`
- `sitemap.xml`
- (this file, for reference)

---

## Step 1 — Open your repository

Go to **github.com** and sign in, then open the repository that holds your
website. It's the one containing `index.html` and `journal.html`.

If you're not sure which one it is: click your profile picture (top right) →
**Your repositories**. The site repo is usually named `y2kvintageclothing.com`
or something ending in `.github.io`.

**Check you're on the right branch.** Near the top left of the file list there's
a button showing a branch name — usually `main`. Whatever it says, remember it.
Everything below needs to happen on that same branch.

---

## Step 2 — Upload the two new posts

1. Make sure you're looking at the **top level** of the repo — the same list
   where you can see `index.html` and `journal.html`. Not inside a subfolder.
2. Click the **Add file** button (top right of the file list) → **Upload files**.
3. Drag `vintage-sizing-guide.html` and `y2k-accessories-guide.html` onto the
   page. You can do both at once.
4. Scroll down. In the **Commit changes** box, type something like
   `Add two new journal posts`.
5. Make sure **Commit directly to the `main` branch** is selected.
6. Click **Commit changes**.

⚠️ **The most common mistake:** uploading into a subfolder. If your new files
end up next to `index.html`, you're right. If they end up inside a folder,
the URLs won't work.

---

## Step 3 — Replace the sitemap

1. In the file list, click on **`sitemap.xml`** to open it.
2. Click the **pencil icon** (top right of the file contents) to edit.
3. Select everything in the box and delete it — `Cmd+A` then `Delete`.
4. Open the new `sitemap.xml` from your Desktop in TextEdit, select all,
   copy, and paste it into the GitHub editor.
5. Scroll down, type a message like `Update sitemap`, click **Commit changes**.

---

## Step 4 — Add the posts to your journal page

This one's an edit rather than an upload, because your journal cards use styling
I can't see from outside.

1. Click **`journal.html`** in the file list, then the **pencil icon**.
2. Find the block of code for the first post card — search for
   `y2k-low-rise-jeans-guide` and you'll land on it. The card starts a line or
   two above that, with something like `<a class="...` and ends with a `</a>`.
3. **Select that whole card and copy it.** Paste two copies directly above it.
4. In the first copy, change three things:
   - the link → `y2k-low-rise-jeans-guide.html` becomes `vintage-sizing-guide.html`
   - the title → **Vintage Sizing, Decoded**
   - the description → *Why a 2002 medium fits like today's XS, how to read flat
     measurements, and the two-minute habit that means you never guess at a
     vintage label again.*
   - the little category label → change `Y2K styling` to **Buying vintage**
5. In the second copy, change the same three things:
   - the link → `y2k-accessories-guide.html`
   - the title → **Y2K Accessories: Butterfly Clips, Chokers &amp; Tiny Bags**
   - the description → *The little things that finish a Y2K outfit — what to hunt
     for secondhand, how to spot the real thing in a thrift bin, and how to wear
     it now without tipping into costume.*
   - leave the category as `Y2K styling`
6. Commit with a message like `Add new posts to journal`.

> **Easier alternative:** open `journal.html` on GitHub, click the **Raw**
> button, select all, copy, and paste the whole thing into our chat. I'll send
> back a finished file you can paste straight in — no hunting through code.

---

## Step 5 — Wait, then check

GitHub Pages takes **1–3 minutes** to rebuild. Then visit:

- https://www.y2kvintageclothing.com/vintage-sizing-guide.html
- https://www.y2kvintageclothing.com/y2k-accessories-guide.html
- https://www.y2kvintageclothing.com/journal.html

If a page shows 404, give it another couple of minutes and hard-refresh with
`Cmd+Shift+R`.

---

## If it still doesn't work

**Pages show 404 after five minutes.** The files probably went into a subfolder.
Go back to the repo — if you don't see them next to `index.html`, that's the
problem. Click into the file, use the **⋯** menu → **Delete file**, and re-upload
from the top level.

**Everything committed but the site looks identical.** Click the **Actions** tab
at the top of your repo. If the most recent run has a red ✗, the build failed —
click it and paste the error into our chat.

**Wrong branch.** If your repo has a `gh-pages` branch, that's the one Pages
publishes from, not `main`. Check **Settings** → **Pages** to see which branch
it's set to, and make sure your uploads went there.

---

## Last thing

Once this is live, tell me and I'll re-run the SEO check to confirm both pages
are up, the sitemap is valid, and the journal links work. Then submit the new
sitemap in Search Console so Google picks the posts up faster:
**Search Console → Sitemaps → enter `sitemap.xml` → Submit.**
