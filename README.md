# Reams Family Creations

Static website for **Reams Family Creations** — custom woodworking (tables, cutting boards, key holders, wall art, and more). Handcrafted with heart, designed for legacy.

## What’s included

- **Home** (`index.html`) — Hero, product categories, customer favorites, and CTAs
- **Gallery** (`gallery.html`) — Photo gallery of past work
- **About** (`about.html`) — Family story and craftsmanship
- **Contact** (`contact.html`) — Link to Google Form for custom work and pricing requests

## Run locally

Open `index.html` in a browser, or use a simple local server:

```bash
# Python
python -m http.server 8000

# Node (npx)
npx serve .
```

Then visit `http://localhost:8000`.

## Contact form (Google Forms)

The Contact page uses **Google Forms**. To connect your form:

1. Create a form at [Google Forms](https://forms.google.com) (e.g. “Custom work request” with name, email, project type, message).
2. Get the form link: **Send** → link icon → copy the URL (e.g. `https://docs.google.com/forms/d/e/1FAIpQLSd.../viewform`).
3. In `contact.html`, find the “Open request form” button and replace `YOUR_GOOGLE_FORM_ID` with the long ID from your URL (the part between `/e/` and `/viewform`). For example, if your link is `https://docs.google.com/forms/d/e/1FAIpQLSdXyZ123/viewform`, the ID is `1FAIpQLSdXyZ123`.

Optional: to embed the form on the page, uncomment the iframe block in `contact.html` and set the `src` to your form’s embed URL (in Google Forms: **Send** → **<>** embed → copy the `src` from the iframe).

## Your images (no Unsplash)

All images are loaded from the **`images`** folder. Add your own files with these names (or change the filenames in the HTML to match what you upload).

**Homepage — “Custom wood creations” section**

| File in `images/`   | Shows as        |
|---------------------|-----------------|
| `cutting-board.jpg` | Cutting Boards  |
| `wall-art.jpg`      | Wall Art & Signs|
| `key-holder.jpg`    | Key Holders     |
| `furniture.jpg`     | Furniture & Tables |

**Homepage — “Customer Favorites” section**

| File in `images/`   | Shows as                    |
|---------------------|-----------------------------|
| `rustic-board.jpg`  | Rustic End-Grain Board      |
| `ring-holder.jpg`   | Ring & Jewelry Holders      |
| `charcuterie.jpg`   | Cheese & Charcuterie Boards |
| `stool.jpg`         | Live-Edge Stools            |

**Gallery page**

| File in `images/`   | Caption                |
|---------------------|------------------------|
| `gallery-1.jpg` … `gallery-12.jpg` | End-grain board, rustic board, wall art, key holder, side table, stool, charcuterie, ring holder, desk, shelves, bowl, serving tray |

You can use `.jpg`, `.jpeg`, `.png`, or `.webp`; if you use a different extension, update the `src` in the HTML (e.g. `images/cutting-board.png`).

**Already in `images/`:** `logo.png` (your Reams Family Creations logo).

## GitHub repo and hosting (ModularGunworksLLC)

You can create this site in a **new repo under your existing GitHub user** `ModularGunworksLLC` and host it on GitHub Pages. Each repo gets its own site; your other repos are unaffected.

### 1. Create the repo

1. Go to [github.com](https://github.com) and sign in as **ModularGunworksLLC**.
2. Click **+** → **New repository**.
3. Name it (e.g. `reams-family-creations`).
4. **Public**, and do **not** add a README (this project already has one).
5. **Create repository**.

### 2. Push this project

From this project folder in a terminal:

```bash
git init
git add .
git commit -m "Initial commit: Reams Family Creations static site"
git branch -M main
git remote add origin https://github.com/ModularGunworksLLC/reams-family-creations.git
git push -u origin main
```

Use your actual repo name in place of `reams-family-creations` if you chose something else.

### 3. Turn on GitHub Pages

1. In the repo: **Settings** → **Pages**.
2. **Source**: Deploy from a **branch**.
3. **Branch**: **main**, folder **/ (root)**.
4. **Save**.

After a couple of minutes the site will be at:

**https://ModularGunworksLLC.github.io/reams-family-creations/**

(Replace `reams-family-creations` with your repo name if different.)

### 4. Custom domain (optional)

Under **Settings → Pages** you can add a custom domain and the DNS records GitHub provides.

## Tech

- Plain HTML and CSS (no build step).
- Fonts: [Google Fonts](https://fonts.google.com) (Cormorant Garamond, DM Sans).
- Contact: Google Forms (no backend on this repo).
