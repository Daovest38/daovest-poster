# DaoVest 海报 & 文案生成器 使用手册

## 一、这个工具是做什么的

行政人员只需选择海报类型、填写日期等资料，就能一键生成海报图片和群组文案，不再需要手动修改图片和文字。

支持 5 种海报：全方位课程、赢在起跑线、宏观行业 Live 分析、Tutorial 通知、康乐活动。

---

## 二、日常使用步骤

1. 用浏览器打开网址（见第三部分）。
2. 在“海报类型”下拉选单选择要做的海报。
3. 填写左边出现的栏位，右边会即时更新预览。
4. 点“下载海报”，海报会存成图片。
5. 如果右边有文案，点“复制文案”，再贴到 Facebook 或 Telegram 群组。

### 各海报要填的资料

| 海报 | 要填写的栏位 | 有文案吗 |
|---|---|---|
| 全方位课程 | Day（1~4）、上课日期、主题 | 有（Facebook 版、Telegram 版） |
| 赢在起跑线 | 日期、地点 | 没有 |
| 宏观行业 Live 分析 | 日期、时间 | 没有 |
| Tutorial 通知 | 日期、海报时间、文案时间、Zoom 注册链接 | 有 |
| 康乐活动 | 日期、时间、地点、活动、FB event 链接 | 有 |

### 小提示

- 选好日期后，星期几会自动算出，不用手动输入。
- 全方位课程文案里的截止日固定为“星期四”。
- Facebook 版文案开头有 `@everyone`，Telegram 版没有。
- 康乐活动的时间可以写 `8.30am`，文案里会自动变成 `8:30am`。
- 如果海报上的文字位置不对，请记下是哪张海报、偏向哪个方向，再请人调整。

---

## 三、第一次设置：放到 GitHub Pages（免费）

### 1. 整理文件

在电脑上准备好以下结构（文件夹名称必须是 `assets`，有“s”）：

```
daovest-poster
├── index.html
└── assets
    ├── quanfangwei.jpeg
    ├── yingzai.jpeg
    ├── hongguan.jpeg
    ├── tutorial.jpeg
    └── kangle.jpeg
```

### 2. 图片文件名对照表

必须改成下面的名字，全部小写，不能有空格：

| 海报 | 文件名 |
|---|---|
| 全方位课程（红色，11月28号） | `quanfangwei.jpeg` |
| 赢在起跑线（跑步，9月13日） | `yingzai.jpeg` |
| 宏观行业 Live 分析（橙色） | `hongguan.jpeg` |
| Tutorial 通知（蓝色，Zoom） | `tutorial.jpeg` |
| 康乐活动（走山，Bukit Kiara） | `kangle.jpeg` |

图片格式可以是 `.jpeg`、`.jpg` 或 `.png`，同一张图片只保留一种。

**重命名方法：**
- Windows：点选文件，按 **F2**，输入新名字，按 Enter。
- Mac：点选文件，按 **Enter**，输入新名字，再按 Enter。
- 如果 Windows 看不到 `.jpeg`，请在文件总管点“查看” → “显示” → 勾选“文件扩展名”。

### 3. 建立 GitHub 账号和仓库

1. 到 github.com 注册账号。
2. 点右上角的 **+**，选 **New repository**。
3. 名称填 `daovest-poster`，选 **Public**，点 **Create repository**。

### 4. 上传文件

1. 在空白的仓库页面点 **uploading an existing file**。
2. 把 `index.html` 和整个 `assets` 文件夹拖进去（建议用 Chrome）。
3. 往下滚动，点 **Commit changes**。
4. 确认仓库里有 `index.html` 和 `assets` 文件夹，文件夹里有 5 张图片。

### 5. 开启 GitHub Pages

1. 进入仓库的 **Settings**，再点左边的 **Pages**。
2. 在 **Build and deployment** 下，Source 选 **Deploy from a branch**。
3. Branch 选 **main**，文件夹选 **/ (root)**，点 **Save**。
4. 等 1~2 分钟，刷新页面，顶部会出现网址：
   `https://你的用户名.github.io/daovest-poster/`
5. 把这个网址分享给同事，并加入书签。

> 请用这个网址打开工具，不要直接双击 `index.html`，否则浏览器会读不到图片。

---

## 四、日后更新

- **更换海报图片：** 打开仓库，点 **Add file** → **Upload files**，上传同名的新图片，再点 **Commit changes**。
- **修改程序：** 点开 `index.html`，点右上角的铅笔图标修改，再点 **Commit changes**。
- 更新后等 1~2 分钟，网页就会变成新版本。

### 换成没有文字的底图

如果设计师提供了没有文字的底图：
1. 用相同文件名覆盖 `assets` 里的图片，尺寸也要相同。
2. 打开工具，勾选“底图已无文字（不覆盖原有文字）”。

这样效果会比覆盖旧文字更干净。

---

## 五、常见问题

| 问题 | 解决方法 |
|---|---|
| 打开网址显示 404 | GitHub 还在部署，等 2 分钟再试，并检查 Settings → Pages。 |
| 海报预览是空白 | 检查 `assets` 文件夹名称和图片文件名是否完全正确。 |
| 下载海报没反应 | 确认是用 GitHub Pages 网址打开，而不是直接打开文件。 |
| 日期或文字位置偏了 | 请记下是哪张海报，找人调整 `index.html` 里的坐标。 |
| 文案里的日期不对 | 检查左边的日期栏位，文案会跟着日期自动更新。 |
| 文字太大、超出框 | 程序会自动缩小字体，如果仍超出，请缩短文字。 |
