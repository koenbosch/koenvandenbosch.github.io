# Koen van den Bosch — Academic Website (static, no Jekyll)

Plain HTML + CSS. No build step, no Gemfile, no theme, no Jekyll processing at all —
GitHub just serves these files exactly as they are. This eliminates every category of
problem from today (Gemfile version conflicts, broken include hooks, CSS specificity
fights, blank-date build failures).

## Files

```
index.html          — the whole site (one page)
styles.css           — all styling
.nojekyll             — tells GitHub Pages to skip Jekyll entirely and serve files as-is
files/cv.pdf         — your CV, already included
files/STILL_NEEDED.txt
images/PUT_YOUR_PHOTO_HERE.txt
```

## Step 1 — Clear out your existing repo

Your `koenbosch.github.io` repo currently has all the academicpages/Jekyll files in it
(`_config.yml`, `Gemfile`, `_includes/`, `_layouts/`, `_sass/`, `_teaching/`, etc.).
Since we're replacing the whole approach, these need to go:

1. Go to your repo on GitHub.
2. Delete every file and folder **except** don't worry about doing this file-by-file —
   the easiest way is: go to **Settings → General → Danger Zone → Delete this
   repository**, delete it, then create a brand new repository with the exact same
   name (`koenbosch.github.io`), public, no README. This guarantees a completely clean
   slate with no leftover Jekyll files that could interfere.
   *(Alternative if you'd rather not delete the repo: go into each top-level folder/file
   individually — `_config.yml`, `Gemfile`, `_includes`, `_layouts`, `_sass`,
   `_publications`, `_talks`, `_teaching`, `_pages`, `assets`, `_data`, `_posts` — and
   delete each one via the trash-can icon. More clicks, same end result.)*

## Step 2 — Upload the new files

In the (now empty) repo: **Add file → Upload files**, and drag in everything from the
zip attached to this message, keeping the folder structure (`files/`, `images/` as
subfolders). Commit.

**Important**: make sure `.nojekyll` uploads too — it's a hidden-style file (starts
with a dot), so if your file browser hides dotfiles, you may need to enable "show
hidden files" or drag the whole folder rather than picking files individually.

## Step 3 — Enable GitHub Pages

1. **Settings → Pages**.
2. **Source**: "Deploy from a branch."
3. **Branch**: `main` (or `master`, whichever your new repo uses by default) / `/ (root)`.
4. **Save**.

Since there's no Jekyll build step, this should go live within a minute — no Actions
workflow to watch, no build logs to debug.

## Step 4 — Add your photo and remaining PDFs

- `images/profile.jpg` — your headshot (square works best, it's cropped into a circle)
- `files/research_statement.pdf`
- `files/jmp.pdf`

See `files/STILL_NEEDED.txt` for exactly which links these correspond to, and how to
add a link to any of the three still-plain-text paper titles once you have a draft.

## What's on the page

- **Sidebar**: photo, name, role, affiliation, location, email, LinkedIn, and CV /
  Research Statement / Teaching buttons.
- **Work in Progress**: Job Market Paper (red tag, visible link, collapsible abstract),
  Financial Stability paper (coauthors, talks, collapsible abstract), Hiding in Plain
  Sight (gray "draft available" tag).
- **Working Papers**: The Informational Role of Sustainable Investors, linking to its
  SSRN page, with the FMA award note and collapsible abstract.
- **Policy Contributions**: the IMF Departmental Paper.
- **Teaching**: all six entries, compact — descriptions only where they add real
  information beyond the title (workshop topics, evaluation scores).

Section headers (Work in Progress / Working Papers / Policy Contributions / Teaching)
are the largest, boldest text on the page. Paper title links use the same blue as
every other link on the site — guaranteed, since it's all one shared color everywhere,
not a matched-by-eye approximation. No divider lines between papers; spacing alone
separates them.
