# 🛠️ How to Update & Customize Your Portfolio

This guide explains how to adjust your profile image position and easily add new projects, skills, or achievements anytime in the future!

---

## 1. 🖼️ How to Adjust Your Profile Image Position

Your portrait position is controlled by a single line in [`css/style.css`](css/style.css#L271).

Open `css/style.css` and find `.profile-portrait-img` around line 270:
```css
.profile-portrait-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center 18%; /* <-- CHANGE THIS VALUE */
}
```

### Quick Reference for `object-position`:
- **`center 10%`** or **`center 5%`**: Moves the photo **down** (shows more of your hair/head).
- **`center 18%`** (Current default): Perfectly balanced headshot center.
- **`center 30%`** or **`center 40%`**: Moves the photo **up** (shows more of your suit/shoulders).
- **`center center`**: Exactly centered vertically.

---

## 2. 🚀 How to Add a New Project

Open [`index.html`](index.html) and scroll to the `<section id="projects">` section.

Copy and paste this template card into the project grid:

```html
<!-- New Project Card -->
<article class="reveal lg:col-span-6 bento-card spotlight-card p-6 sm:p-8 flex flex-col justify-between space-y-6">
  <div class="space-y-4">
    <div class="flex items-center justify-between">
      <span class="status-pill text-[#00e5ff] bg-[#00e5ff]/10 border-[#00e5ff]/20">
        <i data-lucide="shield" class="w-3.5 h-3.5"></i> Security Project
      </span>
      <span class="text-xs font-mono text-[#9ca3af]">Category</span>
    </div>
    <h3 class="text-xl font-display font-bold text-white">Your Project Title</h3>
    <p class="text-sm text-[#9ca3af] leading-relaxed">
      A 1-2 sentence description explaining what problem you solved, what stack you used, and the impact.
    </p>
    <div class="flex flex-wrap gap-1.5 pt-2">
      <span class="tech-tag">Python</span>
      <span class="tech-tag">Flask</span>
      <span class="tech-tag">Cryptography</span>
    </div>
  </div>
  <div class="pt-4 border-t border-white/[0.06] flex items-center justify-between text-xs font-mono">
    <a href="https://your-demo-url.com" target="_blank" class="text-[#00e5ff] hover:underline flex items-center gap-1">
      <i data-lucide="external-link" class="w-3.5 h-3.5"></i> Live Demo
    </a>
    <a href="https://github.com/your-username/repo-name" target="_blank" class="text-[#9ca3af] hover:text-white flex items-center gap-1">
      <i data-lucide="github" class="w-3.5 h-3.5"></i> Repository
    </a>
  </div>
</article>
```

> **Tip:** You can set `lg:col-span-12` for a full-width hero project, or `lg:col-span-6` for half-width.

---

## 3. ⚡ How to Add New Skills

Open [`index.html`](index.html) and find the `<section id="skills">` area.

Simply add a `<span class="tech-tag">...</span>` inside any of the category cards:
```html
<span class="tech-tag">Docker & Kubernetes</span>
<span class="tech-tag">Burp Suite</span>
<span class="tech-tag">Wireshark</span>
```

---

## 4. 🏆 How to Add New Hackathons, CTFs, or Milestones

Open [`index.html`](index.html) and find `<section id="milestones">`.

Add a milestone card:
```html
<div class="reveal bento-card spotlight-card p-6 space-y-3">
  <div class="flex items-center gap-3">
    <div class="p-2.5 rounded-xl bg-[#00e5ff]/10 border border-[#00e5ff]/20 text-[#00e5ff]">
      <i data-lucide="award" class="w-5 h-5"></i>
    </div>
    <div>
      <h3 class="font-display font-bold text-white text-base">Competition Name</h3>
      <span class="text-xs text-[#00e5ff] font-mono">1st Place / Finalist</span>
    </div>
  </div>
  <p class="text-xs text-[#9ca3af] leading-relaxed">
    Brief summary of what you built, defended, or solved.
  </p>
</div>
```

---

## 5. 💻 How to Update the Interactive Terminal

Open [`js/script.js`](js/script.js) and look for the `commands` object around line 40. You can edit the output or add new commands (like `certifications`, `resume`, etc.):

```javascript
certifications: () => `
<div class="text-[#00e5ff] font-bold">Certifications:</div>
<div>1. Certified Ethical Hacker (CEH) - In Progress</div>
<div>2. CompTIA Security+</div>`
```

---

## 6. 🌐 How to Change Social Media / Contact Links

Open [`js/script.js`](js/script.js) and update the `PORTFOLIO_DATA` block at the top:
```javascript
const PORTFOLIO_DATA = {
  name: "Prince",
  email: "imman.prince1309@gmail.com",
  phone: "+91 90033 40109",
  location: "Chengalpattu, Tamil Nadu",
  github: "https://github.com/YOUR_ACTUAL_USERNAME",
  instagram: "https://instagram.com/imman.prince",
  ctfTeam: "Team Marvelss"
};
```
