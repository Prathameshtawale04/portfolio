# Prathamesh Tawale - 3D Interactive Portfolio

> **MCA Student | Aspiring Data Analyst & Data Scientist | Python Developer**  
> A high-performance, recruiter-friendly 3D portfolio featuring scroll-tied Three.js animations, GSAP ScrollTrigger, Lenis smooth scrolling, and custom interactive engineering visualizers.

---

## 🌟 Live Demo & Positioning

- **Name:** Prathamesh Sanjay Tawale
- **Primary Roles:** Data Analyst, Data Scientist, Python Developer
- **Secondary Domains:** Machine Learning, Data Visualization, Full-Stack Web Development, IoT & Embedded Systems
- **Location:** Pune, Maharashtra, India
- **Education:** Master of Computer Applications (MCA) – P.E.S. Modern College of Engineering, Pune (MAH MCA CET 96th Percentile, Rank 800)

---

## 🛠️ Tech Stack & Architecture

- **Frontend Framework:** React 18 (Vite)
- **3D Graphics & Canvas:** Three.js, `@react-three/fiber`, `@react-three/drei`
- **Animation & Scroll Orchestration:** GSAP (GreenSock), GSAP ScrollTrigger
- **Smooth Scrolling:** Lenis (`lenis`)
- **Icons:** Lucide React (`lucide-react`)
- **Styling:** Modular CSS architecture with dark-mode tokens, glassmorphism, fluid responsive layouts, and accessibility support (`prefers-reduced-motion`)

---

## 🚀 Quick Start (Running Locally)

### 1. Prerequisites
Ensure you have [Node.js](https://nodejs.org/) (v18+ recommended) and npm installed:
```bash
node -v
npm -v
```

### 2. Navigate to Project
```bash
cd C:\Users\p\.gemini\antigravity\scratch\prathamesh-portfolio
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Start Development Server
```bash
npm run dev
```
Open your browser at `http://localhost:3000` to preview the interactive experience with instant Hot Module Replacement (HMR).

### 5. Build for Production
```bash
npm run build
```
This compiles optimized, minified, code-split production bundles in the `/dist` directory.

### 6. Preview Production Build
```bash
npm run preview
```
Serves the generated production build locally on `http://localhost:4173`.

---

## 📁 Project Structure

```text
prathamesh-portfolio/
├── public/
│   ├── favicon.svg                       # Tech monogram favicon
│   ├── prathamesh_photo.jpg              # Profile photograph
│   └── Prathamesh_Tawale_Resume.pdf      # Downloadable resume PDF
├── src/
│   ├── assets/                           # Static assets
│   ├── data/
│   │   └── portfolioData.js              # ⚡ SINGLE SOURCE OF TRUTH (All resume data & configs)
│   ├── hooks/
│   │   ├── useScrollSpy.js               # Tracks active section for navbar
│   │   └── useReducedMotion.js           # Accessibility reduced-motion detection
│   ├── components/
│   │   ├── Navbar.jsx                    # Floating glassmorphism navbar with active pill
│   │   ├── Footer.jsx                    # Recruiter-ready footer with status & back-to-top
│   │   ├── CustomCursor.jsx              # Magnetic follower dot & ring for desktop
│   │   ├── ScrollProgressBar.jsx         # Top glowing scroll progress bar
│   │   └── ProjectModal.jsx              # Deep-dive architecture & specs modal
│   ├── three/
│   │   ├── SceneContainer.jsx            # Non-blocking R3F background canvas wrapper
│   │   ├── BackgroundSphere.jsx          # Scroll-tied 3D data sphere & constellation
│   │   └── ProjectVisuals/
│   │       ├── CovidVisual.jsx           # Animated epidemic curves & EDA telemetry
│   │       ├── MovieRecVisual.jsx        # Cosine similarity matrix & neural node graph
│   │       ├── SmartCityVisual.jsx       # Isometric cyber city grid & live sensor pulses
│   │       └── SmartCarVisual.jsx        # Autonomous road lanes, 8-IR beams & sonar radar
│   ├── sections/
│   │   ├── Hero.jsx                      # Full-screen hero with CTA buttons & social links
│   │   ├── About.jsx                     # MCA/BCA narrative, CET rank & verified stats
│   │   ├── Skills.jsx                    # Filterable skill matrix with search & categories
│   │   ├── Projects.jsx                  # Flagship projects with custom interactive visuals
│   │   ├── Education.jsx                 # Academic degree timeline & verified certificates
│   │   ├── Publication.jsx               # Peer-reviewed research spotlight (JARSCT 2025)
│   │   ├── Experience.jsx                # Technical internships & extracurricular activities
│   │   └── Contact.jsx                   # "Let's Build Something Meaningful" & contact channels
│   ├── styles/
│   │   ├── index.css                     # Global tokens, reset, typography, buttons, glassmorphism
│   │   ├── animations.css                # Keyframe pulses, scanlines, custom cursor styles
│   │   ├── visuals.css                   # Project visualizer HUDs, graphs & charts
│   │   └── sections.css                  # Section layouts, grid systems & responsive media queries
│   ├── App.jsx                           # Lenis + GSAP ScrollTrigger root coordinator
│   └── main.jsx                          # React 18 DOM mount
├── package.json
├── vite.config.js                        # Vite config with manual code-splitting chunks
└── README.md
```

---

## ⚙️ How to Update Portfolio Information

All personal details, URLs, project descriptions, skills, and contact settings are centralized in **[`src/data/portfolioData.js`](file:///C:/Users/p/.gemini/antigravity/scratch/prathamesh-portfolio/src/data/portfolioData.js)**.

### 1. Update GitHub Profile & Project Links
Open `src/data/portfolioData.js` and edit:
```javascript
export const personalInfo = {
  ...
  githubUrl: "https://github.com/prathameshtawale", // Replace with your exact GitHub handle
  linkedinUrl: "https://linkedin.com/in/prathameshtawale",
  ...
};
```
For each project in `export const projects`:
```javascript
{
  id: "covid-analysis",
  title: "COVID-19 Data Analysis & BI Dashboard",
  githubUrl: "https://github.com/your-username/covid-19-data-analysis", // Add repository link
  demoUrl: "https://your-demo-url.com", // Add live URL (or leave null)
  ...
}
```

### 2. Replace Your Resume File
- Simply save your latest resume as **`Prathamesh_Tawale_Resume.pdf`** inside the **`public/`** folder.
- The `[Download Resume]` buttons in the Hero and Navbar are wired directly to `/Prathamesh_Tawale_Resume.pdf`!

### 3. Replace Your Profile Photo
- Save your portrait as **`prathamesh_photo.jpg`** in the **`public/`** folder.
- If no image is present, the website automatically falls back to an illuminated monogram (`PT`).

### 4. Toggle Phone Number Visibility
In `src/data/portfolioData.js`:
```javascript
showPhoneInContact: true // Set to true to display phone publicly, or false for privacy
```

### 5. Connecting a Contact Form Service
The contact form currently validates inputs and opens the user's default email client (`mailto:`) with pre-filled subject and body.
To connect a serverless backend without writing server code:
- **Option A (Formspree):**
  1. Register free at [Formspree.io](https://formspree.io/) and create a new form.
  2. In `src/sections/Contact.jsx`, add your Formspree endpoint into the form's `action` or fetch `POST` handler:
     ```javascript
     fetch("https://formspree.io/f/YOUR_FORM_ID", {
       method: "POST",
       headers: { "Content-Type": "application/json" },
       body: JSON.stringify(formData)
     });
     ```
- **Option B (EmailJS):**
  Install `emailjs-com` and call `emailjs.send()` directly from `handleSubmit`.

---

## 🚢 Deployment Guide

### Deploying to Vercel (Recommended)
1. Push your project to a GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "feat: initial portfolio release"
   git branch -M main
   git remote add origin https://github.com/your-username/portfolio.git
   git push -u origin main
   ```
2. Go to [vercel.com](https://vercel.com/) and sign in with GitHub.
3. Click **"Add New..."** -> **"Project"**.
4. Import your `portfolio` repository.
5. Vercel automatically detects **Vite**:
   - **Framework Preset:** Vite
   - **Build Command:** `npm run build`
   - **Output Directory:** `dist`
6. Click **Deploy**. Your portfolio will be live on `https://your-project.vercel.app` with automated HTTPS and global edge CDN caching!

---

### Deploying to Netlify
1. Go to [netlify.com](https://www.netlify.com/) and sign in.
2. Click **"Add new site"** -> **"Import an existing project"** -> **GitHub**.
3. Select your portfolio repository.
4. Set Build Settings:
   - **Base directory:** (leave empty)
   - **Build command:** `npm run build`
   - **Publish directory:** `dist`
5. Click **Deploy site**.

---

## ♿ Accessibility & Performance Features

- **Semantic HTML5:** Full ARIA landmarks, roles, and focus outlines for keyboard navigation.
- **`prefers-reduced-motion`:** Detects user OS accessibility settings to disable 3D orbital animations, complex transitions, and cursor smoothing.
- **Zero Event Blocking:** The 3D canvas is configured with `pointer-events: none` and sits in the background, ensuring smooth scroll and touch interactions across all mobile and desktop devices.
- **Optimized Bundle Chunks:** Three.js and GSAP are modularized into independent chunks via Rollup `manualChunks` to prevent render blocking.
