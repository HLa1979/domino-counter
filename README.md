# 🁣 Domino Counter — Free & On-Device

A mobile-first web app that counts domino dots using **pure computer vision in the browser** — no API key, no account, no cost, works offline.

## ✨ How it works (no AI API used)

1. Captures a photo from your camera
2. Converts to grayscale and finds the domino tile using blob detection
3. Applies morphological filtering (erode → dilate) to isolate pips
4. Uses connected-component analysis to count and locate each pip
5. Splits pips by the tile's centre line → left count + right count

Everything runs on your device in JavaScript. Zero server calls.

## 🚀 Deploy in 5 minutes — completely free

### Step 1 — Push to GitHub

```bash
git init
git add .
git commit -m "Domino counter — on-device CV"
git remote add origin https://github.com/YOUR_USERNAME/domino-counter.git
git branch -M main
git push -u origin main
```

Or drag-and-drop the files into a new GitHub repo via the web UI.

### Step 2 — Deploy to Vercel (free)

1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **Add New Project** → import `domino-counter`
3. Click **Deploy** — no settings needed, it's a static site
4. You get a live URL like `https://domino-counter-abc.vercel.app` ✅

### Alternative: GitHub Pages (also free)

1. Repo → **Settings** → **Pages**
2. Source: branch `main`, folder `/ (root)`
3. Live at `https://YOUR_USERNAME.github.io/domino-counter/`

---

## 📱 Usage tips

- **Best results**: white/cream tile on a dark surface, or dark tile on a light surface
- **Fill the frame** — get the tile to take up most of the view
- **Good lighting** — even, bright light, no harsh shadows
- Tap the **ⓘ** button in the app for on-screen tips
- Use the **upload button** if camera isn't available

## 🔒 Privacy

- No data ever leaves your device
- No accounts, no API keys, no analytics
- Works fully offline after first page load

## 🛠 Tech

- Pure HTML + CSS + Vanilla JS — zero dependencies, no build step
- Computer vision pipeline:
  - Grayscale conversion
  - Adaptive thresholding
  - Morphological opening (noise removal)
  - Connected-component labelling (BFS)
  - Circularity filtering to select pips
- `getUserMedia` for camera access
- `localStorage` for scan history

## 📁 Files

```
domino-counter/
├── index.html    ← entire app
├── vercel.json   ← Vercel deploy config
└── README.md
```
