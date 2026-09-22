# Phallaina · 星吟

> 以太渡鲸，随星而鸣 — 零碎思绪，于此停泊

个人博客站点，由 Hugo 构建，托管于 GitHub Pages。

## 站点特色

- **银河鲸主题**：首页鲸鱼背景随深浅色主题自动切换（浅色 / 深色各一张）
- **深浅色自动切换**：本地时间 0–5 点默认深色，其余默认浅色；可手动切换并记忆偏好
- **三个栏目**：
  - 星吟 — 随笔漫想
  - 碎片 — 按时间轴排列的零碎记录
  - 关于 — 站点与作者
- **标签 / 分类归档**：按主题检索历史内容
- **中文排版细节**：段首缩进两字、衬线标题字体（Noto Serif SC）、正文 Noto Sans SC
- **响应式布局**：手机端自动适配
- **无障碍**：尊重系统「减少动态效果」偏好

## 更新文章

> 站点源码在**私有仓库**，本仓库仅存放 Hugo 构建产物（由部署脚本自动同步）。
> **请勿手动修改本仓库文件**——每次部署会清空并重建全部内容（README.md 除外）。

### 日常更新（已有本地环境）

1. 编辑 `content/` 下的 Markdown 文件。新文章参考现有文章的 front matter 格式：

   ```yaml
   ---
   title: "文章标题"
   date: 2026-09-22
   categories: ["分类"]
   tags: ["标签"]
   ---
   ```

2. 在源码仓根目录运行部署脚本：

   ```powershell
   powershell -ExecutionPolicy Bypass -File .\deploy.ps1
   ```

   脚本自动完成：Hugo 构建 → 同步产物到本仓库 → 提交 → 推送。

3. 等待 1–2 分钟，站点自动更新。

### 新电脑首次搭建

1. 安装 Git：<https://git-scm.com>
2. 克隆源码仓（**私有**，需 ulanlogin 账号登录；自带 `hugo.exe` 与 `deploy.ps1`，无需另装 Hugo）：

   ```powershell
   git clone https://github.com/ulanlogin/iinorii.github.io.git moments-blog
   ```

3. 克隆本部署仓（**公开**，需 phallaina 账号登录）：

   ```powershell
   git clone https://phallaina@github.com/phallaina/phallaina.github.io.git moments-blog-deploy
   ```

4. 两个文件夹必须**同级**，部署仓目录名保持 `moments-blog-deploy`（部署脚本按此定位）。
5. 之后按「日常更新」流程操作。

### 本地预览

```powershell
cd moments-blog
.\hugo.exe server
```

浏览器打开 <http://localhost:1313/> 预览，确认无误后再部署。

## 技术栈

- [Hugo](https://gohugo.io/) — 静态站点生成器（主题：phallaina-white，自研）
- GitHub Pages — 站点托管（本仓库从 `main` 分支 `/ (root)` 部署）
- 本仓库内容由 `deploy.ps1` 自动同步构建产物；主题、文章与配置源码保存在私有仓库，不对外公开

## 版权

© 2026 Phallaina · 星吟 · 主题与文章内容保留所有权利
