<div align="center">
  <img src="https://raw.githubusercontent.com/NovaFlare-Engine-Concentration/NovaFlare-Engine.github.io/refs/heads/main/images/logo2.png" width="380" alt="NovaFlare Icon">
  <br/>
  <h1 align="center">Friday Night Funkin' - NovaFlare Engine</h1>
  <p align="center"><b>✦ Revival ✦</b></p>
  <p align="center">Engine based on Psych originally used on VS Camellia fanmade and focused on optimisation and performance to give players best possible experience. It was later moved to support modules.</p>

  <br/>
  <h2>
    <a href="README-ZH.md">中文版本</a>
  </h2>
</div>

---

## Introduction

**Revival Plan**  
As the name suggests, it is about restoring and refining the older builds of the FNF-NovaFlare-Engine compilation.

**Why do this**  
Purely for fun and preservation.

**How to do it**  
Each release uploaded file contains a `hmm.json` file. This file records the exact commit hash of every library at the time of the release workflow build. In theory, if you use the `hmm.json` from a specific release and run the command `haxelib run hmm install`, you should be able to restore the library versions to exactly what they were when that release was built.

Note: Some versions may require specific compilation steps. These will be noted separately.
And because it uses the more advanced Lime, the Revival version has a few additional options in the FPS adjustment section.

1.  Download and install Haxe 4.3.7.
2.  Execute the following commands to set up the VSCode compilation environment:
    ```
    curl -# -O https://download.visualstudio.microsoft.com/download/pr/3105fcfe-e771-41d6-9a1c-fc971e7d03a7/8eb13958dc429a6e6f7e0d6704d43a55f18d02a253608351b6bf6723ffdaf24e/vs_Community.exe
    echo Installing Visual Studio components (this may take a while)...
    vs_Community.exe --add Microsoft.VisualStudio.Component.VC.Tools.x86.x64 --add Microsoft.VisualStudio.Component.Windows10SDK.19041 -p --wait --quiet
    del vs_Community.exe
    ```
3.  Download the source code. **Important:** Replace the default `hmm.json` in the downloaded source with the one from the release. The repository's default `hmm.json` lacks specific commit references, which can cause compatibility issues with older versions.
4.  Run `haxelib run hmm install` to install the required Haxe libraries.
5.  Run `haxelib run lime setup`.
6.  Run `lime test windows`.

## History

**NovaFlare-V1.2.1-Hotfix**  
Release Date: August 10, 2026  
Release and Download: [V1.2.1-Hotfix](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine/releases/tag/V1.2.1-Hotfix)

Special Instructions:
1.  Compilation requires the command `lime build windows -Dlegacy_gc_compare`; otherwise, a garbage collection (GC) related compile error will occur.
2.  In line 5 of `Project.xml`, the version tag `<app title="NovaFlare Engine" ... version="1.2.1-Hotfix" ... />` can cause compilation errors. You will need to manually change `version="1.2.1-Hotfix"` to `version="1.2.1"`.

**NovaFlare-V1.0.1**  
Original Release Date: September 9, 2023  
Original Release: [1.0.1](https://github.com/beihu235/NovaFlare-Engine-V1.0.1/releases/tag/1.0.1)

Revival Build Date: August 22, 2026  
Revival Release: [V1.0.1-Revival](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine-1.0.1-Revival/releases/tag/V1.0.1-Revival)