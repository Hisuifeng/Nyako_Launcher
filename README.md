# Nyako Launcher

插件优先的 Minecraft Java 版启动器（Windows 桌面端）。

> **本仓库只收集问题、发布安装包。** 启动器源码不在本仓库，也不接受代码类 PR。

[下载最新版本](https://github.com/Hisuifeng/Nyako_Launcher/releases/latest) · [提交问题](https://github.com/Hisuifeng/Nyako_Launcher/issues/new/choose)

## 下载

安装包只在 [Releases](https://github.com/Hisuifeng/Nyako_Launcher/releases) 页发布，每次发布包含两个文件：

| 文件 | 说明 |
| --- | --- |
| `Nyako-Launcher-<版本>-win64.zip` | 便携版，解压即用，无需安装 |
| `Nyako-Launcher-<版本>-win64.zip.sha256` | 对应压缩包的 SHA-256 |

下载后先校验，哈希一致再运行：

```powershell
Get-FileHash .\Nyako-Launcher-0.1.1-win64.zip -Algorithm SHA256
```

发布分为两个通道：**稳定版**（验收通过后发布）和**预览版**（提前试用，可能带已知问题）。可在启动器「关于」页查看当前版本并切换更新通道。

## 运行

环境要求：

- Windows 10 / 11 64 位
- WebView2 Runtime（系统一般自带，缺失时启动器会提示安装）
- Java 17 及以上（可让启动器自动安装）

## 反馈问题

1. 先搜索已有 issue，避免重复
2. 用模板新建：[Bug 报告](https://github.com/Hisuifeng/Nyako_Launcher/issues/new?template=bug_report.yml) / [功能建议](https://github.com/Hisuifeng/Nyako_Launcher/issues/new?template=feature_request.yml)

请不要在 issue 中粘贴 token、完整账号信息，或公开可被利用的漏洞细节（见 [SECURITY.md](SECURITY.md)）。

## 说明

- 启动器不附带 Minecraft 本体、游戏资源或账号；请自备正版账号
- 非 Mojang / Microsoft 官方产品，Minecraft 商标归 Mojang Studios 所有

## 许可与致谢

第三方组件许可清单见启动器「关于」页及安装包内说明，感谢这些伟大的开发者们。
