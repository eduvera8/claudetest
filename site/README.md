# Personal academic site

Plain HTML and CSS. No build step, no dependencies. Edit a file, commit, push,
and GitHub Pages republishes within about a minute.

## Files

    index.html      Homepage: bio, research interests, selected work
    research.html   Working papers, work in progress, publications
    dataviz.html    Figures and charts
    cv.html         Structured CV; links to cv.pdf
    style.css       All styling, shared by every page
    .nojekyll       Tells GitHub Pages to serve these files as-is

## Editing

Everything you need to replace is marked with `<!-- EDIT -->` comments.
Start with `index.html`.

The four pages each carry their own copy of the `<header>` nav block. If you add
or rename a page, update that block in all four files. (That duplication is the
one cost of using plain HTML instead of a template system — worth it while the
site is small.)

### Adding your photo

Put `photo.jpg` in this folder, then in `index.html` replace the
`<div class="portrait">…</div>` with:

    <img class="portrait" src="photo.jpg" alt="Eduardo Vera">

### Adding your CV PDF

Put `cv.pdf` in this folder. The link on `cv.html` already points at it.

### Colours and fonts

Both live at the top of `style.css`, in the `:root` block. The site has a light
and a dark palette; change the matching token in each of the three blocks so
the two themes stay in step.

## Local preview

No server needed — open `index.html` in a browser. To check it the way Pages
serves it:

    python3 -m http.server 8000

Then visit http://localhost:8000.
