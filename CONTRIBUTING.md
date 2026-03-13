# Contributing to JSONCraft

Thanks for your interest in contributing to JSONCraft! This project is a browser-based tool that converts JSON into TypeScript, Python, GraphQL, and SQL models — and contributions of all kinds are welcome.

---

## Table of Contents

- [Getting Started](#getting-started)
- [Ways to Contribute](#ways-to-contribute)
- [Development Setup](#development-setup)
- [Project Structure](#project-structure)
- [Submitting a Pull Request](#submitting-a-pull-request)
- [Adding a New Language Generator](#adding-a-new-language-generator)
- [Code Style Guidelines](#code-style-guidelines)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [Code of Conduct](#code-of-conduct)

---

## Getting Started

1. **Fork** the repository on GitHub
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/JSONCraft.git
   cd JSONCraft
   ```
3. Open `index.html` in your browser — no build step or dependencies required.

---

## Ways to Contribute

- 🐛 Fix a bug
- ✨ Add a new language generator
- 🎨 Improve the UI or CSS
- 📝 Improve documentation
- 🧪 Add or improve JSON test cases
- 💡 Suggest ideas via GitHub Issues

---

## Development Setup

JSONCraft has **zero dependencies** and runs entirely in the browser. There is no npm install, no build pipeline, and no bundler.

```
jsoncraft/
├── index.html   ← UI structure
├── style.css    ← Theming, layout, dark/light mode
└── script.js    ← All conversion logic lives here
```

To work on it:

1. Open `index.html` in your browser directly, or use a simple local server:
   ```bash
   npx serve .
   # or
   python3 -m http.server
   ```
2. Edit files and refresh your browser to see changes.

---

## Submitting a Pull Request

1. **Create a branch** from `main` with a descriptive name:
   ```bash
   git checkout -b feature/rust-struct-generator
   # or
   git checkout -b fix/nested-array-detection
   ```
2. **Make your changes** and test them in the browser.
3. **Commit** with a clear message:
   ```bash
   git commit -m "feat: add Rust struct generator"
   ```
4. **Push** to your fork:
   ```bash
   git push origin feature/rust-struct-generator
   ```
5. Open a **Pull Request** against the `main` branch of this repository.
6. Fill in the PR description explaining what you changed and why.

PRs are reviewed as time allows. Please be patient and responsive to feedback.

---

## Adding a New Language Generator

The roadmap includes Go, Rust, Java, Kotlin, Zod, and Prisma. If you'd like to add one:

1. Add a new conversion function in `script.js` following the pattern of existing generators (e.g. `generateTypeScript`, `generatePython`).
2. Add a corresponding button/tab in `index.html`.
3. Handle nested objects and arrays consistently with the existing generators.
4. Test with a variety of JSON inputs including nested objects, arrays, nulls, and mixed types.
5. Note the new language in your PR description.

---

## Code Style Guidelines

- **Vanilla JS only** — no frameworks or libraries. Keep it zero-dependency.
- Use `camelCase` for variables and functions.
- Keep generator functions self-contained and easy to read.
- Comment any non-obvious logic, especially type inference or edge case handling.
- Avoid breaking the dark/light theme toggle when touching CSS.

---

## Reporting Bugs

Open an [Issue](https://github.com/Ghost-Sellz/JSONCraft/issues) and include:

- A description of the problem
- The JSON input that triggered the bug
- The expected output vs. the actual output
- Browser and OS (since this is a browser-based tool)

---

## Suggesting Features

Open an [Issue](https://github.com/Ghost-Sellz/JSONCraft/issues) with the label `enhancement` and describe:

- What you'd like to see added
- Why it would be useful to developers using JSONCraft
- Any examples of expected input/output

---

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). By participating, you agree to uphold a welcoming and respectful environment for everyone.

---

Happy crafting! 🛠️
