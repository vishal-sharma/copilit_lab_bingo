# 🎱 Bingo Mixer

> **A social icebreaker game — and a hands-on GitHub Copilot Agent workshop all in one.**

Find people who match the squares, get 5 in a row, and shout **BINGO!** ✨  
Then use this very repo to level up your AI-assisted development skills with VS Code Agent Mode.

<div align="center">

[![Play Now](https://img.shields.io/badge/▶%20Play%20Now-GitHub%20Pages-blue?style=for-the-badge)](https://vishal-sharma.github.io/copilit_lab_bingo/)
[![Lab Guide](https://img.shields.io/badge/📚%20Lab%20Guide-Workshop-green?style=for-the-badge)](workshop/GUIDE.md)
[![Open in Codespaces](https://img.shields.io/badge/Open%20in-Codespaces-black?style=for-the-badge&logo=github)](https://codespaces.new/vishal-sharma/copilit_lab_bingo)

</div>

---

## 🕹️ How to Play

```
┌───────────────────────────────────────┐
│  🎯  5×5 board · 24 questions + FREE  │
│                                       │
│  1. Find someone who matches a square │
│  2. Mark it off                       │
│  3. Get 5-in-a-row → BINGO! 🎉        │
└───────────────────────────────────────┘
```

Perfect for **team mixers**, **conferences**, and **onboarding events**.  
Questions like *"bikes to work"*, *"speaks 3+ languages"*, or *"has a hidden talent"* — every card is unique!

---

## 🤖 Workshop: GitHub Copilot Agent Lab

This repo doubles as a **hands-on lab** for VS Code Agent Mode + GitHub Copilot.  
You'll engineer context, design UIs, create custom agents, and build features with TDD — all AI-assisted.

| Part | Title | What You'll Do |
|:----:|-------|----------------|
| [**00**](workshop/00-overview.md) | Overview & Checklist | Get oriented and set up |
| [**01**](workshop/01-setup.md) | Setup & Context Engineering | Onboard AI to your codebase |
| [**02**](workshop/02-design.md) | Design-First Frontend | Redesign the UI with creative themes |
| [**03**](workshop/03-quiz-master.md) | Custom Quiz Master | Build your own quiz theme agent |
| [**04**](workshop/04-multi-agent.md) | Multi-Agent Development | TDD + design agents working together |

> 📝 All guides are available in the [`workshop/`](workshop/) folder for offline reading.

---

## ⚡ Quick Start

### Option A — GitHub Codespaces (zero setup)

[![Open in Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/vishal-sharma/copilit_lab_bingo)

A fully configured dev environment spins up in your browser. No installs needed.

### Option B — Run locally

**Prerequisites:** [Node.js 22+](https://nodejs.org/)

```bash
npm install
npm run dev      # → http://localhost:5173
```

### Option C — VS Code Dev Container

Clone the repo, then run **Dev Containers: Reopen in Container** — everything is pre-configured.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 19 + TypeScript 5.9 (strict) |
| Build | Vite 8 |
| Styling | Tailwind CSS v4 (CSS-first `@theme`) |
| Tests | Vitest 4 + Testing Library |
| Lint | ESLint 9 |
| Deploy | GitHub Pages (auto on push to `main`) |

---

## 🏗️ Build & Deploy

```bash
npm run build    # TypeScript + Vite production build
npm run test     # Run all tests
npm run lint     # Check code style
```

Pushes to `main` automatically deploy to **GitHub Pages** via GitHub Actions.

---

## 🤝 Contributing

Found a bug or have a fun new question idea?  
Check [CONTRIBUTING.md](CONTRIBUTING.md) and open a PR — contributions are welcome!

---

<div align="center">
  Made with ☕ and 🤖 · <a href="workshop/01-setup.md">Start the lab →</a>
</div>
