# Baoning Zhang — Academic Homepage

个人学术主页，基于 [minimal-academic-homepage](https://github.com/Xin-Jiaqi/minimal-academic-homepage) 模板定制。单文件静态站点，无构建步骤、无框架依赖，直接编辑 `index.html` 即可。

访问地址：<https://walterzhang1278.github.io>

## 文件结构

```
.
├── index.html          # 站点全部内容（编辑这个文件即可修改页面）
├── assets/
│   ├── profile-placeholder.svg      # 头像占位图（替换为你的照片）
│   ├── publication-placeholder.svg  # 论文封面占位图
│   └── institution-placeholder.svg  # 机构/校徽占位图
├── tests/validate_template.py       # 模板合法性校验脚本
└── README.md
```

## 本地预览

在仓库根目录运行：

```bash
python -m http.server 8000
```

然后浏览器打开 <http://localhost:8000>。

## 编辑内容

所有文字都在 `index.html` 中，按区块搜索即可修改：

- 顶部导航与 hero 区：姓名、身份、简介、邮箱/GitHub 链接
- `#publications`：发表论文
- `#projects`：项目
- `#experience`：教育与工作经历（时间线）、技能与工具、研究兴趣
- `#notes`：博客/笔记（目前为占位，可按需添加）
- `<footer>`：页脚版权

替换占位图片：把你的照片放到 `assets/` 下，并更新 `index.html` 中对应 `<img src="...">` 的路径即可。SVG 中的文字保持可编辑。

## 部署到 GitHub Pages

本仓库名为 `walterzhang1278.github.io`，属于 GitHub 的 **用户站点（user site）**，部署最简单：

1. **推送代码到 GitHub**

   ```bash
   git add .
   git commit -m "init: personal academic homepage"
   git push origin main
   ```

   （如果默认分支是 `master`，推送到 `master` 也可以，Pages 会自动识别。）

2. **启用 GitHub Pages**

   - 打开仓库页面 → **Settings** → 左侧 **Pages**
   - **Source** 选择 **Deploy from a branch**
   - **Branch** 选择 `main`（或 `master`），目录选 **/(root)**，点击 **Save**
   - 等待 1–2 分钟，页面顶部会显示 `Your site is live at https://walterzhang1278.github.io/`

3. **访问**：<https://walterzhang1278.github.io>

> 用户站点（`<username>.github.io`）会从仓库根目录的 `index.html` 自动发布，无需额外配置。每次 `git push` 后 GitHub Pages 会自动重新部署。

## 校验

修改后可运行模板自带校验：

```bash
python tests/validate_template.py
```
