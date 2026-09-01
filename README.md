# Stick Memo — Website Files

Everything you need for your website is in this folder. You don't need to
know how to code to make small changes — just open `index.html` in a text
editor (Notepad, TextEdit, or a free app like Notepad++ / VS Code) and edit
the text between the tags.

## What's in this folder

```
stickmemo-website/
├── index.html              ← your whole website (one file)
├── README.md                ← this file
└── assets/
    ├── logo.webp             ← your logo, used on the live site
    ├── logo-original.png     ← full-quality logo, for printing/other uses
    ├── templates/             ← put real template screenshots here (see below)
    └── occasional/            ← put real Rakhi/seasonal photos here (see below)
```

## How to put this online

Pick whichever is easiest for you:

- **Netlify Drop** (easiest, free): go to https://app.netlify.com/drop and
  drag this whole folder onto the page. It gives you a live link instantly.
- **GitHub Pages**: upload the folder to a GitHub repository and turn on
  Pages in the repo settings.
- **Any web host / cPanel**: upload the whole folder (keeping the `assets`
  folder alongside `index.html`) to your hosting via File Manager or FTP.

Wherever you host it, always upload the `assets` folder together with
`index.html` — the page won't show your logo or photos without it.

## How to update things yourself

Open `index.html` in a text editor and use Find (Ctrl+F / Cmd+F) to jump to
the part you want to change.

### 1. Prices
Search for `price-card`. You'll find two blocks — Paper (Rs. 200) and Glossy
(Rs. 300). Change the number inside `<div class="amount">Rs. 200 ...`.

### 2. Occasional products (Rakhi, festival specials, etc.)
Search for `EDIT ME EACH SEASON`. Just below it are three `occ-card` blocks —
one per product. For each one:
- Replace the photo: put your image file in `assets/occasional/` (e.g.
  `rakhi-1.jpg`), then change the `<div class="occ-photo">` line to
  `<div class="occ-photo" style="background-image:url('assets/occasional/rakhi-1.jpg'); background-size:cover;">` (delete the placeholder `<svg>` and `<span>` lines inside it if you add a real photo).
- Change the name in `<h3>Silk Thread Rakhi</h3>`.
- Change the price in `<div class="price">Rs. 49</div>`.
- Change the short description in the `<p>` line below it.
- To add a 4th product, copy one whole `occ-card` block (from `<div
  class="occ-card"` to its closing `</div>`) and paste it right after,
  then edit the copy.
- To remove a product, delete its whole `occ-card` block.

### 3. The 9 templates
Each of the 9 cards is a real-to-scale diagram of that sheet's sticker
layout — drawn directly from your measured frame positions, not a photo.
Each dashed box is exactly where one sticker sits on the A4 page, at the
correct size and shape. This means:
- The sticker count shown on each card (e.g. "20 stickers") is real,
  not a placeholder.
- If you change a layout in Canva (move, resize, add, or remove a frame),
  the diagram in `index.html` won't update itself — you'd need to send
  Claude the new positions (or a fresh export) to regenerate that card.
- If you'd rather show actual photos of filled-in templates instead of
  these diagrams, save your exported images into `assets/templates/` and
  ask Claude to swap a card's `<svg>...</svg>` block for an `<img>` tag —
  the folder is already there and ready for that.
- Template names (e.g. "Square Classic") are in the `<span class="label">`
  line of each card if you want to rename any of them.

### 4. Contact details
Your WhatsApp number and Instagram link each appear a few times — search for
`9779704332208` (WhatsApp) or `stickmemo` (Instagram) and update every match
if these ever change.

### 5. Canva template link
Search for `canva.link` — that's the button that sends people to browse your
full template pack.

### 6. Link preview (after you're hosted)
Search for `YOUR-DOMAIN-HERE` (appears 3 times near the top of the file) and
replace it with your real website address once it's live — e.g.
`https://stickmemo.netlify.app`. This makes a proper preview card (your logo
+ title + description) show up when someone shares your site link in
WhatsApp, Instagram, or elsewhere. It's harmless to leave as-is if you
haven't hosted the site yet.

## Notes

- The page is a single HTML file with everything (styling + behaviour)
  built in, so it works offline too — just double-click `index.html` to
  preview it in your browser before uploading anywhere.
- Delivery charges are intentionally left out of the displayed prices, with
  a note underneath the pricing cards explaining they're calculated
  separately.
