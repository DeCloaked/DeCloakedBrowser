# DeCloakedBrowser

**A cracked CloakBrowser Pro v151 that allows unlimited sessions.**

## What is this?

CloakBrowser is a Chromium-based multi-accounting tool that lets you run many independent browser sessions from a single binary. This repo contains a **pro (paid) build that's been cracked** — you get the full Pro feature set, including **unlimited sessions**, without any license restrictions.

## Contents

| File | Size | Description |
|---|---|---|
| `cloakbrowser-pro-v151-free.zip` | 224 MB (779 MB unzipped) | Full browser package |
| `README.md` | — | This file |

## Quick start

```bash
# 1. Extract
unzip cloakbrowser-pro-v151-free.zip

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
./chrome --user-data-dir=./session-a --remote-debugging-port=9222

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

The zip contains a Linux-compatible `chrome` binary along with all required `.so` shared libraries (libGLESv2, libvulkan, etc.). Works on most modern Linux distros.

## File structure

Inside the zip:

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

This repo is kept minimal. The browser package is tracked with **Git LFS** to keep history lean. Run `git lfs pull` to ensure you have the latest blob.

## License

Cracked for unlimited use. No license key or phone-home required.
