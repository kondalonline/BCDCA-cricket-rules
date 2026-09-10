# BCDCA Cricket Rules App

A clean, mobile-friendly reference app for:
- **MCC Laws of Cricket** — all 42 Laws (2017 Code), with full clause-by-clause text
- **BCDCA Senior Competition Rules** (2023-24)
- **BCDCA Junior Competition Rules** (2026-27)

Built as a **Progressive Web App (PWA)** — installs on your Android phone with
its own icon and opens full-screen like a normal app, no APK/Play Store step
required.

---

## Option A — Easiest & most reliable: one single file

**Use `BCDCA-Cricket-Rules.html`** (in this same folder / at the top level of the
zip). It has everything — all the styling, code, and rule content — baked into
one file, so there's nothing that can go missing if it gets transferred on its
own. This is the recommended way to try it.

1. Send yourself `BCDCA-Cricket-Rules.html` (email, WhatsApp, Google Drive, USB
   cable — any method that lands the file on your phone's storage).
2. Open your phone's **Files** app, find the file, and tap it. Choose **Chrome**
   if asked which app to open it with.
3. In Chrome, tap the **⋮** menu (top right) → **Add to Home screen** → **Install/Add**.
4. A "BCDCA Cricket Rules" icon appears on your home screen. Tap it — it opens
   full-screen, no address bar, just like a normal app. Works fully offline from
   then on.

## Option B — Multi-file version (for hosting online)

The `BCDCA-Cricket-Rules-App/` folder contains the same app split into its
component files, for hosting on Netlify Drop, GitHub Pages, or any static host
if you want the full installable-PWA banner experience later. If you just want
to try the app on your own phone, skip this and use Option A.

---

## How the navigation works

- **Home** shows the 3 sections as icons/cards.
- **MCC Laws** → tap any of the 42 Laws → see its numbered clauses → tap any
  clause to read its full text.
- **BCDCA Senior / Junior Rules** → tap a category → tap a rule → read the full
  rule text.
- The **back arrow** (top left) always returns to the exact previous screen.
- The **Home** button (bottom, always visible) jumps straight back to the home
  screen from anywhere.

## Revision history

1. **Initial build**: full app with all three sections, but MCC Law sub-clauses
   were outline/title-only — tapping a clause had nowhere to go.
2. **MCC fix**: found that the source PDF stores each printed page as a
   two-page spread merged into one wide PDF page, which was scrambling
   sentence order and truncating clauses on naive extraction. Rebuilt the
   extraction to read each half of every page in the correct order, then
   cleaned up several resulting PDF artifacts. All 270 clauses across all 42
   Laws now have full, verified text, and are tappable from each Law's clause
   list.
3. **BCDCA accuracy pass**: audited all 179 Senior and Junior rule entries
   line-by-line against the source PDFs — every time, fee, over-count,
   distance and percentage checked out. Fixed one internal numbering slip
   (Senior Rule 40's sub-clauses were labelled 41.1/41.2) and tightened the
   wording of a couple of the more repetitive entries (e.g. the Junior Parent
   Code of Behaviour) without dropping any content.

## A note on accuracy

All content is sourced directly from the three PDFs you provided:
`senior_comp_rules_2023.pdf`, `junior-bcdca-2026-27-rules.pdf`, and
`Laws-of-Cricket-2017-MCC-2026.pdf`. The MCC Laws are presented in full,
extracted directly from the official document. The BCDCA rule text has been
organised and condensed for on-screen readability while preserving every
number, time, over-count, fee and figure exactly as written — condensing was
about tightening wording, not changing meaning. If you spot anything that
still looks off against the source PDFs, flag it and it can be corrected.
