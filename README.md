# 🁣 Domino Counter — Deployment Guide

A mobile-first web app that uses Claude's vision AI to count domino pips from your camera.

---

## 📁 Files
```
domino-counter/
├── index.html      ← The entire app (single file)
└── manifest.json   ← Makes it installable as a home screen app
```

---

## 🚀 Deploy to Vercel (Recommended — 5 minutes)

1. **Create a GitHub account** at github.com (if you don't have one)
2. **Create a new repository** called `domino-counter`
3. **Upload both files** (index.html + manifest.json) to the repo
4. **Go to vercel.com** → Sign up with GitHub → Click "Add New Project"
5. **Import your repo** → Click Deploy
6. ✅ You'll get a URL like `https://domino-counter.vercel.app`

**Share that link with your family!**

---

## 📱 Install as Home Screen App (Android)

1. Open the link in **Chrome** on Android
2. Tap the **3-dot menu** (top right)
3. Tap **"Add to Home screen"**
4. It will appear as an app icon — no App Store needed!

---

## 🔑 API Key Setup

Each family member needs to enter an **Anthropic API key** the first time they open the app.

**Getting a key:**
1. Go to https://console.anthropic.com
2. Sign up for a free account
3. Go to "API Keys" → Create a key (starts with `sk-ant-`)
4. Enter it in the app — it's saved to their device only

**Cost:** Claude Vision is very cheap. Counting dominoes uses ~500 tokens per scan ≈ $0.001 per scan.

---

## 🛡 Privacy & Security
- API keys are stored only in the user's browser (localStorage)
- Images are sent directly to Anthropic's API — not stored anywhere
- No backend, no database, no accounts needed

---

## 🎮 How to Use
1. Open the app and enter your API key
2. Tap **Open Camera** to use your phone camera
   — or tap **Upload** to use a photo from your gallery
3. Point at your domino tiles and tap **Count Pips →**
4. Review the detected tiles (shown as chips like `3|5`)
5. Tap **+ Add to Total** to add to your session score
6. **Reset** starts a fresh game session

---

## 🐛 Troubleshooting
- **Camera not working?** Use the Upload button instead (some browsers restrict camera)
- **Wrong count?** Make sure tiles are well-lit and not overlapping
- **API error?** Double-check your API key is correct and has credits
