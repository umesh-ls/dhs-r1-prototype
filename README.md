# DHS — Dak Handling System · R1 prototype

A working prototype of the topic-driven system for official correspondence, approvals and records
across the Zonal Offices.

**It is not a live system.** It runs entirely in the browser, holds no data, stores nothing, and
sends nothing anywhere. Reloading the page resets it.

---

## Open it

| | |
|---|---|
| **The prototype** | [`DHS-R1-Prototype.html`](DHS-R1-Prototype.html) |
| **Walkthrough deck** | [`DHS-R1-Demo-Presentation.html`](DHS-R1-Demo-Presentation.html) |
| **Deck as PDF** | [`DHS-R1-Demo-Presentation.pdf`](DHS-R1-Demo-Presentation.pdf) |
| **One case, step by step** | [`DHS-R1-SCI52-Walkthrough.html`](DHS-R1-SCI52-Walkthrough.html) &middot; [PDF](DHS-R1-SCI52-Walkthrough.pdf) |
| **The scope, in full** | [`DHS-Scope.pdf`](DHS-Scope.pdf) &middot; [markdown](DHS-Scope.md) |

The scope document is the one to comment on. It is a single document in three parts &mdash; the
narrative, the register of 304 requirements, and eleven annexures &mdash; and it supersedes the four
that preceded it. Every requirement carries a mark saying whether this prototype demonstrates it.

Everything is a single self-contained file — it works offline. Download the file and open it in a
browser if you'd rather not use the hosted page.

---

## Signing in

There is no password. Choose a login from the dropdown at the top of the sidebar; the screen changes
to what that person would actually see.

Where an approval asks for a one-time code, use **`123456`**.

| Login | Who | What they can do |
|---|---|---|
| Secretary — Ludhiana-I | Sh. Balwinder Kakkar | Raises dak for the Satsang Place and signs it |
| Office Staff — Ludhiana-I | Sh. Ramesh Chander | Drafts and puts up; cannot approve |
| Care Taker — Chaunta | Sh. Gurdev Singh | A Sub Centre, read-only |
| Area Secretary — Ludhiana | Sh. Gulshan Dua | Recommends dak onward |
| Dak Sewadar — Area HQ | Sh. Ranjit Kumar | Marks and puts up at the Area |
| State Secretary — Punjab | Dr. Lekhi Ji | Decides what the State settles |
| Zonal Secretary — Zone-II | Sh. Aviraj Singh | Decides what the Zone settles |
| DHS Admin — Zone-II | Sh. Naresh Gupta | Topics & workflows, users and access |
| Engineering / Legal / Accounting | Zonal Office departments | See only their own category of dak |
| 2IC — SCI Office | Col. Ajay Singh | The final approving office |

---

## Worth trying

- **Raise a dak.** *New Dak* → pick a Document Type and Subject. The path, the form and who decides
  are settled by the topic, not by the person raising it.
- **Watch the value decide the office.** On an SCI-15, mark items capital or revenue and change the
  cost — the approving office changes as you type. Nothing is approved at Satsang Place or Area level.
- **Reply and forward.** Open a dak in the Inbox. Recipients are limited to what that dak's own route
  allows; copies are read-only and never enter anyone's pending list.
- **Fill an SCI form.** *SCI Forms* → new. Use **Side by side** to watch the official sheet fill in as
  you type, then open it at actual size.
- **Approve something.** Any approval asks for the one-time code. The moment it is given, the system
  writes the **Approval Letter** and a **duly approved copy of every SCI form** — see them on the dak,
  or in *Approved Records*. The letter sets out the whole of what was approved, since it is the paper
  handed to the committee; the form stays on the office record, carrying the stamp of every authority
  in the line.
- **Watch the numbering.** Raise a dak on a topic that needs an SCI-52. The dak takes an `L-` number
  of its own; the form keeps its `F52-` number; neither changes when they are bound together.
- **Change the rules.** As DHS Admin, open *Topics & Workflows* and edit a topic. Tick *value-based*
  to see the approval limits themselves — change a figure, publish, and routing follows at once. Dak
  already in flight keep the version they started under.

---

## What R1 covers

- Topic-driven routing — the Document Type and Subject settle the path, the mode, the terminal
  authority, the mandatory forms and the value limits
- One Dak ID per dak, taken from its topic — `L-260908-0238` correspondence, `C-260908-0233` a circular
- Every SCI form numbered separately — `F52-260908-0237` — and bound to the dak without either number altering
- Office-instance scoping — each office sees only its own dak, not everything at its level
- Roles: signing authority, office staff, read-only, special status, department members, DHS Admin
- Reply / forward with recipients and copies, bounded by the dak's route
- SCI-15, SCI-52 and SCI-02 reproduced in the official format, with print and PDF
- Inward and outward registers, reports, workflow board, calendar with reminders
- Approval by one-time code — which then issues the approval letter and the approved forms
- The Approval Letter carries the particulars in full, over the stamp of the final approving authority
- The approved form carries the stamps of every authority in the line, in the order the dak travelled
- Approved Records — letters and approved forms kept permanently, open to every office involved
- Light and dark, and a mobile layout

## What R1 does not cover

- Any connection to SCM or the Beas systems
- Real authentication — the login switcher is a demonstration device
- Migration of the existing DHS and DMS records
- The central counter that issues the Dak ID (the scheme is settled; the prototype counts in the browser)

## Still to be settled with Beas

- **What is approved above the Zonal limit on an SCI-15.** The limits we have been given stop at the
  Zonal Office — capital ₹50,000, revenue ₹25,000. Anything larger is routed to the SCI Office
  **provisionally**, and is marked as such on screen.
- **The area codes**, if a reference of the office's own is ever to be quoted in outward correspondence.

---

## Feedback

Comments are welcome on anything — wording, sequence, what is missing, and above all whether the
routing matches how the offices actually work.

---

## What is new in this revision

**A dak is numbered from its topic, not from a form.** A dak takes `L` for correspondence or `C` for a
circular; every SCI form carries an `F` number of its own and binds to the dak without either number
altering. So the marker says at once what a reference identifies — `L` or `C` is a dak, `F` is a form.

- **An approval now writes its own papers.** The moment a decision is recorded the system issues an
  **Approval Letter** and a **duly approved copy of every SCI form** enclosed, without anyone drafting
  either. Both are kept permanently in **Approved Records**.
- **The letter carries the decision, not a reference to it.** It is the paper handed to the committee,
  so on an SCI-52 it sets out who is appointed and on whose bio-data, who continues, who stands
  relieved, and **the committee as it now reads**. The SCI form stays on the office record.
- **Every authority in the line is stamped.** One stamp per office — the place that submitted it, each
  office that recommended it, the office that decided — in the order the dak travelled, each naming a
  person, a designation and a date. The form's own recommendation boxes are filled in; the rest travel
  on an endorsement page. The Approval Letter bears the final approving authority's stamp alone.
- **The sheets in the decks are now shown at full size** — they are the prototype's own A4 pages, so
  what is on the slide is what the office would hold.
- A refusal produces the same papers, with the reason recorded.

*September 2026 · Prepared for review by the Zonal Offices and the SCI Office.*
