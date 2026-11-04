# merlineck.github.io

Personal site and blog, built with Jekyll on GitHub Pages.

## Writing a new post

1. Create a file in `_posts/` named `YYYY-MM-DD-short-title.md`.
2. Start it with this front matter:

   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   description: "One-sentence summary (used on the blog list and LinkedIn preview cards)."
   ---
   ```

3. Write the body in Markdown below the front matter.
4. Commit and push to `master`. GitHub Pages republishes in about a minute.

Optional: after sharing on LinkedIn, add `linkedin: <post URL>` to the front matter
to show a "Join the discussion on LinkedIn" link at the bottom of the post.

Tip: name a file with a future date, or keep drafts outside `_posts/`, to avoid
publishing before you're ready.

## Site settings

Edit `_config.yml` to change the site title, description, and author name.

## Preview locally (optional)

```sh
gem install jekyll jekyll-feed jekyll-seo-tag
jekyll serve
```

Then open http://localhost:4000.
