<div align="center">
  <img src="https://raw.githubusercontent.com/NovaFlare-Engine-Concentration/NovaFlare-Engine.github.io/refs/heads/main/images/logo2.png" width="380" alt="NovaFlare Icon">
  <br/>
  <h1 align="center">Friday Night Funkin' - NovaFlare Engine</h1>
  <p align="center"><b>✦ Revival | 复兴计划 ✦</b></p>
  <p align="center">基于 Psych 引擎，最初用于 VS Camellia 同人作，专注于优化和性能，为玩家提供最佳体验。后来转向支持模块化。</p>
  
  <br/>
  
  <a href="#中文版本">
    <img src="https://img.shields.io/badge/中文版本-2d333b?style=for-the-badge&labelColor=1e6f5c" alt="中文版本">
  </a>
  <a href="#english-version">
    <img src="https://img.shields.io/badge/English_Version-2d333b?style=for-the-badge&labelColor=1e6f5c" alt="English Version">
  </a>
  
  <br/>
  
  <img src="https://img.shields.io/github/v/release/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine?style=for-the-badge&color=1e6f5c" alt="Release">
  <img src="https://img.shields.io/github/repo-size/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine?style=for-the-badge&color=1e6f5c" alt="Repo Size">
  <img src="https://img.shields.io/github/downloads/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine/total?style=for-the-badge&color=1e6f5c" alt="Downloads">
  <img src="https://img.shields.io/github/commit-activity/m/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine?style=for-the-badge&color=1e6f5c" alt="Commit Activity">
  
  <br/>
  
  <img src="https://img.shields.io/badge/Haxe-4.3.7-1e6f5c?style=for-the-badge" alt="Haxe 4.3.7">
  <img src="https://img.shields.io/badge/Lime-1e6f5c?style=for-the-badge" alt="Lime">
  <img src="https://img.shields.io/badge/FNF_Modding-1e6f5c?style=for-the-badge" alt="FNF Modding">
</div>

<br/>

> 复兴计划 —— 修复、优化并留存 FNF-NovaFlare-Engine 的遗产。

---

## 目录

- [简介](#简介)
- [构建指南](#构建指南)
- [版本历史](#版本历史)
- [特别说明](#特别说明)

---

## 简介

### 复兴计划

顾名思义，这个项目旨在修复和优化 FNF-NovaFlare-Engine 老版本的编译。

### 为什么做这个

纯粹为了好玩和存档。

### 怎么做

每个 Release 中都包含一个 `hmm.json` 文件，它将每个库锁定到构建时使用的确切提交。使用该文件并运行：

```bash
haxelib run hmm install
```

你就可以还原该 Release 的精确环境。

> [!NOTE]
> 某些版本可能需要特殊的编译步骤 —— 这些会在[特别说明](#特别说明)中注明。

> [!TIP]
> 得益于升级版的 Lime，复兴版本在 FPS 调整部分增加了一些原版没有的额外选项。

---

## 构建指南

### 1. 安装 Haxe 4.3.7

下载并安装 [Haxe 4.3.7](https://haxe.org/download/version/4.3.7/)。

### 2. 设置 Visual Studio 构建工具

运行以下命令配置 VSCode 编译环境：

```bash
curl -# -O https://download.visualstudio.microsoft.com/download/pr/3105fcfe-e771-41d6-9a1c-fc971e7d03a7/8eb13958dc429a6e6f7e0d6704d43a55f18d02a253608351b6bf6723ffdaf24e/vs_Community.exe
echo 正在安装 Visual Studio 组件（可能需要一段时间）...
vs_Community.exe --add Microsoft.VisualStudio.Component.VC.Tools.x86.x64 --add Microsoft.VisualStudio.Component.Windows10SDK.19041 -p --wait --quiet
del vs_Community.exe
```

### 3. 获取源代码

下载你要构建的版本的源代码。

> [!IMPORTANT]
> 请务必用 Release 中的 `hmm.json` 替换下载源码里的默认文件。源码仓库里的 `hmm.json` 没有具体的 commit 提交记录，直接使用会导致老版本出问题。

### 4. 安装依赖

```bash
haxelib run hmm install
```

### 5. 设置 Lime

```bash
haxelib run lime setup
```

### 6. 构建并运行

```bash
lime test windows
```

---

## 版本历史

### NovaFlare-V1.2.1-Hotfix

**发布日期：** 2026年8月10日  
**下载地址：** [V1.2.1-Hotfix](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine/releases/tag/V1.2.1-Hotfix)

> [!CAUTION]
> **特别说明**

1. 需要用以下命令编译：
   ```bash
   lime build windows -Dlegacy_gc_compare
   ```
   否则会出现关于 GC 的编译报错。

2. 在 `Project.xml` 的第 5 行，把：
   ```xml
   <app ... version="1.2.1-Hotfix" ... />
   ```
   改为：
   ```xml
   <app ... version="1.2.1" ... />
   ```
   否则你会看到：
   ```
   ./ApplicationMain.rc(6): error RC2237 : numeric value expected at Hotfix
   ./ApplicationMain.rc(7): error RC2237 : numeric value expected at Hotfix
   ```

---

### NovaFlare-V1.0.1

**原始发布日期：** 2023年9月9日  
**原始下载地址：** [1.0.1](https://github.com/beihu235/NovaFlare-Engine-V1.0.1/releases/tag/1.0.1)

**复兴构建日期：** 2026年8月22日  
**复兴下载地址：** [V1.0.1-Revival](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine-1.0.1-Revival/releases/tag/V1.0.1-Revival)

---

## 特别说明

- 某些老版本可能需要特定的 Haxe 或 Lime 版本 —— 请查看 Release 说明。
- 复兴版本使用了更新的 Lime 后端，因此解锁了额外的 FPS 选项。
- 所有复兴构建都旨在保留原始体验，同时修复兼容性问题。

---

<div align="center">
  <sub>
    Made with love by the NovaFlare Team
  </sub>
</div>