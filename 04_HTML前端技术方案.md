# HTML 前端技术方案

## 技术路线

- HTML：页面结构与无障碍语义。
- CSS：响应式布局、主题和翻牌动画。
- 原生 JavaScript：筛选、抽牌、记录和本地存储。
- JSON：牌组、单牌、牌阵与版权数据。

## 建议目录

```text
index.html
assets/
  css/
  js/
  images/
    rws/
    etteilla-1/
    etteilla-2/
  data/
    decks.json
    cards-rws.json
    spreads.json
```

## 图片处理

- 下载后保留原始文件，网页使用单独的优化副本。
- 统一方向、裁切比例和文件命名，例如 `rws-major-00-fool.webp`。
- 生成适合列表的缩略图和适合详情页的中等尺寸图片。
- 每套牌使用相同牌背，避免在翻牌前暴露牌面。

## 性能要求

- 首屏不一次加载全部 78 张大图。
- 列表使用缩略图和原生懒加载。
- 详情页按需加载中等尺寸图片。
- 静态资源可部署到 GitHub Pages、Cloudflare Pages 或任意静态主机。

## 后续扩展

可逐步增加 PWA、离线缓存、云同步、多语言和用户账号，但不应阻塞第一版上线。
