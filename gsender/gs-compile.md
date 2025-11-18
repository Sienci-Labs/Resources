---
title: Compile gSender
menu_order: 3
post_status: publish
post_excerpt: Full instructions and troubleshooting for building gSender from its open-source code.
post_date: 2025-10-14 14:48:30
taxonomy:
    knowledgebase_cat: gs-ex
    knowledgebase_tag:
        - gsender
custom_fields:
    KBName: gSender
    basepress_post_icon: bp-caret-right
skip_file: no
---

This guide provides comprehensive instructions on how to compile gSender from its source code for various operating systems, including Windows, macOS (Intel & Apple Silicon), and Linux (including Raspberry Pi). Building from source allows you to <a href="#contributing">contribute to development</a>, test experimental features, or customize the application for your specific needs.

**Note:** This guide is intended for users with some familiarity with command-line interfaces and software development environments. If you are looking to simply install gSender, please refer to the [gSender Installation Guide](https://resources.sienci.com/view/gs-installation/).

## Prerequisites

Before you begin, ensure you have the following software installed on your system. **Version numbers are critical for Node.js and Yarn.**

### 1. Git

Git is essential for cloning the gSender repository.

* **Windows:** [https://git-scm.com/downloads](https://git-scm.com/downloads)
* **macOS:**
  * Install via Homebrew:
    ```bash
    brew install git
    ```
  * Or download directly from [https://git-scm.com/downloads](https://git-scm.com/downloads)
* **Linux:**
    ```bash
    sudo apt-get install git
    ```

### 2. Node.js, npm (Node Package Manager) and Yarn

gSender is a JavaScript/TypeScript application. Node.js and its package manager (npm) are crucial.

* **Recommended Version:** gSender is built using **Node.js version 20.x**.

* **Windows Installation:**
  * Download and install Chocolatey:
    ```powershell
    powershell -c "irm https://community.chocolatey.org/install.ps1|iex"
    ```
  * Download and install Node.js:
    ```powershell
    choco install nodejs --version="20.19.5"
    ```
  * Verify the Node.js version:
    ```powershell
    node -v
    ```
    Should print "v20.19.5".
  * Download and install Yarn:
    ```powershell
    corepack enable yarn
    ```
  * Verify Yarn version:
    ```powershell
    yarn -v
    ```

* **macOS Installation:**
  * Download and install nvm:
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
    ```
  * Source the shell (in lieu of restarting):
    ```bash
    \. "$HOME/.nvm/nvm.sh"
    ```
  * Download and install Node.js:
    ```bash
    nvm install 20
    ```
  * Verify the Node.js version:
    ```bash
    node -v
    ```
    Should print "v20.19.5".
  * Download and install Yarn:
    ```bash
    corepack enable yarn
    ```
  * Verify Yarn version:
    ```bash
    yarn -v
    ```

* **Linux Installation:**
  * Download and install nvm:
    ```bash
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
    ```
  * Source the shell:
    ```bash
    \. "$HOME/.nvm/nvm.sh"
    ```
  * Download and install Node.js:
    ```bash
    nvm install 20
    ```
  * Verify the Node.js version:
    ```bash
    node -v
    ```
    Should print "v20.x.x".
  * Download and install Yarn:
    ```bash
    corepack enable yarn
    ```
  * Verify Yarn version:
    ```bash
    yarn -v
    ```

### 3. Python

Python is often required for Electron's native module compilation (via `node-gyp`).

* **Recommended Version:** Python 3.x is generally expected.

* **Windows Installation:**
  * [Download Python](https://www.python.org/downloads/)
  * Ensure Python is added to your system's PATH during installation.

* **macOS Installation:**
  * Python 3 is typically pre-installed or easily installed via Homebrew.
  * Install `setuptools`:
    ```bash
    sudo -H pip install setuptools
    ```

* **Linux Installation:**
  * [Download Python](https://www.python.org/downloads/) (or use your system's package manager like `sudo apt-get install python3`)

### 4. C++ Compiler & Build Tools

These tools are necessary for compiling native Node.js modules that gSender and its dependencies rely on. The CI workflow explicitly adds `node-gyp` globally.

* **Windows:**
  * Run `npm install --global --production windows-build-tools` to set up necessary tools.
* **macOS:**
  * Install **Xcode Command Line Tools**:
    ```bash
    xcode-select --install
    ```
  * Ensure `setuptools` for Python is installed:
    ```bash
    sudo -H pip install setuptools
    ```
  * **For Apple Silicon (M1/M2/M3 chips):**
    * While Node.js and Electron increasingly support ARM64 natively, some older native modules might still require Rosetta 2. If you face persistent `node-gyp` errors, try running your terminal via Rosetta (Right-click Terminal.app -> Get Info -> "Open using Rosetta"). However, aim for native `arm64` builds if possible.
    * A crucial step often overlooked is ensuring that `node-gyp` has the correct path to the Python executable, especially if you have multiple Python versions. Setting `export PYTHON=/usr/bin/python3` or similar can help.
* **Linux (and Raspberry Pi):**
  * Install **`build-essential`**:
    ```bash
    sudo apt update
    sudo apt install build-essential git libusb-1.0-0-dev pkg-config libudev-dev libgtk-3-dev
    ```
    * `libudev-dev` and `libgtk-3-dev` are crucial for compiling certain native modules on Linux.
  * **Raspberry Pi / Debian-based systems:** You will likely need additional runtime libraries for Electron to run correctly, especially on headless or minimal installations.
    * `libappindicator3-1`: This is a common missing dependency used by gSender.
    ```bash
    sudo apt install libappindicator3-1
    ```
    * Other common Electron dependencies:
    ```bash
    sudo apt install libgconf-2-4 libnss3 libasound2 libsecret-1-0 libgtk-3-0
    ```
  * **Architecture considerations (Raspberry Pi):** gSender is typically built for `arm64` (AArch64). If you are on an older Raspberry Pi OS (like `armhf` on 32-bit systems) or a different ARM architecture, you might encounter issues. Modern Raspberry Pi OS (64-bit) is strongly recommended for native compilation. Cross-compilation is generally not well-supported and can be problematic as reported in community forums.

---

## Cloning the Repository

First, you need to get the gSender source code.

1. Open your terminal or command prompt.
2. Navigate to the directory where you want to store the gSender project.
3. Clone the repository and enter the directory:
    ```bash
    git clone https://github.com/Sienci-Labs/gsender.git
    cd gsender
    ```

---

## Installing Dependencies

Once the repository is cloned, install the project's dependencies using Yarn.

1. **Clean previous builds (optional but recommended):**
    The `package.json` script `prepare` runs `npm run clean`.
    ```bash
    yarn prepare
    ```
    This command typically cleans out old build artifacts (`./dist` and `./output` directories) and prepares the environment.
2. **Install main dependencies:**
    ```bash
    yarn install
    ```
    This command downloads and installs all required Node.js packages as defined in `package.json` and `yarn.lock`. This step can take some time and may compile native modules.

---

### Development Workflow

These commands are ideal for active development, offering features like hot-reloading for faster iteration.

1. **Run in Development Mode (Hot Reloading):**
    ```bash
    yarn dev
    ```
    This launches the local development server. Please open gSender in your browser at [http://localhost:8000](http://localhost:8000).
    Any changes you make to the source code will automatically reload.
2. **Clean previous builds (optional but recommended):**
    ```bash
    yarn clean
    ```
    Removes old build artifacts and prepares a clean environment for a fresh build.

---

### Production / Release Build Workflow

These commands are used to create optimized, distributable versions of gSender for your operating system.

1. **Build the Production Application:**
    ```bash
    yarn build
    ```
    This compiles the app for production into the `dist` directory.
    It includes minification and optimization suitable for release.
2. **Build OS-specific Packages:**
   * `yarn build:windows`
   * `yarn build:macos`
   * `yarn build:linux`
    Each command produces a platform-specific package (e.g., `.exe`, `.dmg`, `.AppImage`, or `.deb`).
3. **Build Electron Package (Cross-platform builder):**
    ```bash
    yarn electron-builder
    ```
    Uses [Electron Builder](https://www.electron.build/) to create a standalone installer.
    The output (e.g., `.exe`, `.dmg`, `.AppImage`, `.zip`) will appear in the `output/` folder.

---

### Raspberry Pi (ARM) Specific Build

The gSender's CI has a dedicated job for building Raspberry Pi packages, which uses a Docker-based approach for consistency and environment control. **For Pi 5 and other 64-bit Raspberry Pi models, native ARM64 compilation is the recommended approach over cross-compilation.**

1. **Inspect the Pi Build Script:** The CI executes `scripts/build-pi.sh`. It's recommended to examine this script and the associated `DockerfilePi` in the project root for the most accurate and up-to-date instructions for building on a Raspberry Pi.
2. **Using Docker (Recommended for Pi):**
    If you have Docker installed on your Raspberry Pi or a cross-compilation environment, you can use the provided Docker setup (ensuring you are in the gSender root directory):
    ```bash
    ./scripts/build-pi.sh
    ```
    This script will build a Docker image and then use it to compile gSender for the Raspberry Pi's ARM architecture. This approach helps encapsulate all dependencies and ensures a reproducible build environment.
3. **Native Compilation on Raspberry Pi (64-bit OS):**
    If you choose to compile directly on a Raspberry Pi running a 64-bit OS (e.g., Raspberry Pi OS (64-bit)), follow the general Linux instructions, ensuring all prerequisites (especially Node.js 20.x `arm64` and the `apt install` dependencies) are met. Some users have successfully compiled on Pi 5 by following these steps.
   * Verify your Node.js architecture: `node -p "process.arch"` should output `arm64`.
   * Ensure all necessary dev libraries are installed: `sudo apt update && sudo apt install build-essential git libusb-1.0-0-dev pkg-config libudev-dev libgtk-3-dev libappindicator3-1 libgconf-2-4 libnss3 libasound2 libsecret-1-0 libgtk-3-0`

---

## Common Troubleshooting

Here are some common issues you might encounter when compiling gSender locally, along with potential solutions, drawing from community experiences and CI practices. If you can't find your particular issue, you can always reach out in our <a href="https://forum.sienci.com/c/gsender/" target="_blank" rel="noopener">Community Forum</a> or <a href="https://github.com/Sienci-Labs/gsender/issues" target="_blank" rel="noopener">GitHub</a> or **try these general debugging steps**:

* **Read Error Messages Carefully:** The error messages often contain clues about the root cause.
* **Search for Specific Errors:** Copy and paste unique error messages into a search engine (or the [Sienci Labs Forum](https://forum.sienci.com/)) to find known solutions.
* **Check GitHub Issues:** Review the gSender GitHub repository's issues page for similar problems, especially those tagged "build issue."
* **Start Fresh:** If you're stuck, delete the entire `gsender` directory, re-clone, and follow the steps from the beginning.
* **Docker:** If you continue to have environment issues, consider using Docker for a consistent build environment, similar to how Sienci Labs builds their releases, especially for Linux/ARM targets.

### `bash` Command Not Found on Windows

* **Problem:** When running `yarn` commands (e.g., `yarn run dev`, `yarn clean`, `yarn prepare`), you may see an error like `'bash' is not recognized as an internal or external command, operable program or batch file.`  
    This occurs because several `package.json` scripts invoke `bash -c "..."`, which isn’t supported natively in Windows Command Prompt or PowerShell.

* **Solution:**
  * **Run from Git Bash (Recommended):**  
        The easiest and most reliable solution is to use the **Git Bash** terminal that comes with [Git for Windows](https://git-scm.com/download/win).  
        Open **Git Bash** (search for it in your Start Menu) and execute all `yarn` and other `gSender` commands referenced in this documentation, from within that terminal. This ensures full compatibility with commands used in the build scripts
  * **Add Git to System PATH (Advanced):**  
        If you prefer using PowerShell or Command Prompt, you can make `bash` available system-wide:
        1.  Search for "Environment Variables" in the Start Menu and select **Edit the system environment variables**.  
        2.  Click **Environment Variables...** → under **System variables**, find and edit `Path`.  
        3.  Add a new entry:  
            `C:\Program Files\Git\bin`  
            (or your actual Git install path).  
        4.  Save your changes and **restart your terminal**.  
        After this, `bash` should work in PowerShell or CMD.
  * **Use Windows Subsystem for Linux (WSL):**  
        For a full Linux-like environment, you can install [WSL](https://learn.microsoft.com/en-us/windows/wsl/install) and a distribution such as Ubuntu, then clone and build gSender entirely from there.

![](/_images/_gsender/_compile/gs_co_compile-path-bash.png){.aligncenter .size-medium}

### Node.js / Yarn Version Mismatches or Corrupted Installs

* **Problem:** Errors during `yarn install` related to package resolution, `node-gyp`, or general build failures.
* **Solution:**
  * **Check Node.js Version:** Ensure you are using **Node.js 20.x** as specified. Use `node -v` and `nvm ls` (if using nvm). If incorrect, switch using `nvm use 20`. Some community guides for Raspberry Pi may suggest Node.js 18.x, but the official CI uses 20.x.
  * **Check Yarn Version:** Ensure you are using `yarn@1.22.22`. Install globally with `npm install --global yarn@1.22.22`.
  * **Clear Caches:**
    ```bash
    yarn cache clean
    npm cache clean --force
    ```
  * **Clean and Reinstall:**
    ```bash
    rm -rf node_modules yarn.lock package-lock.json
    yarn install
    ```

### Native Module Compilation Errors (`node-gyp`)

This is a very common source of issues, often manifesting as errors during `yarn install` or `yarn build` that mention `node-gyp`, Python, or C++ compilers.

* **Problem:** `gyp ERR! build error`, `Could not find any Visual Studio installation`, `Command 'python' not found`, etc.
* **Solution:**
  * **Ensure C++ Build Tools are Installed:** Refer to "C++ Compiler & Build Tools" in the Prerequisites section for your operating system.
    * **Windows:** Verify Visual Studio Build Tools and potentially `vcredist2017` are installed.
    * **macOS:** Ensure Xcode Command Line Tools are installed (`xcode-select --install`) and `pip install setuptools` has been run. If you have multiple Python versions, explicitly set the `PYTHON` environment variable to point to Python 3 (e.g., `export PYTHON=/usr/bin/python3`) before running `yarn install` or `electron-rebuild`.
    * **Linux:** Make sure `build-essential`, `libudev-dev`, and `libgtk-3-dev` are installed (`sudo apt install build-essential libudev-dev libgtk-3-dev`).
  * **Python Path:** Ensure Python 3.x is installed and correctly added to your system's PATH. On some systems, you might need to explicitly link `python` to `python3`.
  * **Rebuild Electron Native Modules:** Sometimes, modules need to be explicitly rebuilt against your specific Electron version.
    ```bash
    yarn run electron-rebuild
    ```
  * **macOS Apple Silicon (M1/M2/M3) Specific:** If you still face issues with native modules after confirming Node.js `arm64` and `xcode-select`, consider deleting `node_modules` and `yarn.lock`, then reinstalling. If `node-gyp` struggles, ensure Python 3 is properly set up and linked. Sometimes, trying to build within a terminal running under Rosetta 2 (if you're having trouble with an `arm64` native module) can be a temporary workaround, though native ARM64 is preferred.

### `yarn prepare` / Native Dependency Issues

* **Problem:** The `yarn prepare` command (which runs `npm run clean` and potentially `prebuild-latest`) fails, or after running it, you still get runtime errors like "Cannot find module..." for native dependencies (e.g., `@serialport/bindings`). This is a common build issue.
* **Solution:**
  * **Ensure `yarn prepare` completed successfully:** This step is crucial for copying prebuilt or compiled native modules to the correct location for Electron. If it failed, review the output for specific errors related to permissions, missing files, or compilation failures.
  * **Manual Copying (Workaround):** In rare cases, the script might not correctly copy the compiled native modules to the expected Electron `dist` directory. Verify that the `gsender/src/node/modules` directory (which holds prebuilt binaries for certain dependencies) exists and its contents are correctly placed in your build output.

### Missing `libappindicator3-1` and other Electron Runtime Dependencies (Linux / Raspberry Pi)

* **Problem:** On minimal Linux installations (like some Raspberry Pi OS variants or older Pi OS versions like Raspberry Pi 4 (2GB)), gSender might fail to launch with errors related to `libappindicator3-1` or other GTK/UI libraries. This is a frequently reported issue on Raspberry Pi.
* **Solution:** Install the missing libraries as outlined in the "Prerequisites - Linux" section:
    ```bash
    sudo apt update
    sudo apt install libappindicator3-1 libgconf-2-4 libnss3 libasound2 libsecret-1-0 libgtk-3-0
    ```

### Architecture Mismatches and Raspberry Pi Specifics

* **Problem:** Issues running gSender on Raspberry Pi or other ARM devices, especially older ones, due to incorrect architecture (e.g., 32-bit `armhf` vs. 64-bit `arm64`). Cross-compilation is often problematic.
* **Solution:**
  * **Use 64-bit OS:** For Raspberry Pi 3/4/5 and other compatible ARM devices, use a 64-bit operating system (e.g., Raspberry Pi OS (64-bit)). gSender is typically built for `arm64`.
  * **Native Compilation:** Focus on compiling directly on the ARM64 device rather than attempting cross-compilation, which often leads to errors.
  * **Consult `scripts/build-pi.sh` and `DockerfilePi`:** For specific ARM build challenges, the project's dedicated Raspberry Pi build script and Dockerfile are the authoritative sources.

### `@electron/remote` Not Found at Runtime

* **Problem:** After building, the application fails to launch or encounters errors related to `@electron/remote`. The `package.json` includes `@electron/remote` in `extraResources` for `electron-builder`, indicating it's handled during the packaging process.
* **Solution:** While less common with proper `yarn install` and `yarn prepare` execution, sometimes `@electron/remote` might still be an issue. If so, after `yarn build` (or `yarn build-latest`), navigate into the build output directory (e.g., `dist/gsender` or `build`) and install it manually:
    ```bash
    # Assuming your build output is in 'dist/gsender' (as per "build.directories.app" in package.json)
    cd dist/gsender
    npm install --save @electron/remote
    cd ../.. # Return to root project directory
    ```

### Disk Space or Long Path Issues (Windows)

* **Problem:** On Windows, deep directory structures can exceed the maximum path length, causing issues during dependency installation.
* **Solution:** Enable long path support in Windows ([requires registry modification or Group Policy](https://learn.microsoft.com/en-us/windows/win32/fileio/maximum-file-path-limitation)). Also, ensure you have sufficient disk space.

### Network Issues (Firewall/Proxy)

* **Problem:** `yarn install` fails to download packages.
* **Solution:** Check your firewall or proxy settings. Ensure `npm` and `yarn` are configured to use your proxy if applicable. `npm` and `yarn` needs access to the internet to download and install dependencies.

![](/_images/_gsender/_compile/gs_co_yarn-network-error.png){.aligncenter .size-medium}

---

## Contributing

If you've successfully built gSender and found a solution to an unlisted problem, consider contributing to the project or creating a <a href="https://github.com/Sienci-Labs/gsender/pulls" target="_blank" rel="noopener">Pull Request</a> to improve this documentation. Your contributions help the entire community!
