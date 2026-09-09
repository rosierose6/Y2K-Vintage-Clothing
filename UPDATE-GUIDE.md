# Updating your site on github.com

Four jobs, in order of how much they matter. Do #1 today; the rest can wait.

Everything happens in your repo on github.com. The two moves you'll repeat:

- **To edit a file:** click the file name → click the pencil icon (top right) →
  make your change → green **Commit changes...** button → **Commit changes**
- **To add a file:** **Add file** → **Create new file** → type the name → paste →
  **Commit changes**

Your site updates about a minute after each commit. Refresh with Cmd+Shift+R
if you don't see it right away.

---

## 1. Fix the products (do this one first)

Right now all eight products on your homepage are sold, so every "View on
Depop" button leads to a dead listing. This is the only change that's
actively costing you.

Open **index.html** and click the pencil.

### 1a — the visible cards

Press **Cmd+F** and search for `<div class="grid">`.

Just below it you'll see eight blocks that each start with `<a class="item"`.
Below the last one you'll find a lone `</div>` and then
`<div class="collection-more">`.

Select everything between `<div class="grid">` and that `</div>` — all eight
blocks — and delete it. Then paste in the contents of
**new-products-block.html** (skip the grey comment at the top, it's just a
note to you).

### 1b — the hidden SEO copy

Still in index.html, scroll to the very bottom.

Your products are listed a second time there, in a block Google reads but
visitors never see. Press **Cmd+F** and search for `ItemList`.

That takes you to a block starting `<script type="application/ld+json">` and
containing `"@type": "ItemList"`. Delete from that opening `<script` line
through its closing `</script>`, and paste in the contents of
**new-seo-products-block.html**.

> **Careful:** there are two of these `ld+json` blocks. The first one says
> `"@type": "Store"` — leave that one completely alone. You only want the
> ItemList one.

Now commit.

---

## 2. Add the autumn journal post

**Add file → Create new file.**

Name it exactly: `y2k-autumn-outfit-ideas.html`

Paste in the entire contents of the file I made you, then commit.

---

## 3. Link the new post from your journal

Open **journal.html** → pencil → find the line `<div class="journal-grid">`.

Paste this directly underneath it so the new post shows up first:

```html
      <a class="jcard" href="y2k-autumn-outfit-ideas.html">
        <div class="cat">Y2K Styling</div>
        <h2>Autumn Y2K Outfits: 5 Ways to Layer Your Vintage Finds</h2>
        <p>Y2K isn't just a summer wardrobe. Five ways to carry your vintage pieces into the colder months — cardigans, tights, boots and knitwear — using things you already own.</p>
        <span class="view">Read the Post</span>
      </a>
```

Commit.

---

## 4. Replace the sitemap

Open **sitemap.xml** → pencil → select all → delete → paste in the new
sitemap.xml I made you → commit.

**Why:** your live sitemap only lists 4 pages, but your site has 9. Four of
your journal posts aren't listed at all, so Google may never have found them.

Afterwards, in Search Console, go to **Sitemaps** in the left menu and submit
`sitemap.xml` again to nudge Google.

---

## Keeping products fresh from now on

Since your pieces are one-of-one, the homepage drifts out of date fast — this
batch lasted about seven weeks before every single item had sold.

Easiest habit: whenever you've sold or listed a few things, just ask me to
refresh it. I can read your Depop shop directly and hand you an updated pair
of blocks in a couple of minutes. You never have to figure out the HTML.
