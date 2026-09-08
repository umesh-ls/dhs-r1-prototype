# Publishing the DHS R1 prototype on GitHub Pages

Everything you need is in this `publish` folder. Nothing has to be built — the files are plain HTML.

```
publish/
  index.html                          the landing page reviewers see first
  DHS-R1-Prototype.html               the prototype
  DHS-R1-Demo-Presentation.html       the walkthrough deck
  DHS-R1-Demo-Presentation.pdf        the deck as PDF
  DHS-R1-SCI52-Walkthrough.html       one case followed end to end
  DHS-R1-SCI52-Walkthrough.pdf        the same, as PDF
  DHS-Scope.pdf                       the scope document, 53 pages
  DHS-Scope.md                        the same, as markdown
  DHS-Scope-fig-numbering.png         figures the markdown refers to
  DHS-Scope-fig-verification.png
  README.md                           shown on the repo page
  .nojekyll                           stops GitHub reprocessing the files
```

Twelve files, about 9 MB in all. The two decks are the largest, at roughly 2 MB each — they carry the
official sheets as images inside the file itself, so that they read at full size and the file still
works with no internet connection. GitHub's web upload takes files far larger than this; it is only
the upload that takes a moment longer.

---

## Before you start — one thing to be clear about

**GitHub Pages on a free account is public to the whole internet**, and Google will index it unless
told not to. The `index.html` here carries a `noindex` instruction, which keeps it out of search
results — but anyone with the link can still open it, and the repository itself is public too.

What is on the page: the RSSB device and the official SCI-15 / SCI-52 / SCI-02 stationery, real office
and area names (Ludhiana, Jalandhar, Punjab, Zone-II), the names used for the demonstration logins,
and the donation approval limits.

If that is fine with the Zonal Office, carry on. If you would rather it were not open to everyone,
say so and I will prepare a version with the office names and limits replaced by neutral ones — or
we use Netlify with a password instead, which takes about the same time.

---

## Steps

### 1. Create the repository

On github.com → **New repository**

- **Name:** `dhs-r1-prototype` (this becomes part of the URL)
- **Public** — required for Pages on a free account
- Tick **Add a README file** (it will be replaced in a moment)
- **Create repository**

### 2. Upload the files

On the repository page → **Add file** → **Upload files**

Drag in everything from this `publish` folder. Two points:

- Upload the **contents** of the folder, not the folder itself — `index.html` must sit at the top
  level of the repository, or the landing page will not appear at the root URL.
- `.nojekyll` starts with a dot, so your file manager may hide it. On a Mac press
  <kbd>Cmd</kbd> + <kbd>Shift</kbd> + <kbd>.</kbd> in Finder to show hidden files. If it will not
  upload, create it on GitHub instead: **Add file → Create new file**, name it `.nojekyll`, leave it
  empty, commit.

Commit the upload. Replace the README GitHub created with the one from this folder when it asks.

### 3. Turn on Pages

**Settings** → **Pages** (left sidebar)

- **Source:** Deploy from a branch
- **Branch:** `main`, folder `/ (root)`
- **Save**

Wait two or three minutes. The page appears at:

```
https://<your-github-username>.github.io/dhs-r1-prototype/
```

The **Actions** tab shows the deployment; a green tick means it is live.

### 4. Check it before sending the link

- The landing page opens and every button works — there are three cards now, not two
- In the prototype: switch logins, open a dak, open an SCI form and use **Side by side**
- Approve something with the code `123456`, then open the **Approval Letter** and the **duly approved
  form** from the dak, and again from **Approved Records**
- Open the two decks and check the sheet pages read clearly — those are the pages that were being
  shown too small before
- Try it once on a phone — the layout should reflow to a single column with a menu button

---

## Which files changed in this revision

If the repository is already up, these are the ones to replace — the rest are unchanged:

| File | Why |
|---|---|
| `DHS-R1-Prototype.html` | approval outputs, the stamps, the letter's particulars |
| `DHS-R1-Demo-Presentation.html` · `.pdf` | 43 slides — two added on the approved form and the stamps |
| `DHS-R1-SCI52-Walkthrough.html` · `.pdf` | 20 slides — sheets now shown at full size |
| `DHS-Scope.pdf` · `.md` | the scope document — numbering, the stamps, letter verification |
| `DHS-Scope-fig-*.png` | the two figures the markdown refers to |
| `index.html` · `README.md` | wording for the above |

---

## Updating it later

Re-upload the changed file: open it in the repository → pencil icon → **Delete** → then
**Add file → Upload files** with the new version. Or simply drag the new file into the repository and
confirm the overwrite. Pages redeploys within a couple of minutes.

Because every file is self-contained, you only ever replace the one that changed.

---

## If the page does not appear

| What you see | Usually means |
|---|---|
| 404 at the root URL | `index.html` is inside a sub-folder — move it to the top level |
| The deck or prototype 404s | The filename differs from the link — names are case-sensitive on Pages |
| Styling looks stripped | `.nojekyll` is missing |
| Still the old version | Pages is cached; wait a few minutes, then reload with <kbd>Shift</kbd> + refresh |

---

## Taking it down

**Settings → Pages → Source → None** unpublishes it immediately. Deleting the repository removes it
altogether.
