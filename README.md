<p align="center"><img src="assets/dian115.jpg" width="104" alt="DIAN115 Logo" /></p>

# MADOW X DIAN115

REX 播放器虚拟缓存模块。按播放器已识别的 TMDB 编号、媒体类型和季集匹配资源，用本机 115 Cookie 获取免转存直链；支持确认转存、分组缓存和失效分享屏蔽。

当前版本：**1.3.1** · 模块 ID：`dian115.virtual-cache` · 发布格式：`REXENC`

## 导入

**[在 REX 中一键导入](https://rexnow.tv/widget?url=https%3A%2F%2Fraw.githubusercontent.com%2Fzxxlxj%2Frex-m%2Fmain%2Fdocs%2Fplugin-platform%2Fexamples%2Fdian115-player%2Fdian115.rex.js)**

此入口使用 REX 官网的 `/widget` 通用链接，在安装 REX 的设备打开；浏览器出现提示时点击“在 Rex 中打开”。

也可在播放器的模块导入入口粘贴集合地址，按同一地址获取后续更新：

```text
https://raw.githubusercontent.com/zxxlxj/rex-m/main/madow.rex
```

[查看导入集合](https://raw.githubusercontent.com/zxxlxj/rex-m/main/madow.rex) · [加密模块单文件](https://raw.githubusercontent.com/zxxlxj/rex-m/main/docs/plugin-platform/examples/dian115-player/dian115.rex.js)

## 配置

在全局设置中选择一种“资源服务”，地址与密钥分别填写。另填自己的 **115 Cookie**；需要转存时，再填 **115 转存目录 CID**（目录编号）。

| 服务 | 地址 | 密钥 |
| --- | --- | --- |
| DIAN115 | 自己的实例基础地址，例如 `https://dian115.example`，可带部署路径 | DIAN115 系统 OpenAPI Key |
| 独立回调服务器 | 回调基础地址，例如 `https://callback.example/api/portal/player/v1/virtual-cache` | MADOW API Key |

隐藏的另一种服务配置不参与请求。插件自动拼接接口路径，密钥通过请求头发送。DIAN115 模式需使用已支持播放器虚拟缓存接口的新版本；在“虚拟缓存”页配置站点账号并按需开启允许播放器查询站点资源。已有本地条目直接返回，本地无条目才查询站点。

独立回调需实现[开放协议](docs/callback-server-v1.md)，可参考 license-server 的播放器接口。回调接口未实现时，仅安装插件无法取得资源。115 Cookie 只由播放器发给 115；DIAN115 和回调服务器均不代取链、不代转存。

## 使用

- **播放**：查询不解锁；开始播放或确认转存时按需自动解锁，遵循站点原有积分与额度。已有分享参数直接复用，同一分享的多个文件共用授权。
- **视频信息**：按维度优先采用发布者标记，再补本地 FFP 和文件名中的分辨率、HDR、编码等参数；不显示大小。电影不解析季集。
- **转存资源**：最近媒体按 TMDB 合并，剧集按季和 HDR 分类。可单文件、单集或整类确认转存；合并同分享请求，去重并限制提交频率。结果未知时保留记录，先到 115 核实。
- **插件说明 · 今日已解锁**：查看按分享去重的当日统计、解锁说明，以及 DIAN115 项目和 Wiki 入口。资源行不显示解锁状态。
- **失效清单**：确认失效的分享在本机屏蔽；可导出去重后的站点分享 ID，本地来源不导出。导出不会自动提交站点。

资源信息默认缓存 120 秒（15–600 秒可调），本机资源缓存默认 8 MiB（1–64 MiB 可调）。直链缓存取“两小时”和“115 返回到期时间”的较早者；无法确认到期时间时不缓存。不同服务、密钥、Cookie 和文件参数分别隔离。

插件自有缓存、分享链接和转存记录采用认证加密。Cookie 和 API Key 的输入项由播放器设置系统保管，宿主设置是否加密取决于播放器。播放器重建脚本环境后，请先重新打开模块载入配置，再继续详情页操作。

## 发布内容

| 路径 | 内容 |
| --- | --- |
| `madow.rex` | 稳定导入集合，含模块版本、图标和加密脚本地址 |
| `docs/plugin-platform/examples/dian115-player/dian115.rex.js` | 原生加密模块；加密前已移除全部源码注释 |
| `assets/dian115.jpg` | DIAN115 官方原图副本 |
| `docs/callback-server-v1.md` | 回调服务器开放协议 |
| `checksums.json` | 版本与公开文件 SHA-256 摘要 |

图标原图来自 [madbrolab/dian115](https://github.com/madbrolab/dian115/blob/main/frontend/public/logo.jpg)，Git blob 为 `617f73c9057f5a5d0e3d11a1f5eef979f4776b18`。本仓库仅发布独立播放器模块和开放材料。

离线用例及加密格式已校验；仍需在目标 REX 版本验证原生解密、起播、外链、导出和转存确认交互。转存仅应在点击“确认转存”后执行，宿主不能预取确认入口。取链沿用宿主默认 UA，HTTP 请求栈与视频引擎的 UA 是否一致需真机验证。

[DIAN115 GitHub](https://github.com/madbrolab/dian115) · [使用 Wiki](https://madbrolab.github.io/dian115/) · [REX](https://rexnow.tv/)
