# Putting the chart online

The site is four self-contained files. There is nothing to build and nothing to
install — GitHub only has to serve them.

    index.html               the chart
    convoy-year.html         the great convoys' year
    convoy-crossings.html    crossings through the year
    convoy-trade.html        what each convoy is worth
    README.md
    .nojekyll

It is already set up: this folder is a git repository whose origin is
`github.com/LordAlexander-Sir/CVNchart`, published from the `main` branch at the
repository root, and it appears at

    https://lordalexander-sir.github.io/CVNchart/

## Publishing a new version

**In GitHub Desktop, make sure the current repository is `CVNchart` and not
`Book`.** This folder is a repository *inside* another one, and git will not let
the outer repository commit the inner one's files — that is what "nothing added to
commit but untracked files present" means when it names `chart/site/CVNchart/`. The
files are not lost and nothing is wrong; they simply belong to the other repository.

If CVNchart is not in the repository list: **File → Add local repository**, and
point it at this folder.

Then it is the ordinary thing: tick the changed files, write a summary, **Commit to
main**, and **Push origin**. The site updates a minute or two later.

The same from a terminal, in this folder:

    git add -A
    git commit -m "new chart"
    git push

## When the model is rebuilt

Run `publish_site.py` in the working folder. It takes the four freshly built pages,
adds the strip of links that lets each one reach the others, and writes them into
its own `site/` directory. Copy those four files over the ones here and commit.

Do not copy `settled-sphere-chart_v32.html` straight over `index.html` any more — it
would go up without the strip of links, and the other three pages would become
unreachable from it.

## Two things worth knowing

**A free account can only publish Pages from a public repository.** The repository
itself is visible to anyone who finds it, so put nothing in it you would not show.
All four pages carry `<meta name="robots" content="noindex, nofollow">`, so search
engines will not list them and nobody will stumble on the address by accident — but
it is not private and should not be treated as private. Keep the workbook, the
reference and the notes out of it; the pages alone give nothing away that a reader
of the book would not see.

**The three fonts come from Google Fonts** — IM Fell English SC, Spectral and IBM
Plex Mono. Online that is what makes the pages look right. If you would rather they
depended on nothing at all, say so and I will bake the fonts in; it adds a few
hundred kilobytes per page and makes them work offline.
