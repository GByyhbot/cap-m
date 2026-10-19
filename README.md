<p align="center"><img src="assets/dian115.jpg" width="104" alt="DIAN115 Logo" /></p>

# MADOW X DIAN115

在 REX 中浏览、播放电影和剧集资源，也可转存到自己的 115 网盘。

当前版本：**1.3.2**

## 导入

**[一键导入 REX](https://rexnow.tv/widget?url=https%3A%2F%2Fraw.githubusercontent.com%2Fzxxlxj%2Frex-m%2Fmain%2Fdocs%2Fplugin-platform%2Fexamples%2Fdian115-player%2Fdian115.rex.js)**

如果没有自动打开 REX，可复制下面的集合地址，在播放器中导入：

```text
https://raw.githubusercontent.com/zxxlxj/rex-m/main/madow.rex
```

## 填写设置

1. 选择“资源服务”，按下表填写地址和密钥。
2. 填写自己的 **115 Cookie**。
3. 需要转存时，再填写 **115 转存目录 CID**（目录编号）。其他设置保持默认即可。

| 资源服务 | 需要填写 |
| --- | --- |
| DIAN115 | 自己的 DIAN115 地址，以及系统 OpenAPI Key |
| 独立回调服务器 | 服务提供方给出的域名，例如 `madow.example`，以及 MADOW API Key |

地址和密钥分开填写。独立回调只需填域名，后面的路径会自动补齐。

使用 DIAN115 时，如需查询站点资源，请在“虚拟缓存”页面开启站点资源查询，并配置好站点账号。

## 使用提醒

- 浏览资源不会解锁；播放或确认转存时，按站点规则自动解锁。
- 播放链接自动缓存，最长两小时；115 更早到期时会提前失效。
- 在“转存资源”中查看最近获取的媒体，可按文件、单集或整类确认转存。剧集支持按季和 HDR 分类。
- 在“插件说明 · 今日已解锁”中查看解锁说明和今日数量。
- 失效资源会在本机隐藏，失效清单可导出。转存结果不明确时，请先到 115 核实。

图标沿用 [DIAN115 官方 Logo](https://github.com/madbrolab/dian115/blob/main/frontend/public/logo.jpg)。

[DIAN115 GitHub](https://github.com/madbrolab/dian115) · [使用 Wiki](https://madbrolab.github.io/dian115/)
