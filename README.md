# Deploying a React App to GitHub Pages

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f680/lottie.json"> Introduction
This guide walks you through the process of deploying a **React.js** project to **GitHub Pages** in a few simple steps.

## 📌 Prerequisites
- A **GitHub account**
- **Node.js & npm** installed
- A **React project** (create one using `npx create-react-app my-app` if needed)

---

## 1️⃣ Install `gh-pages`
First, navigate to your React project folder and install the `gh-pages` package:

```sh
npm install gh-pages --save-dev
```

---

## 2️⃣ Update `package.json`
Modify your `package.json` file to include the following fields:

```json
"homepage": "https://your-github-username.github.io/your-repo-name",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```
🔹 Replace `your-github-username` with your **GitHub username**
🔹 Replace `your-repo-name` with your **repository name**

---

## 3️⃣ Initialize a Git Repository (If Not Already Initialized)

```sh
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-github-username/your-repo-name.git
git push -u origin main
```

---

## 4️⃣ Deploy the App
Run the deployment command:

```sh
npm run deploy
```

This will build your React app and push the **`build/`** folder to the `gh-pages` branch on GitHub.

---

## 5️⃣ Enable GitHub Pages
1. Go to **GitHub Repository → Settings**
2. Scroll down to **Pages**
3. Under **Branch**, select `gh-pages`
4. Click **Save**

Your React app will be live at:
**`https://your-github-username.github.io/your-repo-name/`** 🎉

---

## 6️⃣ Fixing Routing Issues (Optional)
For React Router, add this to `public/index.html`:

```html
<browserrouter basename="/your-repo-name">
```

Or use a **redirect file** (`public/_redirects` for Netlify users).

---

## ✅ Conclusion
Now your React app is deployed on **GitHub Pages**! 🚀

Let me know if you need any clarifications or additional steps! 😃


