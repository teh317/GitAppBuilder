# Universal-Multi-Platform-App-Builder-For-GIthub-Actions
Package Web Builds from No Code Apps into actual Native Packages easily for Android, Windows and Mac through Github Actions!

# 🚀 Universal Multi-Platform App Builder

Turn any web application (**Vite, React, Vue, Svelte, Next.js, Solid**) into native **Android (.apk)**, **Windows (.exe)**, and **macOS (.dmg)** production packages using a single, unified GitHub Actions workflow.

No local Android Studio setups, no native macOS/Windows machine dependencies, and **zero manual Rust configuration required.**

---

## ✨ Why This Exists (and why it's different)

Usually, turning a web app into native desktop and mobile versions requires maintaining separate codebases, heavy wrappers, or massive configuration files. 

This repository provides a **headless, zero-resistance template** that builds your native apps on the fly inside GitHub's cloud runners. It automatically:
*   **Scaffolds Tauri v2** setups dynamically on the runner so you don't have to commit complex Rust boilerplate to your repo.
*   **Injects mobile responsive viewports** to ensure desktop layouts look flawless on mobile screens.
*   **Converts a single image asset** (`logo.png` or `icon.png`) into all required native platforms formats (`.ico`, `.icns`, and Android asset maps) automatically.
*   **Syncs your app version** directly with your project's root `package.json`.

---

## 🛠️ How to Use (Plug & Play)

Getting your cross-platform pipeline up and running takes less than two minutes.

### 1. Copy the Workflow
Create a new file in your repository at `.github/workflows/build.yml` and paste the contents of the `build.yml` file found in this repository.

### 2. Customize Two Lines
At the very top of the file, update the configuration zone with your application's metadata:

```yaml
# ==========================================
# 🎛️ CONFIGURATION ZONE
# ==========================================
env:
  APP_NAME: "YourAppName"            # The name of your executable/app
  APP_ID: "com.yourcompany.app"      # Your unique reverse-DNS bundle identifier
