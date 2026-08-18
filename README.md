# eliaruehle.github.io

Personal website, served as a static site by **GitHub Pages**. It's a single
hand-written `index.html` (with inline CSS) — no build step, no framework. The
design mirrors <https://ninodimontalcino.github.io/>.

## File overview

| Path                     | What it is                                                        |
| ------------------------ | ---------------------------------------------------------------- |
| `index.html`             | The whole site. Edit this to enter all your content.             |
| `portrait.png`           | Your photo (top-right). **You need to add this file.**           |
| `CV.pdf`                 | Your CV, linked by the "CV" button. **You need to add this file.** |
| `img/`                   | Thumbnails and images. `placeholder.svg` is a stand-in.          |
| `blog/`                  | Optional blog posts, one `.html` file each.                      |

## How to enter your information

Open `index.html` and look for the `<!-- COMMENT -->` markers — each section is
labeled. In order, you'll want to:

1. **Title & meta** (top of file): replace `Your Name` in `<title>` and the
   `<meta author>` / `<meta description>` tags.
2. **Portrait**: save a photo as `portrait.png` in the repo root (or change the
   `src` in the portrait `<img>` to whatever you name it).
3. **About / intro**: edit the `<h1 class="name">`, the `<h4 class="email">`,
   and the intro paragraph.
4. **Background**: each `<li class="positions">` is one role/degree. Add or
   delete rows freely.
5. **Links row**: update each `academic-link-box` with your real URLs (Google
   Scholar, GitHub, LinkedIn, Twitter, email, CV). Delete any you don't use.
6. **Fields of Interest**: edit the `<span class="box-interest">` tags.
7. **Projects / Publications**: copy a whole `<li class="li-container"> … </li>`
   block to add another entry. Each has a title link, authors (wrap your own
   name in `<b class="b-personal">`), a venue line, link buttons
   (`<a class="a-paper">`), topic tags, and a thumbnail image.
8. **Talks / Blog**: optional — fill in or delete the whole section.
9. **Footer**: update the "Last Updated" date.

### Attaching your CV

Drop a file named `CV.pdf` in the repo root. The "CV" button already points to
it. To use a different name, update the two `CV.pdf` references in the CV link
box inside `index.html`.

### Adding images / thumbnails

Put image files in `img/` and point a card's `<img src="img/yourfile.png">` at
them. `img/placeholder.svg` is used everywhere until you swap in real images.

### Changing the color / theme

Near the top of the `<style>` block there's a `:root { --accent: saddlebrown; }`
rule. Change `--accent` (and the soft/chip variants) to re-skin the entire site
in one place — e.g. `#1b3a5b` (navy) or `#14532d` (green).

### Writing a blog post

Copy `blog/example-post.html`, rename it, edit the content, then add a link to
it from the **Blog** section in `index.html`.

## Previewing locally

It's plain HTML, so just open `index.html` in a browser. For a local server
(so relative paths behave exactly like production):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publishing with GitHub Pages

Because the repo is named `eliaruehle.github.io`, GitHub Pages serves it at
<https://eliaruehle.github.io> automatically. To enable it:

1. Commit and push your changes to the `main` branch.
2. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a
   branch**, branch `main`, folder `/ (root)`, then **Save**.
3. Wait ~1 minute, then open <https://eliaruehle.github.io>.

Every push to `main` re-publishes the site.

## Credit

Design adapted from the personal site of
[Nino Scherrer](https://ninodimontalcino.github.io/).
