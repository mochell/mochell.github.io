# mochell.github.io — Jekyll site

This repository uses the **Minimal Mistakes** Jekyll theme (the same theme as
[willychap.github.io](https://willychap.github.io)), deployed via GitHub Pages.

---

## Deployment (one-time setup)

### 1. Push these files to your GitHub repository

Copy all files from this folder into your `mochell.github.io` repository root,
replacing any existing `index.html` or other files.

Your repository should look like this:

```
mochell.github.io/
├── _config.yml
├── _data/
│   └── navigation.yml
├── _pages/
│   ├── research.md
│   ├── publications.md
│   └── talks.md
├── assets/
│   └── css/
│       └── main.scss
├── index.md
├── Gemfile
└── README.md
```

> **Keep your existing `/pics/` folder** — all image and CV links point to
> `https://mochell.github.io/pics/...` which will still work.

### 2. Enable GitHub Pages

In your repository on GitHub:
- Go to **Settings → Pages**
- Under *Source*, select **Deploy from a branch**
- Choose **main** (or **master**) branch, `/ (root)` folder
- Click **Save**

GitHub Pages will build the Jekyll site automatically. It takes ~1 minute.

---

## Editing content

All content is plain Markdown. No HTML needed.

| File | What it controls |
|------|-----------------|
| `_config.yml` | Site title, your name, bio, sidebar links |
| `index.md` | Home/About page |
| `_pages/research.md` | Research projects page |
| `_pages/publications.md` | Publications list |
| `_pages/talks.md` | Talks & presentations |
| `_data/navigation.yml` | Top navigation links |

### Adding a new page

1. Create `_pages/newpage.md`
2. Add this front matter at the top:
   ```yaml
   ---
   layout: single
   title: "My New Page"
   author_profile: true
   permalink: /newpage/
   ---
   ```
3. Add it to `_data/navigation.yml`:
   ```yaml
   - title: "New Page"
     url: /newpage/
   ```

### Changing your photo

Update the `avatar` line in `_config.yml`:
```yaml
author:
  avatar: "https://mochell.github.io/pics/YOUR_PHOTO.jpg"
```

Or place a photo in `assets/images/` and reference it as `/assets/images/photo.jpg`.

### Changing the skin color

Edit `_config.yml`:
```yaml
minimal_mistakes_skin: "default"
# options: "default", "air", "aqua", "contrast", "dark", "dirt", "mint", "plum", "sunrise"
```

---

## Preview locally (optional)

```bash
gem install bundler
bundle install
bundle exec jekyll serve
# → open http://localhost:4000
```
