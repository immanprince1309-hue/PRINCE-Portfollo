# Prince — Cybersecurity Engineer & Full-Stack Developer Portfolio

A modern, responsive, recruiter-ready portfolio website engineered for Prince (B.E. Cyber Security, Tagore Engineering College, Anna University).

## 🚀 Live Preview & Deployment

### Quick Local Preview
1. Simply double-click `index.html` to open it in any web browser, OR
2. Run a local web server with Python:
   ```bash
   python -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser.

### Free Deployment on GitHub Pages (2 Minutes)
1. Push this directory to a GitHub repository (e.g. `prince-portfolio` or `username.github.io`).
2. Go to **Settings** > **Pages**.
3. Under **Branch**, select `main` (or `master`) and folder `/ (root)`.
4. Click **Save** — your site will be live instantly!

---

## 🛠️ Personalization & Placeholders

All personal information and placeholders can be configured in one central place:

### 1. Update Socials & Links
Open `js/script.js` and edit the `PORTFOLIO_CONFIG` object at the top:
```javascript
const PORTFOLIO_CONFIG = {
  name: "Prince",
  title: "Cybersecurity Engineer & Full-Stack Developer",
  email: "imman.prince1309@gmail.com",
  phone: "+91 90033 40109",
  location: "Chengalpattu, Tamil Nadu",
  
  // Social Links
  githubUrl: "https://github.com/YOUR_GITHUB_USERNAME", // Update your GitHub
  instagramUrl: "https://instagram.com/imman.prince",
  
  // Project URLs
  projects: {
    femcare: { live: "#", repo: "https://github.com/..." },
    ...
  }
};
```

### 2. Add Your Real Headshot Photo
- Save your portrait image as `images/profile.jpg`.
- The site will automatically load `images/profile.jpg` with a cyber-styled glowing border. If the file is missing, it will gracefully fall back to the custom cyber avatar `images/profile.svg`.

---

## 🎨 Design System & Features
- **Color Palette**: Cyber Dark (`#08090c`), Deep Surface (`#0e1117`), Electric Cyan (`#00F0FF`), Neon Green (`#39FF14`).
- **Typography**: `Inter` (UI & Body) + `JetBrains Mono` (Headings, Badges, Metrics).
- **Responsive Layout**: Fluid breakpoints for mobile (375px), tablet (768px), and high-res desktop (1440px+).
- **Zero Build Step**: Pure semantic HTML5 + Tailwind CSS CDN + Lucide Icons + Vanilla JavaScript for zero-lag instant loading.
