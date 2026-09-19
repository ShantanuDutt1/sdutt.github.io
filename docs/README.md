# Shantanu Dutt: portfolio site

A static website for GitHub Pages. No build step, no dependencies. Double-click `index.html` to preview it in a browser.

## What is in the package

| File | What it is |
| --- | --- |
| `index.html` | The whole site in one self-contained file: words, styling, and scripts |
| `README.md` | This guide |

Everything lives in `index.html` on purpose. There are no CSS or JavaScript files to keep in the right folders, so the styling can't break if files are moved, downloaded one at a time, or previewed on their own.

Inside `index.html`, a comment at the top is a map of the file. Search for these labels to jump around:

| Label | What it holds | Edit it when you want to... |
| --- | --- | --- |
| `STYLES` | Colors, fonts, layout | change the look. Start with section 1 (TOKENS) |
| `HERO`, `ABOUT`, `PROJECTS`, `EXPERIENCE`, `AWARDS`, `SKILLS`, `CONTACT`, `FOOTER` | The words | change wording, add a project or job, fix a link |
| `HERO ANIMATION` | The contour map script | make it faster, denser, calmer. Only edit the `CONFIG` block |
| `PAGE BEHAVIOR` | The project filter buttons | add a new filter category (rarely needed) |

`EDIT:` in a comment marks a spot that is safe to change.

## Common edits

**Add a project.** In `index.html`, find the `TEMPLATE: NEW PROJECT CARD` comment at the end of the project grid. Copy the template, paste it above the comment, and fill it in. Pick the size with `s6`, `s4`, `s3`, or `s2`, and the category with `data-cat` and `data-tags`.

**Add a job, award, or skill group.** Each has a `TEMPLATE` comment at the end of its section.

**Change colors.** Edit the variables in the `STYLES` block, section 1. The four project category colors are `--cat-research`, `--cat-mapping`, `--cat-modelling`, and `--cat-comm`.

**Change the fonts.** Swap the family names in the Google Fonts `<link>` in `index.html`, and in `--display` and `--serif` in the `STYLES` block.

**Change your email.** It appears twice in `index.html` (the CONTACT band and the FOOTER).

## Links

The full list of links, with where each came from, is in the `LINK MAP` comment at the top of `index.html`.

The project links use the exact paths from the original portfolio (`Research/...`, `GIS Analytics/...`, `General Analytics/...`, `White Papers/...`, `Resume`). Spaces are written as `%20` and the colon as `%3A`.

These paths only work if the matching files exist next to `index.html` in the same repository:

- If the path is a **file** (for example a PDF), add the extension to the link, e.g. `Research/Salamander%20Habitat%20Suitability%20Study%20(2018).pdf`.
- If the path is a **folder**, it needs an `index.html` inside it, or the link should point at the file inside it. Otherwise GitHub Pages shows a 404.

## Publishing on GitHub Pages

1. Create a repository named exactly `ShantanuDutt1.github.io` to get the address `https://shantanudutt1.github.io/`. Any other repository name publishes at `https://shantanudutt1.github.io/<repo-name>/`.
2. Put `index.html` at the top level of the repository (the root), along with your `Research`, `GIS Analytics`, `General Analytics`, `White Papers` and `Resume` files.
3. In the repository, go to Settings, then Pages, and set the source to your main branch, root folder.

## Privacy note

Do not publish your master resume PDF. It includes references with other people's contact details. Publish a version without the references at the `Resume` path.
