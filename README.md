# Deploying a React App to GitHub Pages

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f680/512.gif" alt="🚀" width="32" height="32"> Introduction
This guide walks you through the process of deploying a **React.js** project to **GitHub Pages** in a few simple steps.

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/26a1/512.gif" alt="⚡" width="32" height="32"> Prerequisites
- A **GitHub account**
- **Node.js & npm** installed
- A **React project** (create one using `npx create-react-app my-app` if needed)

---

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4a1/512.gif" alt="💡" width="32" height="32"> Install `gh-pages`
First, navigate to your React project folder and install the `gh-pages` package:

```sh
npm install gh-pages --save-dev
```

---

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4a1/512.gif" alt="💡" width="32" height="32"> Update `package.json`
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

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4a1/512.gif" alt="💡" width="32" height="32"> Initialize a Git Repository (If Not Already Initialized)

```sh
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-github-username/your-repo-name.git
git push -u origin main
```

---

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4a1/512.gif" alt="💡" width="32" height="32"> Deploy the App
Run the deployment command:

```sh
npm run deploy
```

This will build your React app and push the **`build/`** folder to the `gh-pages` branch on GitHub.

---

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4a1/512.gif" alt="💡" width="32" height="32"> Enable GitHub Pages
1. Go to **GitHub Repository → Settings**
2. Scroll down to **Pages**
3. Under **Branch**, select `gh-pages`
4. Click **Save**

Your React app will be live at:
**`https://your-github-username.github.io/your-repo-name/`** <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f389/512.gif" alt="🎉" width="32" height="32">

---

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f4a1/512.gif" alt="💡" width="32" height="32"> Fixing Routing Issues (Optional)
For React Router, add this to `public/index.html`:

```html
<browserrouter basename="/your-repo-name">
```

Or use a **redirect file** (`public/_redirects` for Netlify users).

---

## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/2705/512.gif" alt="✅" width="32" height="32"> Conclusion
Now your React app is deployed on **GitHub Pages**! <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f680/512.gif" alt="🚀" width="32" height="32">

Let me know if you need any clarifications or additional steps! <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/2764_fe0f/512.gif" alt="❤" width="32" height="32">


## <img src="https://fonts.gstatic.com/s/e/notoemoji/latest/1f31f/512.gif" alt="🌟" width="32" height="32"> Show Some Love!  
If you liked this, consider giving it a ⭐ and following me! 🚀  

<a href="https://github.com/aman-khan001">
  <img src="https://img.shields.io/github/followers/your-username?label=Follow%20Me&style=social" alt="GitHub Followers">
</a>

[![GitHub followers](https://img.shields.io/github/followers/aman-khan001?label=Follow%20Me&style=social)](https://github.com/aman-khan001)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/aman-khan001/)  

<img src="https://media.giphy.com/media/3o7abKhOpu0NwenH3O/giphy.gif" width="200px">



