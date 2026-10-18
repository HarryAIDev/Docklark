<p align="center">
  <a href="README.md">English</a> · <strong>简体中文</strong>
</p>

<p align="center">
  <a href="https://docklark.com/zh/">
    <img src="assets/docklark-mark.svg" width="88" height="88" alt="Docklark 标志">
  </a>
</p>

<h1 align="center">Docklark</h1>

<h3 align="center">连接远方，专注眼前。</h3>

<p align="center">
  为 Apple Silicon Mac 打造的原生 SSH 工作台。<br>
  把服务器、会话与文件，放进一个顺手的工作空间。
</p>

<p align="center">
  <a href="https://docklark.com/zh/download/"><img src="https://img.shields.io/badge/macOS-Apple%20Silicon-20312a?style=flat-square&amp;logo=apple&amp;logoColor=white" alt="目标平台：macOS · Apple Silicon"></a>
  <a href="https://docklark.com/zh/features/"><img src="https://img.shields.io/badge/SSH-%2B%20JumpServer-52723a?style=flat-square" alt="SSH 与 JumpServer"></a>
  <a href="https://github.com/HarryAIDev/Docklark/releases"><img src="https://img.shields.io/badge/status-in%20development-b78b35?style=flat-square" alt="开发中，尚未公开发布"></a>
</p>

<p align="center">
  <a href="https://docklark.com/zh/"><strong>官方网站</strong></a> ·
  <a href="https://docklark.com/zh/docs/"><strong>使用文档</strong></a> ·
  <a href="https://github.com/HarryAIDev/Docklark/releases"><strong>版本发布</strong></a> ·
  <a href="https://github.com/HarryAIDev/Docklark/issues"><strong>问题反馈</strong></a>
</p>

<p align="center">
  <a href="#认识-docklark">产品功能</a> ·
  <a href="#下载与安装">下载与安装</a> ·
  <a href="#连接前的准备">连接准备</a>
</p>

<br>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/zh-workspace-dark.webp">
    <source media="(prefers-color-scheme: light)" srcset="assets/zh-workspace-light.webp">
    <img src="assets/zh-workspace-light.webp" alt="使用虚构主机、会话与命令重建的 Docklark 中文工作台预览" width="100%">
  </picture>
</p>

<p align="center">
  <sub>开发版预览 · 使用虚构数据重建的演示图。<br>浅色与深色均展示快速开始，不代表真实连接完成或性能测试。</sub>
</p>

## 认识 Docklark

从保存连接，到运行下一条命令，让日常远程工作更顺手。以下能力已进入开发版，完整工作流仍在进行实机验收。

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>⌘ &nbsp; 连接，井然有序</h3>
      <p>直连 SSH 与 JumpServer 访问，配合连接保存、多级目录、收藏和搜索，让常用环境随手可达。</p>
    </td>
    <td width="50%" valign="top">
      <h3>▥ &nbsp; 为每个会话留出空间</h3>
      <p>标签、嵌套分屏与独立窗口自由组合，让相关任务放在一起，切换时保持上下文。</p>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h3>⇄ &nbsp; 文件，就在终端旁</h3>
      <p>SFTP 双栏浏览本地与远端目录，在传输队列中查看进度，并按需取消任务。</p>
    </td>
    <td valign="top">
      <h3>›_ &nbsp; 常用命令，随时可用</h3>
      <p>保存可复用的快捷命令，通过统一撰写栏选择当前会话或指定会话后发送。</p>
    </td>
  </tr>
  <tr>
    <td valign="top">
      <h3>◉ &nbsp; 重要信息，一眼掌握</h3>
      <p>查看 SSH 入口主机的 CPU 与内存，并在已保留的终端输出中查找需要的内容。</p>
    </td>
    <td valign="top">
      <h3>◐ &nbsp; 让工作台合你心意</h3>
      <p>浅色与深色外观、终端配色，以及英文和简体中文界面，让日常操作更自在。</p>
    </td>
  </tr>
</table>

SFTP 与主机监控作用于 SSH 入口主机，不会跟随嵌套 SSH 或 JumpServer 中选中的目标资产。更多能力与使用边界请查看[产品功能](https://docklark.com/zh/features/)。

## 下载与安装

**首个公开版本仍在准备中，目前尚无公开安装包。**

- **目标平台：** macOS · Apple Silicon
- **系统要求：** 最低 macOS 版本将在公开发布时确认；Intel 支持尚未公布
- **版本信息：** 请通过 [GitHub Releases](https://github.com/HarryAIDev/Docklark/releases) 与[官方版本页面](https://docklark.com/zh/download/)查看下载状态和安装说明

## 连接前的准备

等待首个公开版本期间，可以先了解连接所需的信息：

1. [准备直连 SSH](https://docklark.com/zh/docs/ssh/)：确认主机、端口、账号、网络条件与主机指纹。
2. [通过 JumpServer 连接](https://docklark.com/zh/docs/jumpserver/)：确认堡垒机入口、认证要求与目标资产权限。
3. [查看开发路线](https://docklark.com/zh/roadmap/)：了解开发进展和仍待验收的部分。

## 反馈与交流

遇到问题，或有一个好想法？欢迎[提交 Issue](https://github.com/HarryAIDev/Docklark/issues)，也可以[通过 X 联系 Harry](https://x.com/HarryAIDev)。

反馈问题时，请附上应用版本、macOS 版本、复现步骤和预期结果。公开截图或日志前，请移除密码、私钥、令牌和敏感主机信息。

---

<p align="center">
  由 <a href="https://x.com/HarryAIDev">Harry</a> 打造，源于日常远程工作的需要。<br>
  <sub>本仓库用于 Docklark 的版本发布、使用说明与问题反馈，不包含应用源码。</sub>
</p>
