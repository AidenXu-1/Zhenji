<p align="center">
  <img src="assets/zhenji-logo.svg" width="112" alt="帧集相机笑脸标志">
</p>

<h1 align="center">帧集</h1>

<p align="center">
  把截图、录屏与素材整理，收进一条安静的本地工作流。
</p>

<p align="center">
  macOS 15+ · Apple Silicon · 本机处理 · 公开测试版
</p>

<p align="center">
  <a href="https://github.com/AidenXu-1/Zhenji/releases/latest"><strong>下载最新版本</strong></a>
  ·
  <a href="PRIVACY.md">隐私说明</a>
  ·
  <a href="KNOWN_ISSUES.md">已知限制</a>
  ·
  <a href="SUPPORT.md">问题反馈</a>
</p>

![帧集：截图、录屏与素材采集的一体化本地工作流](assets/zhenji-hero.svg)

## 一次完成，从捕捉到整理

帧集是一款面向 macOS 的截图、录屏与素材采集工具。它把高频动作放在快捷键附近，把编辑和整理留在同一条工作流里，减少在多个应用之间来回切换。

| 截图 | 录屏 | 采集与整理 |
| --- | --- | --- |
| 区域、窗口、全屏与上次范围 | 屏幕、麦克风与摄像头 | 图片与视频采集板 |
| 标注、圆角、阴影与固定截图 | 区域框选、暂停继续与本地编辑 | OCR、二维码与本地图片翻译 |
| 滚动长图与快速复制、保存 | 自动缩放、录中标记与导出 | 素材库与连续工作流 |

## 下载与安装

当前版本为 **0.2.0 公开测试版**，支持 macOS 15 或更高版本及 Apple Silicon Mac。

- [下载 DMG（推荐）](https://github.com/AidenXu-1/Zhenji/releases/download/v0.2.0/Zhenji-0.2.0-macOS-arm64.dmg)
- [下载 ZIP（备用）](https://github.com/AidenXu-1/Zhenji/releases/download/v0.2.0/Zhenji-0.2.0-macOS-arm64.zip)
- [查看版本说明](https://github.com/AidenXu-1/Zhenji/releases/tag/v0.2.0)

安装步骤：

1. 打开 DMG，把“帧集”拖入“应用程序”。
2. 首次启动若被 macOS 拦截，进入“系统设置 → 隐私与安全性”，在“安全性”区域点击“仍要打开”。
3. 按应用内引导授予屏幕录制权限。只有启用对应功能时，才需要麦克风或摄像头权限。
4. macOS 授权后若功能没有立即生效，请退出并重新打开帧集。

> 当前公开测试版未使用 Developer ID，也未经过 Apple 公证。临时签名可用于校验包体完整性，但不会获得 Gatekeeper 直接放行。“仍要打开”也不能代替屏幕录制、麦克风或摄像头授权。

## 隐私边界

- 无需注册账户。
- 当前版本不包含广告、行为分析或遥测上报。
- 截图、录屏、OCR、二维码识别和图片翻译默认在用户的 Mac 上处理。
- 用户内容不会由帧集主动上传。
- 发布包在上传前会检查本机绝对路径、内部任务标记、调试覆盖率数据和常见凭据特征。

更完整的权限与数据说明见 [PRIVACY.md](PRIVACY.md)。提交问题前，请先遮挡截图或录屏中的账号、聊天内容、文件路径及其他敏感信息。

## 校验下载文件

下载同一版本的 `SHA256SUMS.txt` 后，可在终端执行：

```bash
shasum -a 256 -c SHA256SUMS.txt
codesign --verify --deep --strict --verbose=4 /Applications/帧集.app
```

校验和用于确认下载文件字节一致；`codesign` 用于检查 App 包体签名完整性。它们都不代表 Apple 公证或 Gatekeeper 信任。

## 项目说明

此仓库仅用于公开下载、版本说明和问题反馈，不包含帧集的产品源码，也不以开源许可证发布。

遇到问题请先查看 [已知限制](KNOWN_ISSUES.md)，再通过 [GitHub Issues](https://github.com/AidenXu-1/Zhenji/issues) 提交可复现信息。
