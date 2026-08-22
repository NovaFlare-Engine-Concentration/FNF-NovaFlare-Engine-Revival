这是中文版，所有链接都改成了超链接格式：

```markdown
<div align="center">
  <img src="https://raw.githubusercontent.com/NovaFlare-Engine-Concentration/NovaFlare-Engine.github.io/refs/heads/main/images/logo2.png" width="380" alt="NovaFlare Icon">
  <br/>
  <h1 align="center">Friday Night Funkin' - NovaFlare Engine</h1>
  <p align="center"><b>✦ Revival | 复兴计划 ✦</b></p>
  <p align="center">基于 Psych 引擎，最初用于 VS Camellia 同人作，专注于优化和性能，为玩家提供最佳体验。后来转向支持模块化。</p>
</div>

---

## 简介

**复兴计划**  
顾名思义，就是修复和优化 FNF-NovaFlare-Engine 老版本的编译。

**为什么做这个**  
纯粹好玩儿。

**怎么做**
在 Release 上传的文件里会有一个 `hmm.json`，它所记录的每个库都是基于 release 工作流编译时的最新提交。也就是说，你只需要使用 release 上传文件中的 `hmm.json`，并执行命令 `haxelib run hmm install`，大致就可以恢复到和 release 发布时一样的库版本。

注意，有些版本的编译可能需要特殊操作，会特别说明。

并且因为沿用的是更牛逼的lime，所以复兴版本中的调整fps部分会多出来几个选项

1. 下载并安装 Haxe 4.3.7。
2. 执行以下代码配置 VSCode 编译环境：
   ```
   curl -# -O https://download.visualstudio.microsoft.com/download/pr/3105fcfe-e771-41d6-9a1c-fc971e7d03a7/8eb13958dc429a6e6f7e0d6704d43a55f18d02a253608351b6bf6723ffdaf24e/vs_Community.exe
   echo Installing Visual Studio components (this may take a while)...
   vs_Community.exe --add Microsoft.VisualStudio.Component.VC.Tools.x86.x64 --add Microsoft.VisualStudio.Component.Windows10SDK.19041 -p --wait --quiet
   del vs_Community.exe
   ```
3. 下载源代码。**注意**：请务必使用 release 发布的 `hmm.json` 替换下载源码里的默认文件。因为源码仓库里的 `hmm.json` 没有具体的 commit 提交记录，直接使用会导致老版本出问题。
4. 执行 `haxelib run hmm install` 安装 Haxelib 库。
5. 执行 `haxelib run lime setup`。
6. 执行 `lime test windows`。

## 版本历史

**NovaFlare-V1.2.1-Hotfix**  
发布日期：2026年8月10日  
发布及下载地址：[V1.2.1-Hotfix](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine/releases/tag/V1.2.1-Hotfix)

特别说明：
1. 需要用 `lime build windows -Dlegacy_gc_compare` 进行编译，否则会出现关于 GC 的编译报错。
2. `Project.xml` 里第 5 行的 `<app title="NovaFlare Engine" ... version="1.2.1-Hotfix" ... />` 编译可能会报错：
   ```
   ./ApplicationMain.rc(6): error RC2237 : numeric value expected at Hotfix
   ./ApplicationMain.rc(7): error RC2237 : numeric value expected at Hotfix
   ```
   需要手动把 `version="1.2.1-Hotfix"` 改成 `version="1.2.1"`。

**NovaFlare-V1.0.1**  
原始发布日期：2023年9月9日  
原始发布地址：[1.0.1](https://github.com/beihu235/NovaFlare-Engine-V1.0.1/releases/tag/1.0.1)

复兴构建日期：2026年8月22日  
复兴发布地址：[V1.0.1-Revival](https://github.com/NovaFlare-Engine-Concentration/FNF-NovaFlare-Engine-1.0.1-Revival/releases/tag/V1.0.1-Revival)