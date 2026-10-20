<p align="center"><img src="https://raw.githubusercontent.com/zxxlxj/rex-m/main/assets/dian115.jpg" width="104" alt="DIAN115 Logo" /></p>

# MADOW X DIAN115

在 REX 中浏览 DIAN115 已缓存的电影、剧集，并按需播放。

当前版本：**2.0.0**。请先更新 DIAN115 到包含新版播放器代理功能的版本，再更新模块。

**[一键导入 REX](https://rexnow.tv/widget?url=https%3A%2F%2Fraw.githubusercontent.com%2Fzxxlxj%2Frex-m%2Fmain%2Fdocs%2Fplugin-platform%2Fexamples%2Fdian115-player%2Fdian115.rex.js%3Fv%3D2.0.0)**

也可在播放器中导入集合地址：

```text
https://raw.githubusercontent.com/zxxlxj/rex-m/main/madow.rex?v=2.0.0
```

## 开始使用

1. 填写 **DIAN115 地址**和 **DIAN115 API Key**。
2. 打开“获取播放账号”，点击选择主账号或备用账号。
3. 在“DIAN115 媒体缓存”中浏览资源，或在播放器媒体详情页选择资源播放。

支持 HTTP、HTTPS 和内网地址，例如 `http://192.168.1.100:8080`。

如需在本地没有资源时查询 MADOW，请在 DIAN115 的虚拟缓存页面启用站点查询，并配置站点账号。

## 播放与缓存

- 浏览资源不会解锁或获取直链；点击播放时才由 DIAN115 使用所选账号处理。
- 播放结果会在下一次加载资源时同步到本机。已同步的直链直接播放，不再请求 DIAN115。
- 直链最长缓存两小时，115 提前到期时立即失效。切换播放账号后使用各自的缓存。
- 资源列表显示视频参数与文件大小；2160P 统一显示为 4K，不同版本分别展示。
- “模块说明”中可查看解锁说明、今日统计和项目链接。

[DIAN115 GitHub](https://github.com/madbrolab/dian115) · [使用 Wiki](https://madbrolab.github.io/dian115/)
