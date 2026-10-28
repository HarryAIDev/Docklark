<p align="center"><a href="README.md">English</a> · <strong>简体中文</strong></p>
<p align="center"><a href="https://docklark.com/zh/"><img src="assets/docklark-mark.svg" width="80" height="80" alt="Docklark 标志"></a></p>
<h1 align="center">Docklark — Mac SSH 与运维工作台</h1>
<p align="center">把连接、终端、文件和主机工具放进同一个原生工作台。<br>面向 Apple Silicon，完全免费，无需购买或订阅。</p>
<p align="center"><a href="https://github.com/HarryAIDev/Docklark/releases/latest"><strong>下载 Mac 版</strong></a> · <a href="https://docklark.com/zh/features/">全部功能</a> · <a href="https://docklark.com/zh/docs/">使用文档</a> · <a href="https://docklark.com/zh/roadmap/">开发进展</a></p>

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-zh-workspace-dark.webp"><img src="https://docklark.com/assets/product/native-zh-workspace-light.webp" width="100%" alt="Docklark 运维工作台：终端、连接、远端文件与资源曲线"></picture></p>

从 Windows 转到 macOS 后，Harry 希望找回使用 Xshell 时有条理、顺手的远程工作体验，这就是 Docklark 的起点。保存连接、安排会话、传输文件和处理常用主机操作，都集中在一个 Mac 应用中。

> 官网于 2026 年 10 月 27 日对照已安装的 v0.2.96（构建 106）更新。配图是使用公开演示数据采集的中英文、深浅主题应用实拍，并非生产会话。界面核对与本机样例上传不代表全部认证方式、远端写入、容器操作、转发规则或服务器环境均已验收。[功能页](https://docklark.com/zh/features/#review-scope)说明核对范围；开发路线记录历史进展，不是安装包验收清单。

## 可以用它做什么

### 整理连接，回到熟悉的工作区

- **连接资料库：** 多级目录与颜色继承、搜索、收藏、复制、批量移动和属性修改，以及不含敏感信息的连接模板。
- **SSH 访问：** 密码或私钥认证、JumpServer 入口、受管 SSH 跳板链、保活、压缩与转发选项。密码使用 macOS 钥匙串；主机指纹与认证提示仍需确认。
- **灵活安排会话：** 标签、可调整大小的嵌套分屏和多窗口；跨分屏、跨窗口移动已连接会话，切换终端／运维布局，将收藏和快捷命令停靠四边。
- **保存工作区：** 保存命名的多窗口布局，重启后恢复为待连接会话，再手动连接。快照不保存终端输出、草稿和密码。
- **配置迁移：** Docklark JSON 导入导出与本地 SSH 密钥管理。普通导出不含密码；可选择独立口令保护的加密密码备份，但不包含私钥内容或验证码。这不是云同步或 Xshell 专有格式导入。

### 处理命令与终端输出

- **统一撰写栏：** 选择当前会话或明确的 SSH 接收目标，核对来源窗口和可用状态后发送。Enter 发送，Shift+Enter 换行；全窗口 SSH 范围不包含本地 Shell。
- **快捷命令：** 分组、排序、`{{name}}` 参数与拖入终端；Ctrl+R 复用本次运行的历史，Tab 补全命令或已确认的远端路径，只回填、不执行。标记为危险的命令需要确认。
- **终端查找：** 搜索当前标签或本窗口的标签与分屏，支持正则、区分大小写和循环定位；在内嵌查找栏与独立窗口间切换时保留搜索状态。
- **持久高亮与输出提醒：** 有优先级的文本／正则规则、前景与背景预览，可用于全局、连接或单个会话。可选通知仅显示会话名和规则名，不包含匹配的终端正文；提醒不会执行命令。
- **Shell 集成：** 跳转命令提示符、选择最近命令输出、查看退出码，并可调整键位行为与滚动历史。远端 Bash／Zsh 集成需要配置，不会据此推断目标主机变化。
- **本地 Shell 衔接：** SSH 结束后保留标签与已保留的输出，继续使用本地 Shell。

查找覆盖已保留输出，并非无限历史。发送命令前请核对接收目标：多会话发送不是跨服务器原子事务。显式敏感片段使用钥匙串，仅发给单一终端，不加回车、不广播。

### 传输文件，编辑远端文本

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-zh-sftp-dark.webp"><img src="https://docklark.com/assets/product/native-zh-sftp-light.webp" width="100%" alt="Docklark 原生 SFTP 双栏窗口与传输队列，使用演示文件"></picture></p>

- **嵌入式或独立 SFTP：** 本地／远端目录浏览，文件和目录传输，隐藏文件与空目录，重命名、新建文件夹及复制路径。
- **传输队列：** 1～5 个文件并发，默认 3 个；支持按任务取消、重试、定位文件和复制结果。重叠路径按顺序处理；重名项目编号另存，不覆盖、不合并。
- **跟随 Shell 目录：** 启用 Shell 集成并确认同一主机后，文件面板可跟随终端目录变化。
- **远端文本编辑器：** 行号、查找替换、跳转行、保存前差异预览、远端变更冲突检查与支持的编码保留。文本上限 2 MiB；不支持原子替换的服务器仅提供另存。断线后仍可只读查看和复制未保存草稿。
- **终端 `rz` / `sz`：** ZMODEM 上传下载与独立进度窗口，需目标提供兼容工具并允许该协议；单文件须小于 4 GiB。

SFTP 需要服务器允许 SFTP v3 子系统，不跟随符号链接或设备文件，不删除非空目录，也不支持跨连接断点续传。

### 观察主机，集中处理运维操作

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-zh-tools-dark.webp"><img src="https://docklark.com/assets/product/native-zh-tools-light.webp" width="100%" alt="Docklark 工具中心：多主机概览与会话工具"></picture></p>

- **资源监控：** CPU、内存、Swap、网络速率、磁盘空间、Top 5 进程及 1／5／15 分钟历史曲线。Linux／macOS 采集通过独立 SSH 命令通道完成，无需远端 agent 或 sudo；macOS 内存为估算值。默认每 5 秒刷新，可暂停或自定义为 1～3600 秒。
- **多主机概览：** 表格／卡片视图，快速进入所选主机的终端、资源、文件与工具。
- **进程管理：** 搜索和查看远端进程，确认后请求结束进程。
- **Docker 工具：** 容器状态、镜像、端口、支持的指标、最近日志、启停／重启控件与独立容器终端，具体取决于远端 Docker 环境和权限。
- **端口转发：** 命名的本地、远程和动态 SOCKS 规则，可随会话启动，也可独立启停，无需断开 SSH。

**先确认正在操作哪台主机。** SFTP、监控和主机工具面向 SSH 入口，或受管跳板链最终已认证的主机，不跟随嵌套 `ssh` 命令或 JumpServer 菜单选中的资产。仍需相应的远端 exec／SFTP／Docker 权限，并分别验证实际工作流；真实远端 macOS 指标仍在验收中。

### 编排步骤，保留记录，调整外观

- **步骤流程：** 手动启动或单步执行命令、文本／正则等待、敏感输入提示与暂停，支持每步超时及危险步骤确认。流程绑定单一会话；断线、重连或开始传输会停止流程，不是无人值守调度器或多服务器事务。
- **会话输出日志：** 默认关闭；可开始、暂停、恢复或停止 UTF-8 记录，选择时间戳，并查找、复制或导出。可为连接启用认证后自动记录。普通远端输出仍可能包含秘密，处理敏感信息前请暂停，分享前检查导出。
- **诊断日志：** 与会话日志分开管理，本地 INFO／DEBUG 等级无需重启即可切换，也可导出排查。不记录终端正文、命令、密码、私钥或文件内容，不会自动上传；分享前仍需检查运行元数据。
- **外观：** 英文与简体中文，跟随系统／浅色／深色界面；13 套终端配色，主题预览、搜索与收藏，JSON 和 `.itermcolors` 导入、JSON 导出、自定义颜色、全局或会话独立字体与外观。背景不透明度和毛玻璃强度可分别调节。

<p align="center"><picture><source media="(prefers-color-scheme: dark)" srcset="https://docklark.com/assets/product/native-zh-themes-dark.webp"><img src="https://docklark.com/assets/product/native-zh-themes-light.webp" width="100%" alt="Docklark 原生主题中心与终端配色预览"></picture></p>

## 下载并开始使用

**[v0.2.96](https://github.com/HarryAIDev/Docklark/releases/tag/v0.2.96) · 2026 年 10 月 27 日发布 · Apple Silicon（arm64）**

[DMG 安装包](https://github.com/HarryAIDev/Docklark/releases/download/v0.2.96/Docklark_0.2.96_2026.10.27_arm64.dmg) · [SHA-256 校验文件](https://github.com/HarryAIDev/Docklark/releases/download/v0.2.96/Docklark_0.2.96_2026.10.27_arm64.dmg.sha256) · [最新正式版](https://github.com/HarryAIDev/Docklark/releases/latest)

1. 将 DMG 与对应校验文件下载到同一目录，在终端切换到该目录并校验：

   ```sh
   shasum -a 256 -c Docklark_0.2.96_2026.10.27_arm64.dmg.sha256
   ```

2. 打开 DMG，按安装界面指引将 Docklark 复制到“应用程序”，保持 macOS 安全保护开启。
3. 准备有访问权限的 SSH 账号，通过可信渠道确认主机指纹。
4. 添加连接，先从一个会话开始，再尝试多会话命令或管理操作。

开发者已反馈在 **macOS 27** 上实测可用，更早版本尚未测试。此版本未提供 Intel 安装包。Developer ID 签名与公证尚未独立核验；校验值一致用于检查文件完整性，不能证明发布者身份。最新信息请查看[下载与安装指南](https://docklark.com/zh/download/)。

## 文档与项目状态

- [入门与设置](https://docklark.com/zh/docs/) · [SSH 连接指南](https://docklark.com/zh/docs/ssh/) · [JumpServer 指南](https://docklark.com/zh/docs/jumpserver/)
- [完整功能与使用边界](https://docklark.com/zh/features/) · [每日功能进展](https://docklark.com/zh/roadmap/)
- [Mac SSH 客户端指南](https://docklark.com/zh/ssh-client-for-mac/) · [Mac SFTP 客户端指南](https://docklark.com/zh/sftp-client-for-mac/) · [实用文章](https://docklark.com/zh/blog/) · [关于 Docklark](https://docklark.com/zh/about/)

Docklark 处于早期持续开发阶段，初期更新频繁，后续按阶段发布。详细使用说明以官网为准，可下载的安装包以 Releases 为准。

**本仓库用于公开版本发布、使用说明与问题反馈，不是应用源码仓库。** GitHub 自动生成的源码压缩包包含本仓库文档与素材，并非应用源码。

## 反馈与交流

欢迎[提交 Issue](https://github.com/HarryAIDev/Docklark/issues)，或[通过 X 联系 Harry](https://x.com/HarryAIDev)。请提供应用版本、macOS 版本、复现步骤与预期结果。分享截图和日志前，移除密码、私钥、令牌、敏感主机信息与个人文件路径。

Docklark 是独立项目。Xshell 是 NetSarang Computer, Inc. 的商标；Docklark 与 NetSarang 无关联，亦未获得其赞助或认可。

<p align="center">由 Harry 打造，源于日常远程工作的需要。<br><a href="https://docklark.com/zh/">docklark.com</a></p>
