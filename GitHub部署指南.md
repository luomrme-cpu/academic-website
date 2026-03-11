# 学术网站 GitHub Pages 部署指南

## 概述
这个指南将帮助你将学术个人网站部署到 GitHub Pages，让全世界都能访问你的学术主页。

## 前提条件
- 已有 GitHub 账号
- 安装了 Git
- 项目代码已准备好

## 步骤一：创建 GitHub 仓库

1. **登录 GitHub**
   - 访问 [github.com](https://github.com)
   - 登录你的账号

2. **创建新仓库**
   - 点击右上角的 "+" → "New repository"
   - 填写仓库信息：
     - **Repository name**: `academic-website` (建议与项目名一致)
     - **Description**: `主页` (可选)
     - **Public** (选择 Public，因为 GitHub Pages 免费版只支持公开仓库)
     - **Initialize with README**: 勾选
   - 点击 "Create repository"

## 步骤二：推送代码到 GitHub

1. **打开终端/命令提示符**
   - 导航到你的项目目录：
     ```bash
     cd d:\ccteat\academic-website
     ```

2. **初始化 Git 仓库**
   ```bash
   git init
   ```

3. **添加远程仓库**
   ```bash
   git remote add origin https://github.com/你的用户名/academic-website.git
   ```
   将 `你的用户名` 替换为你的 GitHub 用户名

4. **添加文件到暂存区**
   ```bash
   git add .
   ```

5. **提交代码**
   ```bash
   git commit -m "初始提交：学术个人网站"
   ```

6. **推送到 GitHub**
   ```bash
   git branch -M main
   git push -u origin main
   ```

## 步骤三：启用 GitHub Pages

1. **进入仓库设置**
   - 访问你的仓库页面：`https://github.com/你的用户名/academic-website`
   - 点击 "Settings" 标签

2. **启用 GitHub Pages**
   - 在左侧菜单找到 "Pages"
   - 在 "Source" 部分：
     - 选择 "Deploy from a branch"
     - Branch 选择 "main"
     - Directory 选择 "/ (root)"
   - 点击 "Save"

3. **等待部署完成**
   - 通常需要 1-3 分钟
   - 部署完成后，你会看到你的网站地址
   - 网站地址格式：`https://你的用户名.github.io/academic-website`

## 步骤四：上传论文附件

如果你想在网站上提供论文附件，请按照以下步骤：

1. **创建 papers 文件夹**
   ```bash
   mkdir papers
   ```

2. **上传 PDF 文件**
   - 将你的论文 PDF 文件复制到 `papers` 文件夹
   - 例如：`paper1.pdf`, `paper2.pdf`, `paper3.pdf`

3. **提交并推送**
   ```bash
   git add papers/
   git commit -m "添加论文附件"
   git push origin main
   ```

## 如何分享你的项目

### 1. 分享网站链接
直接发送 GitHub Pages 的地址给别人：
```
https://你的用户名.github.io/academic-website
```

### 2. 分享项目代码
发送 GitHub 仓库地址：
```
https://github.com/你的用户名/academic-website
```

### 3. 在简历或邮件中添加链接
```
个人学术主页：https://你的用户名.github.io/academic-website
GitHub：https://github.com/你的用户名/academic-website
```

## 更新网站内容

当你需要更新网站内容时：

1. **修改 HTML 文件**
2. **提交更改**
   ```bash
   git add .
   git commit -m "更新网站内容"
   git push origin main
   ```

3. **等待 GitHub 重新部署**（通常 1-3 分钟）

## 常见问题

### Q: GitHub Pages 不显示更新怎么办？
A:
1. 确保代码已推送到 main 分支
2. 检查 GitHub Pages 设置是否正确
3. 等待 5-10 分钟
4. 清除浏览器缓存

### Q: 如何自定义域名？
A:
1. 在仓库 Settings → Pages 中设置自定义域名
2. 需要购买并配置域名解析

### Q: 如何使用个人域名而非 GitHub.io？
A: 可以购买域名并 CNAME 指向 GitHub Pages

## 高级配置

### 1. 添加 404 页面
在项目根目录创建 `404.html` 文件

### 2. 添加网站图标
在 `public` 文件夹放置 `favicon.ico`

### 3. 添加 robots.txt
在项目根目录创建 `robots.txt` 文件

### 4. 添加 analytics
可以在 HTML 中添加 Google Analytics 或其他统计代码

---

祝你部署顺利！如有问题，请查看 [GitHub Pages 官方文档](https://docs.github.com/en/pages)。