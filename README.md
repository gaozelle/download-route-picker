<div align="center">
  <img src="assets/app-icon.png" width="128" alt="下载线路选择图标">
  <h1>下载线路选择</h1>
  <p>粘贴下载链接，实测 Clash Verge 节点，自动选择最快线路并下载。</p>
  <p><strong>macOS Beta · 当前版本 0.5.3</strong></p>
</div>

## 下载

请前往 [最新版本页面](https://github.com/gaozelle/download-route-picker/releases/latest) 下载 `下载线路选择-0.5.3-macOS.zip`。

这个仓库目前只用于 Beta 版本分发和问题反馈，**暂未公开源代码**。

## 它解决什么问题

VPN 节点的延迟不等于真实文件下载速度。下载线路选择会针对你粘贴的文件链接逐条做小流量测试，再让本次下载使用实测最快的线路。

它使用独立的本地代理端口和独立策略组，不会为了测速反复切换其他 App 正在使用的策略组。

## 功能

- 针对真实下载链接测试节点速度
- 显示每条线路的测速进度和速度
- 自动选择最快线路并完成下载
- 显示最终线路、平均下载速度和保存位置
- 自定义下载文件夹
- 支持取消、断点续传、在访达中显示和打开文件
- 首次启动检查 Clash Verge，并在确认后安装专用配置
- 写入配置前自动备份，拒绝覆盖未知自定义脚本

## 使用要求

- macOS 11 或更高版本
- Intel 或 Apple 芯片 Mac
- 已安装并运行 Clash Verge Rev
- 当前验证环境：Clash Verge v2.5.2、Mihomo v1.19.29

## 安装与第一次使用

1. 从 [Releases](https://github.com/gaozelle/download-route-picker/releases/latest) 下载 ZIP 并解压。
2. 把“下载线路选择.app”拖入“应用程序”文件夹。
3. 首次打开如果 macOS 提示无法验证开发者，请在访达中右键 App，选择“打开”，再确认一次。
4. 保持 Clash Verge 正在运行。
5. 按启动向导完成环境检查；需要时按提示安装专用配置，并重启 Clash Verge。
6. 粘贴直接下载链接、选择保存文件夹，然后点击“开始测速并下载”。

完整说明见 [Beta 测试指南](docs/BETA_TEST_GUIDE.md)。

## TUN 模式

本 App 不会开启、关闭或切换 TUN 模式。测速和下载会显式连接本机 `127.0.0.1:17891` 专用代理端口；Clash Verge 原有的系统代理、TUN 状态和其他策略组保持不变。

## 已知限制

- 只支持无需登录、Cookie 或网页交互的直接文件链接。
- 每条线路最多测试约 1 MB、最长约 4 秒；节点较多时需要等待。
- 当前主要适配 Clash Verge Rev，尚未验证其他 Clash 客户端。
- 当前 Beta 使用临时签名，首次打开可能出现 macOS 安全提醒。
- 尚未加入“为指定 AI App 固定某条 VPN 线路”的功能。

## 反馈

- [报告无法安装、测速或下载的问题](https://github.com/gaozelle/download-route-picker/issues/new?template=bug_report.yml)
- [提交使用体验和建议](https://github.com/gaozelle/download-route-picker/issues/new?template=beta_feedback.yml)

提交截图或日志前，请遮住订阅地址、节点凭据、控制器密钥和个人文件路径。

## 隐私

App 在本机运行，不包含账号、遥测、广告或分析 SDK，不会把 Clash 配置上传到开发者服务器。详见 [隐私说明](PRIVACY.md) 和 [安全说明](SECURITY.md)。

## 项目关系

本项目与 Clash Verge Rev、Mihomo 及任何代理服务商均无隶属或官方合作关系。

