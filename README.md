<p align="center"><img src="assets/dian115.jpg" width="104" alt="DIAN115 Logo" /></p>

# MADOW X DIAN115

在 REX 中浏览、播放电影和剧集资源，也可转存到自己的 115 网盘。

当前版本：**1.4.5**

## 导入

**[一键导入 REX](https://rexnow.tv/widget?url=https%3A%2F%2Fraw.githubusercontent.com%2Fzxxlxj%2Frex-m%2Fmain%2Fdocs%2Fplugin-platform%2Fexamples%2Fdian115-player%2Fdian115.rex.js%3Fv%3D1.4.5)**

如果没有自动打开 REX，可复制下面的集合地址，在播放器中导入：

```text
https://raw.githubusercontent.com/zxxlxj/rex-m/main/madow.rex?v=1.4.5
```

## 填写设置

1. 选择“资源服务”，按下表填写地址和密钥。
2. 填写自己的 **115 Cookie**。
3. 需要转存时，再填写 **115 转存目录 CID**（目录编号）。其他设置保持默认即可。

| 资源服务 | 需要填写 |
| --- | --- |
| DIAN115 | 自己的 DIAN115 地址，以及系统 OpenAPI Key |
| 独立回调服务器 | 服务提供方给出的域名，例如 `madow.example`，以及 MADOW API Key |

DIAN115 支持 HTTP、HTTPS 和内网地址，例如 `http://192.168.1.100:8080`；省略协议时默认使用 HTTP。

使用 DIAN115 时，如需查询站点资源，请在“虚拟缓存”页面开启站点资源查询，并配置好站点账号。

## 转存资源

在“转存资源”的选项里操作：

1. 选择“查看资源”，资源编号留空，载入最近媒体。填写卡片上的编号再载入，可逐级查看文件；剧集按季和 HDR 分类。
2. 填写文件、单集或分类编号，选择“转存所选资源”并载入。单个文件直接转存。
3. 批量转存时，核对数量和目标目录，选择“确认批量转存”并载入。需要继续时，选择“继续上次转存”。

例如媒体编号为 `1`，分类编号为 `1.1`。转存整个分类时选择分类编号；只转存一集时选择该集或文件的编号。

## 使用提醒

- 1.4.5 修复安装、更新模块时的执行错误；通过上方地址导入即可。
- 浏览资源不会解锁；播放或确认转存时，按站点规则自动解锁。
- 播放链接自动缓存，最长两小时；115 更早到期时会提前失效。
- 优化资源与播放缓存，减少重复读取和请求；旧缓存会自动迁移，首次升级可能稍慢。
- 资源列表显示分辨率、HDR、编码和文件大小，不同版本分行显示；2160P 统一显示为 4K。
- DIAN115 本地已有对应资源时直接返回，缺失时才查询站点；未解锁的站点资源不会写入本地虚拟缓存。
- “转存资源”的操作中可选择“使用说明与今日统计”，资源库不再单列插件说明。
- 从收藏或历史打开后没有资源，可在“使用说明与今日统计”查看“最近资源请求”；剧集请先选中具体一集。
- 失效资源会在本机隐藏，失效清单可导出。转存结果不明确时，请先到 115 核实。

图标沿用 [DIAN115 官方 Logo](https://github.com/madbrolab/dian115/blob/main/frontend/public/logo.jpg)。

[DIAN115 GitHub](https://github.com/madbrolab/dian115) · [使用 Wiki](https://madbrolab.github.io/dian115/)
