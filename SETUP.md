# 🚀 硅基侵略 - 部署步骤

解压后，按以下步骤操作（约 10 分钟完成）。

---

## 第一步：安装 Hugo Extended

**macOS：**
```bash
brew install hugo
```

**Windows：**
```bash
scoop install hugo-extended
# 或
winget install Hugo.Hugo.Extended
```

验证（输出须含 extended）：
```bash
hugo version
```

---

## 第二步：初始化项目并安装主题

进入解压后的 `silicon-blog` 目录，依次运行：

```bash
# 初始化 git 仓库
git init

# 安装 PaperMod 主题（子模块方式）
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

---

## 第三步：本地预览（可选）

```bash
hugo server
```

打开 http://localhost:1313 查看效果。确认没问题后 Ctrl+C 停止。

---

## 第四步：在 GitHub 创建仓库

1. 登录 GitHub，点右上角 **+** → **New repository**
2. 仓库名必须为：`Auroralalaa.github.io`
3. 设为 **Public**
4. **不要**勾选任何初始化选项，直接点 Create

---

## 第五步：推送代码

```bash
git add .
git commit -m "init: 初始化硅基侵略博客"
git branch -M main
git remote add origin https://github.com/Auroralalaa/Auroralalaa.github.io.git
git push -u origin main
```

---

## 第六步：开启 GitHub Pages

1. 打开仓库页面 → **Settings** → **Pages**
2. Source 选择 **GitHub Actions**
3. 保存

等待约 1-2 分钟，访问：
👉 **https://Auroralalaa.github.io**

---

## 日常写作

```bash
# 新建文章
hugo new content/posts/文章名.md

# 编辑文章，将 draft: false，写入内容

# 发布
git add .
git commit -m "post: 文章标题"
git push
```

push 后约 1 分钟自动上线。
