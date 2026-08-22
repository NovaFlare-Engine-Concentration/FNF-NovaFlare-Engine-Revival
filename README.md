<div align="center">
  <img src="https://raw.githubusercontent.com/NovaFlare-Engine-Concentration/NovaFlare-Engine.github.io/refs/heads/main/images/logo2.png" width="380" alt="NovaFlare Icon">
  <br/>
  <h1 align="center">Friday Night Funkin' - NovaFlare Engine</h1>
  <p align="center"><b>✦ Revival ✦</b></p>
  <p align="center">A Psych-based engine originally built for the VS Camellia fanmade, focused on optimisation and performance for the best possible experience. Later shifted to support modular design.</p>
  
  <br/>
  
  <h2 align="center">
    <a href="README-ZH.md">中文版本</a>
  </h2>
</div>

<br/>

> Revival — Restoring, refining, and preserving the legacy of FNF-NovaFlare-Engine.

---

## Table of Contents

- [Introduction](#introduction)
- [How to Build](#how-to-build)
- [Version History](#version-history)
- [Special Notes](#special-notes)

---

## Introduction

### Revival Plan

As the name suggests, this project is about restoring and refining the older builds of the FNF-NovaFlare-Engine compilation.

### Why do this

Purely for fun and preservation.

### How to do it

Each release includes a `hmm.json` file that locks every library to the exact commit used at build time. By using that file and running:

```bash
haxelib run hmm install
```

you can restore the exact environment of that release.

> [!NOTE]
> Some versions may require special compilation steps — these will be noted in the [Special Notes](#special-notes) section.

> [!TIP]
> Thanks to the upgraded Lime, the Revival version includes a few extra FPS adjustment options not found in the original.

---

## How to Build

### 1. Install Haxe 4.3.7

Download and install [Haxe 4.3.7](https://haxe.org/download/version/4.3.7/).

### 2. Set up Visual Studio Build Tools

Run the following commands to set up the VSCode compilation environment:

```bash
curl -# -O https://download.visualstudio.microsoft.com/download/pr/3105fcfe-e771-41d6-9a1c-fc971e7d03a7/8eb13958dc429a6e6f7e0d6704d43a55f18d02a253608351b6bf6723ffdaf24e/vs_Community.exe
echo Installing Visual Studio components (this may take a while)...
vs_Community.exe --add Microsoft.VisualStudio.Component.VC.Tools.x86.x64 --add Microsoft.VisualStudio.Component.Windows10SDK.19041 -p --wait --quiet
del vs_Community.exe
```

### 3. Get the Source Code

Download the source code for the version you want to build.

> [!IMPORTANT]
> Replace the default `hmm.json` in the downloaded source with the one from the release. The repository's default `hmm.json` lacks specific commit references, which breaks older versions.

### 4. Install Dependencies

```bash
haxelib run hmm install
```

### 5. Set up Lime

```bash
haxelib run lime setup
```

### 6. Build and Run

```bash
lime test windows
```

---

## Version History

### NovaFlare-V1.2.1-Hotfix

**Release Date:** August 10, 2026  
**Download:** [V1.2.1-Hotfix](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine/releases/tag/V1.2.1-Hotfix)

> [!CAUTION]
> **Special Instructions**

1. Compile with:
   ```bash
   lime build windows -Dlegacy_gc_compare
   ```
   Otherwise, you'll get GC-related build errors.

2. In `Project.xml` (line 5), change:
   ```xml
   <app ... version="1.2.1-Hotfix" ... />
   ```
   to:
   ```xml
   <app ... version="1.2.1" ... />
   ```
   Otherwise you'll see:
   ```
   ./ApplicationMain.rc(6): error RC2237 : numeric value expected at Hotfix
   ./ApplicationMain.rc(7): error RC2237 : numeric value expected at Hotfix
   ```

---

### NovaFlare-V1.0.1

**Original Release Date:** September 9, 2023  
**Original Download:** [1.0.1](https://github.com/beihu235/NovaFlare-Engine-V1.0.1/releases/tag/1.0.1)

**Revival Build Date:** August 22, 2026  
**Revival Download:** [V1.0.1-Revival](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine-1.0.1-Revival/releases/tag/V1.0.1-Revival)

---

## Special Notes

- The Revival version uses a newer Lime backend, which unlocks additional options.
- All revival builds aim to preserve the original experience while fixing compatibility issues.

---

<div align="center">
  <sub>
    Made with love by the NovaFlare Team
  </sub>
</div>