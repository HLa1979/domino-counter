# 🁣 Domino Counter

## ✨ How it works

1. Captures a photo from your camera
2. Converts to grayscale and finds the domino tile using blob detection
3. Applies morphological filtering (erode → dilate) to isolate pips
4. Uses connected-component analysis to count and locate each pip
5. Splits pips by the tile's centre line → left count + right count

Everything runs on your device in JavaScript. Zero server calls.


## 📁 Files

```
domino-counter/
├── index.html    ← entire app
├── vercel.json   ← Vercel deploy config
└── README.md
```
