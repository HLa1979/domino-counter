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
