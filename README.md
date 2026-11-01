# BlogSpace — Professional Editorial Blogging Platform

> **Share Your Stories with the World.**  
> A modern, responsive, high-craft editorial blogging application developed purely with **HTML5**, **CSS3**, and **Vanilla JavaScript**, featuring zero framework dependencies and robust **LocalStorage** persistence.
>
> **Author:** Minhaz Fahim  
> **Contact:** [minhazfahim442@gmail.com](mailto:minhazfahim442@gmail.com)  
> **Live Demo:** [https://ais-pre-26na4xqefbpyn3udl6krtw-947406464766.asia-east1.run.app](https://ais-pre-26na4xqefbpyn3udl6krtw-947406464766.asia-east1.run.app)

---

## 🌟 Project Overview

**BlogSpace** is an editorial platform designed for independent writers, researchers, and creators. It delivers a fast, accessible, distraction-free reading and writing experience inspired by modern digital publications like Medium, Substack, and The Verge.

The application was architected from the ground up to showcase clean, idiomatic frontend engineering:
- **Semantic HTML5** document outlines and accessibility landmarks (`<header>`, `<main>`, `<article>`, `<nav>`, `<aside>`, `<footer>`).
- **Modern CSS3** custom properties (variables), flexible box layout (Flexbox), CSS Grid, fluid typography, subtle micro-interactions, and comprehensive mobile responsiveness (from 320px mobile to 1440px+ ultra-wide desktop).
- **Vanilla JavaScript (ES6+ Modules)** handling complete state management, data mutations, live DOM rendering, form validations, search & category filtering, and modal dialogs.
- **LocalStorage Data Engine** simulating authentic backend persistence for user accounts, session state, articles, likes, views, and draft/published statuses.

---

## 🚀 Key Features

### 1. Home Feed (`index.html`)
- **Editorial Hero Section:** High-impact typography, tagline, live pulse indicator, and primary calls-to-action.
- **Featured Story Spotlight:** Highlights the flagship editorial piece with high-resolution imagery, reading time, and author credentials.
- **Category Filter Pills:** Interactive filters with dynamic post count badges (`All`, `Technology`, `Design`, `Productivity`, `Culture`, `Business`, `Lifestyle`).
- **Live Instant Search:** Debounced instant keyword search across article titles, descriptions, content body, and author names with clear button.
- **Interactive Story Cards:** Responsive 3-column grid displaying category pill, date, reading time calculation, author avatar, and "Read Article" action.
- **Distraction-Free Article Reader Modal:** Full long-form reading experience with formatted typography, blockquotes, author bio, social share shortcuts, and an interactive **Applaud (Like)** button.
- **Friendly Empty State:** Graceful fallback when search or category yields no matches.
- **Newsletter Subscription:** Simulated email newsletter with input validation and feedback toast notifications.

### 2. Authentication System (`login.html` & `register.html`)
- **Simulated Frontend Auth:** Uses LocalStorage to persist user accounts and current session.
- **Show/Hide Password:** Interactive eye toggle button.
- **Live Password Strength Meter:** Visual meter calculating score (Weak, Fair, Good, Strong) based on length, mixed casing, numbers, and special characters.
- **Form Validation:** Real-time validation for required fields, RFC email format, password matching, and duplicate email prevention.
- **Demo Account Quick-Fill:** One-click button to automatically fill demo credentials (`alex@blogspace.io` / `password123`).
- **Remember Me:** Stores user email in browser storage for subsequent sessions.

### 3. Author Studio Dashboard (`dashboard.html`)
- **Metrics & Analytics:** Real-time statistics cards computing **Total Stories**, **Published Stories**, **Draft Stories**, and **Total Reader Impressions**.
- **User Profile Summary:** Displays current user name, role, avatar, and personalized time-of-day greeting ("Good morning / afternoon / evening").
- **Author Story Table:** Responsive layout displaying story thumbnail, title, category, creation date, reading time, and view count.
- **Live Status Toggle:** Single-click toggle between `Published` (green badge) and `Draft` (amber badge) with instant recalculation of metrics.
- **CRUD Operations:** Preview full article, navigate to edit mode, or delete permanently with a modal confirmation dialog.
- **Responsive Mobile Sidebar:** Off-canvas drawer menu with smooth sliding transition and backdrop overlay.

### 4. Blog Creator & Polish Editor (`create-blog.html`)
- **Dual Mode (Create & Edit):** Dynamically pre-fills existing post data when passed `?id=<post_id>` or initializes a new story.
- **Editorial Inputs:** Title, subtitle/excerpt, category selector, and cover image URL with live preview.
- **One-Click Cover Presets:** Instant image presets for Technology, Design, Workspace, Minimal, Culture, and Strategy.
- **Markdown Formatting Toolbar:** Quick buttons to insert Bold, Italic, Section Heading 2 (`##`), Subsection 3 (`###`), Blockquotes (`>`), Bullet Lists (`-`), and Code snippets (`` `code` ``).
- **Live Word & Read-Time Meter:** Real-time word counter and calculated reading time (`Math.ceil(words / 200)`).
- **Live Preview Tab:** Seamlessly toggle between "Write" mode and "Live Preview" mode to inspect rendered layout before publishing.
- **Draft & Publish Actions:** Save work in progress as private draft or publish live to the home feed.

---

## 🛠️ Technology Stack

| Layer | Technology | Details |
|---|---|---|
| **Structure** | HTML5 | Semantic elements (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`) |
| **Styling** | CSS3 | Custom Properties (variables), Flexbox, CSS Grid, Media Queries, Zero frameworks |
| **Interactivity** | Vanilla JavaScript (ES6+) | Modular architecture (`import` / `export`), async event handlers, DOM manipulation |
| **Persistence** | Browser `localStorage` | Serialized JSON data storage for users, posts, sessions, and interactions |
| **Typography** | Google Fonts | Inter (Weights: 300, 400, 500, 600, 700, 800) |
| **Icons** | Pure SVG | Crisp, inline vector graphics (zero CDN dependencies) |

---

## 📁 Project Structure

```
blogspace/
│
├── index.html              # Home Feed: Hero, Featured, Filters, Grid, Reader Modal
├── login.html              # Login Page: Form validation, password toggle, demo fill
├── register.html           # Register Page: Password strength meter, duplicate check
├── dashboard.html          # Author Dashboard: Metrics, Post management, Status toggles
├── create-blog.html        # Blog Editor: Formatting toolbar, live preview, presets
├── README.md               # Project documentation & GitHub instructions
│
├── css/
│   ├── style.css           # Global design system, typography, header, grid, modal, footer
│   ├── auth.css            # Authentication cards, inputs, strength meter, alerts
│   └── dashboard.css       # Sidebar, stats cards, data table, editor, preview tabs
│
├── js/
│   ├── blog.js             # Core data engine, seed initialization, CRUD, toasts
│   ├── auth.js             # Form validation, session management, password meter
│   ├── dashboard.js        # Metrics calculation, table rendering, delete modal
│   └── main.js             # Homepage controller, search, categories, reader modal
│
├── src/
│   └── utils/
│       ├── blog-logic.ts   # Decoupled core business logic functions
│       └── blog-logic.test.ts # Automated unit tests (Node.js test runner)
│
├── package.json            # Development dependencies & build scripts
└── vite.config.ts          # Multi-page HTML bundler configuration
```

---

---

## 🌐 Deployment & Environments

BlogSpace supports both cloud containerized hosting and local development environments:

| Environment | URL / Port | Purpose |
|---|---|---|
| **Cloud Run Preview** | [ais-pre-26na4xqefbpyn3udl6krtw-947406464766.asia-east1.run.app](https://ais-pre-26na4xqefbpyn3udl6krtw-947406464766.asia-east1.run.app) | Live preview deployment hosted on Google Cloud Run |
| **Local Development** | `http://localhost:3000` | Local Vite development server |

---

## ⚙️ Project Configuration & Environment Setup

### 1. Environment Variables (`.env.example`)
Configuration settings are documented in `.env.example`:
- `APP_URL`: Specifies the application base URL for routing and self-referential links (defaults to `http://localhost:3000`).
- `GEMINI_API_KEY`: Optional slot for Google GenAI / Gemini API key when integrating server-side generative capabilities.

### 2. Platform Capabilities (`metadata.json`)
The application defines its metadata, permissions, and capabilities in `metadata.json`:
- Declares platform capabilities (`MAJOR_CAPABILITY_SERVER_SIDE_GEMINI_API`).
- Outlines application name and editorial description.

### 3. Bundler & Dev Server (`vite.config.ts`)
Configured to bundle all five HTML pages via Rollup multi-page inputs:
- Multi-page entry points: `index.html`, `login.html`, `register.html`, `dashboard.html`, `create-blog.html`.
- Container environment HMR handling: Automatically configures file-watching and hot module reloading based on `DISABLE_HMR` environment settings.

### 4. Dependencies & Extensibility (`package.json`)
- Includes development tools (`tsx`, `typescript`, `vite`) and testing runners.
- Includes `@google/genai` to align with the platform's `MAJOR_CAPABILITY_SERVER_SIDE_GEMINI_API` capability for potential future server-side AI content enhancements.

### 5. Repository Cleanliness (`.gitignore`)
Configured to keep Git repositories clean and focused:
- Ignores build artifacts (`dist/`, `build/`), logs, and `node_modules/`.
- Ignores local environment secrets (`.env*` except `.env.example`).
- Ignores container artifacts (`.aistudio/`) and browser test snapshots (`.playwright-cli/`).

---

## 💻 How to Run Locally

### Prerequisites
- Node.js (version 18 or higher recommended)
- A modern web browser (Chrome, Firefox, Safari, Edge)

### Installation & Execution
1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/blogspace.git
   cd blogspace
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```
   Open your browser and navigate to `http://localhost:3000`.

4. **Run Automated Unit Tests:**
   ```bash
   npm test
   # or: npx --yes tsx --test src/utils/blog-logic.test.ts
   ```

5. **Build for Production:**
   ```bash
   npm run build
   ```
   The compiled, optimized multi-page application will be generated in the `dist/` directory.

---

## 🧪 Testing Checklist & Verification Flow

To evaluate the complete functionality of BlogSpace:

1. **Homepage:**
   - [x] Open `index.html`. Observe default seed articles loaded into LocalStorage.
   - [x] Click on any category filter pill (`Technology`, `Design`, etc.) and verify grid filtering.
   - [x] Type in the search input (e.g., "typography" or "principles") and observe real-time filtering.
   - [x] Click "Read Article" on any card or the featured banner to open the reader modal.
   - [x] Click the "Applaud" (heart) button inside the modal and confirm the like count increments.
   - [x] Test the mobile hamburger navigation on viewports below 768px.

2. **Authentication:**
   - [x] Navigate to `login.html`. Click "Click to Fill Demo Account" and submit.
   - [x] Navigate to `register.html`. Test typing a short password to observe the live strength meter.
   - [x] Register a new user and confirm automatic redirect to the dashboard.

3. **Author Dashboard:**
   - [x] Navigate to `dashboard.html`. Check total, published, and draft statistics.
   - [x] Click on the status badge (`Published` / `Draft`) in any row to toggle its live visibility.
   - [x] Click the "Delete" button and confirm the modal prompt appears before deleting.

4. **Create & Edit Story:**
   - [x] Click "Write New Story" (`create-blog.html`).
   - [x] Enter title, excerpt, select category, and click one of the preset cover chips.
   - [x] Write content using toolbar buttons (Bold, H2, Quotes).
   - [x] Switch to the "Live Preview" tab to inspect rendered markdown.
   - [x] Click "Publish Story" and verify it redirects to dashboard with updated count and shows on the home feed.
   - [x] Click "Edit" on a post from the dashboard, modify content, and save.

---

## 🔒 Limitations of Frontend-Only Authentication

> **Important Disclaimer:**  
> The authentication and user management system implemented in this application is strictly a **frontend demonstration simulation** utilizing browser `localStorage`.
>
> - **No Server-Side Verification:** Passwords and user sessions are stored locally in the browser. In production, password hashing (e.g. bcrypt, Argon2) and secure HTTP-only cookie-based JWT or OAuth sessions on a backend server are required.
> - **Client-Side Persistence:** Clearing browser cache or switching devices/browsers will reset or segregate the stored data.
> - **Educational Scope:** This project fulfills the design, architectural, and JavaScript programming requirements of a frontend engineering assignment without relying on external backend services.

---

## 🔮 Future Improvements

- [ ] Dark Mode / Light Mode theme toggle with `prefers-color-scheme` persistence.
- [ ] Commenting system allowing reader replies under published stories.
- [ ] Export stories to Markdown (`.md`) or PDF.
- [ ] Image drag-and-drop file upload using FileReader API.
- [ ] Integration with a production headless CMS or REST/GraphQL backend.

---

## 📤 GitHub Submission Instructions

To push this project to your GitHub profile:

1. Initialize git in the root folder:
   ```bash
   git init
   git add .
   git commit -m "feat: complete BlogSpace responsive blogging platform"
   ```
2. Create a new repository on [GitHub](https://github.com/new) named `blogspace`.
3. Link and push your local repository:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<your-username>/blogspace.git
   git push -u origin main
   ```
4. Optional: Enable **GitHub Pages** under repository settings (`Settings > Pages > Deploy from branch: main / root`) for live hosting!

---

*Crafted with passion, meticulous typography, and modern web standards by Minhaz Fahim.*
