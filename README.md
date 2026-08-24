# DeCloakedBrowser

**A cracked CloakBrowser Pro v151 that allows unlimited sessions.**

## What is this?

CloakBrowser is a Chromium-based multi-accounting tool that lets you run many independent browser sessions from a single binary. This repo contains a **pro (paid) build that's been cracked** — you get the full Pro feature set, including **unlimited sessions**, without any license restrictions.

## Contents

| Path | Size | Description |
|---|---|---|
| `cloakbrowser-pro-v151-free/` | 760 MB | Full extracted browser package |
| `README.md` | — | This file |

The `.zip` file is still present but not tracked in git — it's kept as a convenient download.

## Quick start

```bash
# 1. Clone (files are already extracted)
git clone https://github.com/DeCloaked/DeCloakedBrowser.git
cd DeCloakedBrowser

# 2. Launch the browser
./cloakbrowser-pro-v151-free/chrome

# 3. (Optional) Launch with a custom user-data-dir for a dedicated session
./cloakbrowser-pro-v151-free/chrome --user-data-dir=./session1

# 4. Headless mode (no display server required)
./cloakbrowser-pro-v151-free/chrome --headless --no-sandbox
```

## Key flags

| Flag | What it does |
|---|---|
| `--user-data-dir=<path>` | Isolated session profile (cookies, storage, extensions) |
| `--headless` | Run without a display — perfect for servers / Docker |
| `--no-sandbox` | Required when running as root or in containers |
| `--window-size=1920,1080` | Set initial window dimensions |
| `--disable-gpu` | Disable GPU acceleration (helps in headless / container envs) |

## Unlimited sessions

Because this is a cracked Pro build, you can run **any number of concurrent sessions** — just launch separate `chrome` processes with different `--user-data-dir` paths:

```bash
# Session A
./cloakbrowser-pro-v151-free/chrome --user-data-dir=./session-a --remote-debugging-port=9222

# Session B (in another terminal)
./chrome --user-data-dir=./session-b --remote-debugging-port=9223

# Session C (in yet another terminal)
./chrome --user-data-dir=./session-c --remote-debugging-port=9224
```

Each session has its own:
- Cookies & local storage
- Extensions & settings
- Fingerprint (fingerprinting is per-profile)

## Linux

The extracted `chrome` binary is Linux-compatible (linux-x64) with all required `.so` shared libraries (libGLESv2, libvulkan, etc.) included. Works on most modern Linux distros without additional dependencies.

## File structure

Extracted directory layout:

```
cloakbrowser-pro-v151-free/
├── chrome                   # Main binary (~514 MB)
├── chrome_crashpad_handler  # Crash reporting
├── icudtl.dat               # ICU unicode data
├── v8_context_snapshot.bin  # V8 JS engine snapshot
├── resources.pak             # Bundled resources
├── *.pak                     # Localized / resource bundles
├── snapshot_blob.bin         # V8 snapshot blob
├── vk_swiftshader_icd.json   # Vulkan SwiftShader config
└── locales/                  # UI localization files
```

## Version

**CloakBrowser Pro v151** — cracked / freeware

## Repository

This repo tracks 671 files directly — **Git LFS** handles the heavy binaries (chrome, chromedriver, shared libraries) to keep history lean. Clone includes everything via LFS.

## License

Cracked for unlimited use. No license key or phone-home required.
