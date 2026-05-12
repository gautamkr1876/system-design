# 🚀 Deploy to GitHub Pages — Step-by-Step Guide

Get your Q&A page live on the internet in **under 10 minutes**, completely free.

After this, you'll have a URL like:
**`https://your-username.github.io/interview-prep/`**

That you can:
- Bookmark on phone/laptop
- Share with friends preparing for interviews
- Open anywhere with internet

---

## ✅ What You Need

- A GitHub account (free — [sign up](https://github.com/signup) if you don't have one)
- The two files we created:
  - `index.html` (your Q&A page)
  - `README.md` (description for your repo)

---

## 🪜 Method 1: Easy Way (Web UI — No Git Commands)

Best if you're new to GitHub.

### Step 1: Create a New Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **`+`** icon (top right) → **New repository**
3. Fill in:
   - **Repository name**: `interview-prep` (or any name you like)
   - **Description**: "My frontend interview Q&A reference"
   - **Public** ✅ (required for free GitHub Pages)
   - ✅ Check **"Add a README file"**
4. Click **Create repository**

### Step 2: Upload Your Files

1. On your new repo page, click **Add file** → **Upload files**
2. Drag both files into the upload area:
   - `index.html`
   - `README.md` (this will replace the auto-generated one — that's fine)
3. Scroll down, write commit message: `Add singleton Q&A page`
4. Click **Commit changes**

### Step 3: Enable GitHub Pages

1. In your repo, click **Settings** (top menu)
2. In the left sidebar, click **Pages**
3. Under **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / `(root)` → click **Save**
4. Wait ~1 minute. Refresh the Pages settings page.
5. You'll see: **"Your site is live at `https://your-username.github.io/interview-prep/`"** 🎉

### Step 4: Visit Your Live Site

Click the URL — your Q&A page is now live on the internet!

---

## 🪜 Method 2: Power User Way (Git Command Line)

If you're comfortable with terminal:

```bash
# Create a new folder and add your files
mkdir interview-prep
cd interview-prep
# Copy your index.html and README.md into this folder

# Initialize Git
git init
git add .
git commit -m "Initial Q&A reference"

# Connect to GitHub (create the repo on github.com first)
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/interview-prep.git
git push -u origin main
```

Then enable Pages in the repo Settings (same as Step 3 above).

---

## 📱 Bonus: Add to Phone Home Screen

Once live, on your phone:

**iPhone (Safari):**
1. Open the URL
2. Tap the Share button
3. Tap **Add to Home Screen**

**Android (Chrome):**
1. Open the URL
2. Tap the menu (3 dots)
3. Tap **Add to Home screen**

Now your study page is one tap away — like a real app!

---

## 🔄 Updating Content Later

When you want to add new questions or topics:

**Easy way (web UI):**
1. Go to your repo on GitHub
2. Click on the file you want to edit (e.g., `index.html`)
3. Click the **pencil ✏️ icon** (Edit this file)
4. Make changes, scroll down, **Commit changes**
5. Wait ~1 minute → live site updates automatically

**Git way:**
```bash
# Edit files locally
git add .
git commit -m "Add React hooks questions"
git push
```

---

## 🌳 Recommended Folder Structure (for growth)

As you add more topics, organize like this:

```
interview-prep/
├── index.html              ← landing page with links to all topics
├── README.md
├── singleton.html          ← singleton Q&A (current)
├── react-hooks.html        ← future topic
├── event-loop.html         ← future topic
├── css-grid.html           ← future topic
└── system-design.html      ← future topic
```

You can update `index.html` to be a **homepage with links to all topics**:

```html
<h1>My Interview Prep</h1>
<ul>
  <li><a href="singleton.html">Singleton Pattern (44 Q)</a></li>
  <li><a href="react-hooks.html">React Hooks (50 Q)</a></li>
  <li><a href="event-loop.html">Event Loop (30 Q)</a></li>
</ul>
```

Just say the word and I'll generate any new topic in the same format.

---

## 💡 Troubleshooting

**"Site shows 404 Not Found"**
- Wait 2-3 minutes after enabling Pages (it takes a moment to deploy)
- Make sure your file is named `index.html` exactly (lowercase)
- Check Settings → Pages shows "Your site is live at..."

**"My changes aren't showing"**
- Hard refresh: `Ctrl + Shift + R` (Windows) or `Cmd + Shift + R` (Mac)
- Wait ~1 minute after committing — Pages takes a moment to rebuild

**"Want a custom domain?"**
- Buy a domain (Namecheap, Google Domains, etc.)
- In Pages settings, add your custom domain
- GitHub provides free HTTPS — done

---

## 🎯 Your Next Steps

1. ✅ Upload `index.html` + `README.md` to GitHub
2. ✅ Enable Pages
3. ✅ Bookmark the live URL on your phone
4. ✅ Come back and ask me to generate the next topic (React Hooks? Event Loop? Just say the word)

Happy studying! 🚀
