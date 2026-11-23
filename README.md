# ✨ 3d-setup-progress

<div align="center">

**A premium, animated multi-step progress component built with pure HTML, Tailwind CSS & vanilla JavaScript.**

Smooth. Responsive. Purple + Slate. Zero dependencies.

[![Made with HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-success?style=for-the-badge)]()

</div>

---

## 🎯 Overview

A beautifully crafted **5-step progress bar** with buttery-smooth animations, 3D depth, and a polished congratulatory flow. Every step is filled with a satisfying **fill → tick** sequence before advancing — no jarring jumps, just pure premium polish.

Perfect for:
- 🧾 Onboarding flows
- 💳 Checkout / payment steppers
- 🛠️ Setup wizards
- 📝 Multi-page forms

---

## 🚀 Features

| Feature | Description |
|---|---|
| 🎨 **3D Depth** | Layered gradients, inset shadows & soft glows for a tactile, premium feel |
| 🌈 **Purple + Slate Theme** | Sophisticated color harmony with dark slate background for highlight |
| ⚡ **Smooth Sequence** | Circle fills purple → tick appears → line progresses → next step activates |
| 🔄 **Smart Prev Button** | Hidden on step 1, slides in smoothly from step 2 onwards |
| ✅ **Full Tick Coverage** | Even step 5 gets its tick mark before the Finish action |
| 🎉 **Congratulations Page** | Animated success card with 3D tick, pulse ring & spinner |
| 🌀 **Random 360° Spinner** | Full-turn rotation with random start/end points every cycle |
| 📱 **Fully Responsive** | Pixel-perfect from 320px phones to desktop |
| 🚪 **Redirect Ready** | Hooks ready for `window.location.href` to any next page |

---

## 📸 Preview

<div align="center">

| Stepper | Success Page |
|:---:|:---:|
| *5-step progress with fill-and-tick animation* | *Congratulations with spinning redirect indicator* |

</div>

> 💡 *Tip: Open the file in browser to experience the smooth transitions live.*

---

## 🛠️ Tech Stack

- **HTML5** — Semantic structure
- **Tailwind CSS** (CDN) — Utility-first styling
- **Vanilla JavaScript** — State machine & animations
- **CSS3** — Custom keyframes, conic gradients, 3D shadows

**Zero build tools. Zero npm. Just open and go.**

---

## 📦 Quick Start

### Option 1 — Direct Download
1. Download `index.html`
2. Double-click to open in your browser
3. Done ✅

### Option 2 — Clone the Repo
```bash
git clone https://github.com/abdurrab70/3d-setup-progress.git


```
Then open `index.html` in your browser.

### Option 3 — Local Server (recommended for development)
```bash
# With Python
python -m http.server 8000

# Or with Node
npx serve
```
Visit `http://localhost:8000`

---

## 🎮 How It Works

```
[Step 1: Account] → [Step 2: Profile] → [Step 3: Details] → [Step 4: Payment] → [Step 5: Done] → 🎉 Success
```

### The Animation Sequence

Every time **Next** is clicked:

1. **Fill** — Current step's circle fills with purple gradient (`~480ms`)
2. **Tick** — Checkmark scales in and number fades out (`~380ms`)
3. **Advance** — Progress line fills smoothly & next step becomes active (`~850ms`)

The whole chain is locked with an `isAnimating` flag so nothing breaks — no double clicks, no visual glitches.

---

## 🔗 Connect to Your Next Page

Inside the `<script>` tag, find the `showSuccess()` function and uncomment the redirect line:

```javascript
redirectTimer = setTimeout(() => {
  // 👇 Change to your actual URL
  window.location.href = 'dashboard.html';
}, 4500);
```

That's it — the spinner will run for 4.5 seconds, then redirect automatically.

---

## 🎨 Customization Guide

### Change Step Labels

Find this array in the `<script>`:

```javascript
const labels = ['Account', 'Profile', 'Details', 'Payment', 'Done'];
```

Replace with your own step names. Also update the HTML labels accordingly:

```html
<span class="step-label ...">Account</span>
```

### Change Theme Colors

Look for the CSS custom properties near the top:

```css
:root {
  --indigo: #6366f1;
  --indigo-dark: #4f46e5;
}
```

Or simply **find-and-replace** these purple values across the file:

| Current | Replace with |
|---|---|
| `#a855f7` | Your primary |
| `#7c3aed` | Your primary dark |
| `#c084fc` | Your primary light |

### Adjust Animation Speed

In the JavaScript `completeStep()` function:

```javascript
setTimeout(() => { ... }, 480);  // Fill duration
setTimeout(() => { ... }, 380);  // Tick duration
```

In CSS, look for `transition` properties on `.track-fill`, `.step-circle`, `.fill-overlay`, etc.

### Change Number of Steps

Currently set to **5 steps**. To add/remove:
1. Add/remove `.step-col` divs in the HTML
2. Update the `labels` array
3. Adjust `.steps-container { grid-template-columns: repeat(5, 1fr); }` — change `5` to your count
4. Line math: `left: 10%; right: 10%` — for `N` steps it's `left: calc(50% / N); right: calc(50% / N);`

---

## 📁 Project Structure

```
3d-polished-stepper/
│
├── index.html          # Complete standalone file
│                       # (HTML + CSS + JS in one place)
│
└── README.md           # You're reading it 😊
```

**Why single file?**
Because this is a *component demo* — copy, paste, drop into any project. No setup, no build step, no headaches.

---

## 🌐 Browser Support

| Browser | Status |
|---|---|
| Chrome | ✅ Full support |
| Edge | ✅ Full support |
| Firefox | ✅ Full support |
| Safari | ✅ Full support (iOS 14+) |
| Opera | ✅ Full support |

> Requires modern CSS (`conic-gradient`, `mask`, `clamp`, `backdrop-filter`). IE is not supported.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the project
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

---

## 📄 License

Distributed under the **MIT License**. Free to use in personal & commercial projects.

See `LICENSE` for more information.

---

## 💡 Inspiration

Built with a love for **micro-interactions** — the small details that make interfaces feel *alive*. If a progress bar can feel satisfying, everything else should too.

---

<div align="center">

### ⭐ If this helped you, consider giving it a star!

**Made with 💜 and a lot of `cubic-bezier()`**

</div>
