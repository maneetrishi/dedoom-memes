# 🦝 Dedoom Live Memes Repository

This repository hosts dynamic meme attacks for the **Dedoom Chrome Extension**.

When distracting websites (Instagram, YouTube, TikTok, Reddit, etc.) are opened, Dedoom pulls randomly from this meme pool.

## 🚀 How to Host & Update Memes in Real Time

### 1. Push this folder to your GitHub
1. Create a new GitHub repository (e.g. `dedoom-memes`).
2. Upload the contents of this folder (`manifest.json` and the `memes/` directory).
3. Ensure the repository is **Public** so the extension can read `manifest.json` and the images.

### 2. Connect to Dedoom
In Dedoom's **background.js** or via the **Dedoom Dashboard Settings**:
Set your raw GitHub manifest URL:
```text
https://raw.githubusercontent.com/<YOUR-GITHUB-USERNAME>/<YOUR-REPO-NAME>/main/manifest.json
```

### 3. Adding or Updating Memes Anytime
Whenever you want to add new memes or edit captions:
1. Add new images into `memes/` (e.g. `meme26.png`).
2. Add an entry to `manifest.json`:
   ```json
   {
     "id": "meme26",
     "url": "memes/meme26.png",
     "caption": "your hilarious new caption here"
   }
   ```
3. Commit and push to GitHub.

**That's it!** All installed Dedoom extensions worldwide will automatically sync the updated memes in the background. No extension reload, no reinstall, and no Chrome Web Store re-review required!
