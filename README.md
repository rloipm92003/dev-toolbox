# Dev Toolbox · 开发者工具箱

一个**零依赖、纯前端、单文件**的开发者常用工具集合。打开 `index.html` 即用，所有计算都在浏览器本地完成，数据不上传任何服务器。

> **在线使用：** https://rloipm92003.github.io/dev-toolbox/

## 功能

| 工具 | 说明 |
| --- | --- |
| **JSON** | 格式化（2/4 空格）、压缩成一行、字符串转义，实时校验语法 |
| **Base64** | UTF-8 安全的编码与解码，中文不乱码 |
| **URL** | 全文编码、仅编码 URL、解码 |
| **时间戳** | 实时显示当前秒/毫秒时间戳，时间戳与日期双向往返，含相对时间与星期 |
| **UUID** | 批量生成 UUID v4（1–100 个） |
| **哈希** | SHA-1 / SHA-256 / SHA-512 |
| **正则** | 在线测试正则，列出全部匹配位置与捕获分组 |
| **颜色** | HEX / RGB / HSL 互转，附带 WCAG 亮度与建议文字色 |

## 使用

不需要构建，不需要安装依赖：

```bash
git clone https://github.com/<your-name>/dev-toolbox.git
cd dev-toolbox
```

然后直接用浏览器打开 `index.html`，或者起一个本地静态服务：

```bash
python -m http.server 8080
# 访问 http://localhost:8080
```

> 哈希与 UUID 功能依赖 `crypto.subtle` / `crypto.randomUUID`，需要通过 `https://` 或 `localhost` 打开。直接双击 `file://` 打开时部分浏览器会禁用这些 API。

## 特性

- **单文件** — 一个 `index.html` 装下全部功能，方便 fork 和魔改
- **零依赖** — 没有 npm、没有 CDN、没有构建步骤
- **隐私友好** — 纯本地运算，输入内容不会离开你的浏览器
- **暗色模式** — 跟随系统 `prefers-color-scheme` 自动切换
- **响应式** — 手机、平板、桌面都能用

## 贡献

欢迎提 Issue 和 PR。新增工具的约定：

1. 在 `#tabs` 中加一个 `<button class="tab" data-tab="xxx">`
2. 在 `.wrap` 中加一个 `<section class="panel" id="panel-xxx" hidden>`
3. 在 `<script>` 中写对应逻辑，保持无依赖

## License

[MIT](LICENSE)
