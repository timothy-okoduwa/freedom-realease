<div align="center">

# ⚡ freedom

### **Your Day Runs Itself.**

An automatic execution engine built for high-agency builders.  
Plan once, press start, and let your day run itself.

[![Version](https://img.shields.io/badge/version-v3.8.0-7C3AED?style=for-the-badge)](https://usefreedom.top/changelog)
[![100% Free](https://img.shields.io/badge/pricing-100%25%20free-1FAE6B?style=for-the-badge)](https://usefreedom.top/download)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Windows-2F6FED?style=for-the-badge)](https://usefreedom.top/download)
[![License: MIT](https://img.shields.io/badge/license-MIT-black?style=for-the-badge)](LICENSE)

<br />

<img src="apps/web/public/screenshots/dashboard.png" alt="Freedom Desktop Execution Suite" width="100%" style="border-radius: 14px; box-shadow: 0 20px 50px rgba(0,0,0,0.15);" />

</div>

---

```
   █▀▀ █▀█ █▀▀ █▀▄ █▀█ █▀▄▀█
   █▀  █▀▄ ██▄ █▄▀ █▄█ █░▀░█
```

Most productivity tools force you to micro-manage them. You end up spending more time organizing cards and dragging boards than actually executing deep work. 

**Freedom** changes that. It takes your planned schedule, task queue, and break intervals, turning them into a calm, floating execution engine on macOS and Windows that removes decision fatigue and protects your focus rhythm.

---

## ✨ Features

### 🧠 Prompt-to-Plan Day Planner & Voice Dictation
Turn unstructured brain-dumps, messy task lists, and natural spoken voice memos into structured, chronological day timelines with automatic duration buffers and tags powered by Gemini multimodal intelligence.

<img  alt="plan-builder-prompt" src="https://github.com/user-attachments/assets/1a6f1c9f-a204-4cc5-bf40-0ee963606cc4" width="100%" style="border-radius: 12px; margin: 12px 0;" />


### 🎯 Global Crosshair Screen Snipping (`Ctrl + Option + Space`)
Hit the system shortcut from any workspace. Freeze-frame and crop Jira tickets, GitHub PRs, Figma artboards, or Slack conversations to instantly synthesize them into concrete queue tasks with visual source screenshots attached.

### 🔄 The Day Recovery Engine (Schedule Re-balancer)
When meetings run 45 minutes over or emergencies derail your morning, click **“Recover My Day”** to intelligently push non-critical tasks to backlog, protect focus blocks, and restore realistic completion milestones without guilt.


<img  alt="day-recovery-engine" src="https://github.com/user-attachments/assets/50766ba4-4650-4d05-9da5-a17ecb649660" width="100%" style="border-radius: 12px; margin: 12px 0;"/>


### 💊 Floating Pill Capsule HUD
Stays pinned on top of all virtual desktops and full-screen windows (VS Code, Figma, browser). Single-click to view active task; double-click to expand full dashboard; drag anywhere across displays. Quick duration adjusters (`+10m`, `-10m`, custom time) keep you in flow.

### 🎙️ Hands-Free Voice HUD with Multi-Action Chaining
Floating dynamic HUD supporting continuous speech recognition, multi-command chaining (e.g. *“add 10 minutes and resume timer”*), and accent-tolerant fuzzy parsing resilient to homophones.

### ✍️ Standup & Retro Ghostwriter (4 Agile Tones)
Converts your day’s real execution logs into crisp, bulleted updates formatted specifically for **Slack**, **Discord**, **Sprint Retro**, or **Executive** summaries with 1-click clipboard export.

### 📊 Planning Fallacy Moat & Historical Calibration
Tracks actual time spent vs. initial estimates across categories. Generates calibrated multiplier badges (e.g., `1.4x typical overrun on Backend API`) so future AI day plans automatically absorb your genuine velocity.

### 📈 365-Day Consistency Heatmap & Objective Score
Objective algorithm measuring planning accuracy alongside completion, outputting a transparent 0–100 score dial and an edge-safe GitHub-style activity matrix with streak protection.


<img alt="v2 5 0-heatmap" src="https://github.com/user-attachments/assets/7b9b9430-59a4-4fe7-ab0e-eea6a7affb4b" width="100%" style="border-radius: 12px; margin: 12px 0;"/>

### 🎵 Distraction Shield & Ambient Audio Engine
Integrated music player with curated flow tracks (*Ninajirachi — iPod Touch*, *Mizmo — Hello*) selectable directly from the status bar menu.

### 🍎 Native Apple HIG & Status Bar Integration
Crafted strictly following Apple Human Interface Guidelines: native squircle dock icons, adaptive monochrome menu bar template items for Dark and Light appearances, and instant tray controls.

---

## ⌨️ System Shortcuts

| Shortcut | Action | Scope |
| :--- | :--- | :--- |
| `Ctrl + Option + Space` | **Global Screen Snipping & Task Synthesizer** | System-Wide (macOS & Windows) |
| `Cmd + K` / `Ctrl + K` | **Command Palette / Quick Navigation** | In-App |
| `Space` | **Toggle Pause / Resume Active Task** | In-App |
| `Cmd + .` / `Ctrl + .` | **Skip Current Task to Next Queue Item** | In-App |

---

## 📥 Download & Quick Start

### 1. Download
Get the official v3.8.0 release:
- 🍏 **[Download Freedom for macOS (Apple Silicon & Intel DMG)](https://usefreedom.top/download)**
- 🪟 **[Download Freedom for Windows (Setup EXE)](https://usefreedom.top/download)**
- 📦 Direct releases also available on **[GitHub Releases](https://github.com/timothy-okoduwa/freedom-realease/releases)**.

### 2. macOS First-Run ("App is Damaged" / Unidentified Developer)
Because Freedom is an open-source indie build without a commercial Apple Developer certificate, macOS Sequoia and Sonoma flag web downloads with a quarantine attribute.

If macOS says *"Freedom is damaged and cannot be opened"*, run this 5-second fix in **Terminal**:

```bash
xattr -cr /Applications/Freedom.app
```

*(Alternative if administrator permission required: `sudo xattr -rd com.apple.quarantine /Applications/Freedom.app`)*

Then double-click **Freedom.app** in your Applications folder to launch! 🎉

---

## 🛠️ Architecture & Monorepo Structure

Freedom is engineered as a high-performance TypeScript monorepo powered by **Turborepo**, **Electron**, **Next.js 14**, **Tailwind CSS**, and **Zustand**.

```
freedom/
├── apps/
│   ├── desktop/      # Electron app + floating capsule HUD + screen snipping agent
│   │   ├── main/     # Main process: global shortcuts, tray, native windowing
│   │   └── renderer/ # React dashboard: plan builder, execution engine, HUD
│   └── web/          # Next.js 14 landing page, changelog, trust & download portal
└── packages/
    ├── ui/           # Shared Apple-inspired design system & components
    └── config/       # Shared TypeScript & Tailwind configurations
```

### Local Development Setup

```bash
# 1. Clone the repository
git clone https://github.com/timothy-okoduwa/freedom-realease.git
cd freedom

# 2. Install dependencies
pnpm install

# 3. Run development servers (Web on :3005 + Electron desktop)
pnpm dev

# Or run individual applications:
pnpm --filter @freedom/web dev      # Runs Next.js web application
pnpm --filter @freedom/desktop dev  # Runs Electron desktop application
```

### Building Release Packages

```bash
# Package universal macOS DMG:
pnpm --filter @freedom/desktop dist:mac

# Package Windows installer:
pnpm --filter @freedom/desktop dist:win
```

---

## 🤝 Contributing

We welcome contributions from builders, designers, and hackers!  
Feel free to open an issue or submit a pull request on [GitHub](https://github.com/timothy-okoduwa/freedom-realease).

---

## 📜 License

[MIT License](LICENSE) © 2026 Timothy Okoduwa & Freedom Contributors. Built for high-agency builders.
