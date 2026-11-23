# DaoVest 海报 & 文案生成器

## 部署到 GitHub Pages（免费）
1. 在 GitHub 新建仓库（例如 `daovest-poster`），把本文件夹内所有文件上传（`index.html`、`assets/` 文件夹）。
2. 仓库 → Settings → Pages → Source 选 `Deploy from a branch`，Branch 选 `main` / `/ (root)` → Save。
3. 约 1 分钟后得到链接：`https://你的用户名.github.io/daovest-poster/`，行政同事用浏览器打开即可。

> 不要直接双击 index.html 打开，浏览器会限制图片读取，请用 GitHub Pages 链接，或在本机运行 `python3 -m http.server`。

## 换成无文字底图
把无文字底图用**相同文件名、相同尺寸**覆盖 `assets/` 里的图片，然后在页面勾选“底图已无文字”。

## 调整文字位置
`index.html` 里每张海报的 `boxes` 设定了文字位置：`x, y, w, h` 为覆盖区域（图片像素），`size` 为字号，`ax` 左对齐起点、`cx` 居中点。
