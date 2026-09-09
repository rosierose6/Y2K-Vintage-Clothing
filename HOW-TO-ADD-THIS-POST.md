# Adding the autumn post to your site

Three small steps. Nothing here touches your existing pages beyond one paste.

## 1. Upload the new post

Put `y2k-autumn-outfit-ideas.html` into your GitHub Pages repo, in the same
folder as `journal.html` and `index.html`.

It already matches your current post design — same header, fonts, sparkle
effect, footer — and has its own SEO title, description, social preview and
Google structured data filled in.

## 2. Add it to the journal page

Open `journal.html`, find the line that starts:

    <div class="journal-grid">

Paste this block directly underneath it, so the new post appears first:

```html
      <a class="jcard" href="y2k-autumn-outfit-ideas.html">
        <div class="cat">Y2K Styling</div>
        <h2>Autumn Y2K Outfits: 5 Ways to Layer Your Vintage Finds</h2>
        <p>Y2K isn't just a summer wardrobe. Five ways to carry your vintage pieces into the colder months — cardigans, tights, boots and knitwear — using things you already own.</p>
        <span class="view">Read the Post</span>
      </a>
```

## 3. Replace your sitemap

Swap your existing `sitemap.xml` for the one included here.

**Why this matters:** your live sitemap only listed 4 pages, but your site
actually has 9. Four of your journal posts — the fairycore guide, the vintage
sizing guide, the accessories guide and the low-rise jeans guide — weren't
listed at all, which means Google may not have found them yet. The new file
lists everything.

Once it's uploaded, you can nudge Google in Search Console: go to **Sitemaps**
in the left menu and submit `sitemap.xml` again.
