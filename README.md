# MCPCBox Downloads

为旧版「多玩我的世界盒子 PC 版」提供替代下载源、兼容资源与 GitHub Pages 静态文件。

这个仓库主要服务于 [`MCPCBox Community Fix`](https://github.com/yuyu107/mcpcbox-community-fix)，用于替代原程序中已经失效或无法再访问的在线资源地址。

> 本仓库不是多玩官方资源库，也不隶属于多玩、YY、Mojang、Microsoft、Azul、Oracle 或其他相关厂商。

## 主要用途

目前本仓库承担这些功能：

- 提供 MCPCBox 修复版所需的 Java 运行环境替代下载源。
- 提供 Minecraft 正式版版本 JSON 的兼容静态地址。
- 通过 GitHub Pages 为旧版盒子提供可直接访问的静态网页和资源。
- 保存旧接口替换时需要的文件校验值、目录结构与兼容说明。
- 作为 `mcpcbox-community-fix` 主项目的配套资源仓库。

主程序、补丁源码以及普通用户可直接使用的 Release 成品不放在这里，请前往：

[`yuyu107/mcpcbox-community-fix`](https://github.com/yuyu107/mcpcbox-community-fix)

## Minecraft 版本 JSON

当前为旧版 MCPCBox 提供 **Minecraft 1.6.2 至 1.16.5 共 52 个正式版**的 Windows 兼容 JSON。

修复版盒子使用的版本 JSON 基址为：

`https://yuyu107.github.io/mcpcbox-downloads/`

目录按照 Minecraft 版本号组织，例如：

- `1.7.10/1.7.10.json`
- `1.8.9/1.8.9.json`
- `1.12.2/1.12.2.json`
- `1.16.5/1.16.5.json`

这些 JSON 在标准版本信息基础上针对旧启动器做了兼容处理，重点避免其错误解析与当前 Windows 无关的依赖项。

## Java 运行环境

原版盒子内置的多个 Java 下载地址已经失效，因此 Community Fix 会将对应地址替换到本仓库托管的兼容包。

当前主修复方案使用：

- Java 7u80 x64 兼容运行环境。
- Java 8u252 x64 兼容运行环境。

替代包需要同时满足旧盒子预期的：

- 压缩包目录结构。
- 文件名与解压后目录布局。
- 主程序内对应的 MD5 校验值。

因此不要在不更新主程序补丁清单的情况下直接替换现有 Java 文件。

## 已知旧 Java 校验值

以下为原程序中曾使用的旧下载项，仅作为逆向与兼容研究记录：

| 文件 | 原程序内置 MD5 |
| --- | --- |
| `jre_7_windows.7z` | `28640ba60fc62f7149124d3522aac9dd` |
| `java_7_8_v32.7z` | `07685aa514748192314591f21b40b01e` |
| `Java_7_8_V64.7z` | `0aae6a0b8a2049abc80afa193bd64ecc` |

这些旧校验值不代表当前修复版实际使用的文件校验值；当前值应以 `mcpcbox-community-fix` 中对应版本的补丁清单为准。

## 静态网页

本仓库也用于托管部分旧页面的替代静态内容，例如“精彩视频”兼容页面。

需要频繁维护、依赖当前在线接口的“游戏直播”页面则单独部署在：

`https://yuyu107.github.io/web/live/`

对应在线源码由 `yuyu107/web` 仓库维护，避免把实时接口逻辑和下载资源混在一起。

## 与主项目的分工

### `mcpcbox-community-fix`

负责：

- MCPCBox 主程序补丁源码。
- 补丁清单与校验值。
- 本地皮肤工具源码。
- 兼容网页源码说明。
- GitHub Releases 成品。

### `mcpcbox-downloads`

负责：

- Java 等替代下载资源。
- Minecraft 版本 JSON。
- GitHub Pages 静态资源。
- 与旧下载接口兼容有关的资源文件。

### `web`

负责：

- 需要持续在线更新的动态兼容页面。
- 当前“游戏直播”列表与直播播放器页面。

## 普通用户

如果只是想使用修复后的多玩我的世界盒子，通常 **不需要手动下载这个仓库里的文件**。

请直接前往主项目 Releases：

- `MCPCBox Community Fix v6.3`：修复版主程序。
- `MCPCBox Local Skin Manager v1.0`：独立本地皮肤导入/管理工具。

主项目地址：

https://github.com/yuyu107/mcpcbox-community-fix

## 说明与版权

本仓库用于非官方兼容性研究与旧软件功能恢复。

仓库中的项目自有脚本、配置与说明不改变第三方组件原有的许可证和版权归属。Minecraft、Java 运行环境及其他第三方软件、商标和内容的权利归各自权利人所有。
