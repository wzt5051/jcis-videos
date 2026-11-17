# Supporting videos — static site

Built from `D:\Langmuir投稿资料\03-Supporting Information\Videos` (22 mp4, 6.3 MB total).

## What is here
- `index.html` — the site (no external CSS/JS, works offline by double-click)
- `videos/` — the 22 movies, unchanged copies
- `posters/` — first-glance thumbnails (frame at 30% of each movie)
- `manifest.csv` — machine-readable list (id, file, kind, headline, parameters)

## How to publish (pick one)

**A. GitHub Pages — fastest, free, permanent-enough**
1. Create a public repo, e.g. `jcis-videos`.
2. Upload the *contents* of this folder to the repo root.
3. Settings → Pages → Branch `main` / root → Save.
4. URL becomes `https://<user>.github.io/jcis-videos/` (live in ~1 min).
Note: 6.3 MB is far below any GitHub limit; no LFS needed.

**B. Zenodo — recommended for a citable data DOI**
1. New upload → Upload type: *Dataset* → add all movies + `manifest.csv`.
2. Fill title/authors/description with the manuscript title; link the article DOI later.
3. Publish → you get `https://doi.org/10.5281/zenodo.XXXXXXX`, which can be cited in the
   Data availability statement. Zenodo also renders an HTML preview page per record.

**C. OSF / Figshare** — same idea; both mint DOIs.

## Where to put the link in the submission
- Cover Letter: one sentence, e.g. "Supporting videos S01–S22 are also browsable at <URL>."
- Manuscript, Data availability statement: cite the DOI if you use Zenodo.
- Do **not** replace the SI upload: Elsevier still wants the files in the submission;
  the link is a convenience for reviewers.

## Regenerating
`build_site.py` in the manuscript workspace rebuilds this folder from the SI video directory.
