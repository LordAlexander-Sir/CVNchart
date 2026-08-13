# Putting the chart online

The chart is one self-contained file. There is nothing to build and nothing to
install — GitHub only has to serve it.

## The short way, entirely in the browser (about three minutes)

1. Go to **github.com/new**. Name the repository something like
   `settled-sphere`. Leave it **Public** (see the note at the bottom). Do not tick
   "Add a README" — you are about to upload one.
2. On the empty repository's page, click **uploading an existing file**.
3. Drag in the three files from this folder: **`index.html`**, **`README.md`** and
   **`.nojekyll`**. If your file manager hides dotfiles, `.nojekyll` can be skipped —
   it is only insurance.
4. Click **Commit changes**.
5. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy
   from a branch**, Branch to **main** and folder to **/ (root)**. Click **Save**.
6. Wait a minute or two. The address appears at the top of that same page:

       https://<your-username>.github.io/settled-sphere/

That is the chart, live, on any phone, tablet or desktop.

## The git way, if you would rather

From this folder, with `<you>` replaced by your GitHub username:

    git init
    git add index.html README.md .nojekyll
    git commit -m "Chart of the Settled Sphere"
    git branch -M main
    git remote add origin https://github.com/<you>/settled-sphere.git
    git push -u origin main

Then do step 5 above. Afterwards, publishing a new version of the chart is:

    git add index.html && git commit -m "new chart" && git push

## When you rebuild the chart

Copy the new `settled-sphere-chart_v32.html` over `index.html` in this folder and
upload it again — GitHub's upload page will replace the old one. Nothing else about
the repository needs to change.

## Two things worth knowing

**A free account can only publish Pages from a public repository.** The repository
itself will be visible to anyone who finds it, so put nothing in it you would not
show. The chart already carries `<meta name="robots" content="noindex, nofollow">`,
so search engines will not list it, and nobody will stumble on the address by
accident — but it is not private, and it should not be treated as private. Keep the
workbook, the reference and the notes out of it; the chart alone gives nothing away
that a reader of the book would not see.

**The three fonts come from Google Fonts** — IM Fell English SC, Spectral and IBM
Plex Mono. Online that is what makes the chart look like a chart. If you would rather
it depended on nothing at all, say so and I will bake the fonts into the file; it
adds a few hundred kilobytes and makes it work offline.
