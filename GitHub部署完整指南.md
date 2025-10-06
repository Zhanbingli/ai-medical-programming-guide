# 🚀 GitHub Pages 自动部署完整指南

## ✅ 已完成的准备工作

- ✅ GitHub Actions 配置文件已创建（`.github/workflows/deploy.yml`）
- ✅ 本地构建测试成功
- ✅ 项目结构完整

## 📝 部署步骤（从零开始）

### 第 1 步：初始化 Git 仓库（如果还没有）

```bash
# 在项目目录下
cd /Users/lizhanbing12/ai-book

# 初始化 Git
git init

# 添加所有文件
git add .

# 首次提交
git commit -m "初始提交：AI时代医学工作者编程实战指南"
```

### 第 2 步：在 GitHub 创建仓库

1. **打开浏览器**，访问：https://github.com/new

2. **填写仓库信息**：
   - Repository name: `ai-medical-programming-guide`（或你喜欢的名字）
   - Description: `AI时代医学工作者编程实战指南 - 从零基础到AI辅助编程`
   - Public（公开）或 Private（私有）都可以
   - ⚠️ **不要勾选** "Add a README file"
   - ⚠️ **不要勾选** "Add .gitignore"
   - ⚠️ **不要勾选** "Choose a license"

3. **点击** "Create repository"

### 第 3 步：推送代码到 GitHub

复制 GitHub 显示的命令，或使用以下命令（替换成你的用户名）：

```bash
# 添加远程仓库（替换 YOUR_USERNAME）
git remote add origin https://github.com/YOUR_USERNAME/ai-medical-programming-guide.git

# 重命名分支为 main
git branch -M main

# 推送代码
git push -u origin main
```

**示例**：
```bash
# 如果你的 GitHub 用户名是 lizhanbing12
git remote add origin https://github.com/lizhanbing12/ai-medical-programming-guide.git
git branch -M main
git push -u origin main
```

> 💡 **提示**：首次推送可能需要输入 GitHub 用户名和密码（或 Personal Access Token）

### 第 4 步：启用 GitHub Pages

推送代码后，需要在 GitHub 仓库中启用 Pages：

1. **进入仓库页面**
   - 访问：`https://github.com/YOUR_USERNAME/ai-medical-programming-guide`

2. **点击 Settings**（设置）
   - 在仓库顶部菜单栏找到 "Settings"

3. **找到 Pages 设置**
   - 左侧菜单找到 "Pages"
   - 或直接访问：`https://github.com/YOUR_USERNAME/ai-medical-programming-guide/settings/pages`

4. **配置 Source**
   - Source: 选择 **GitHub Actions**（不是 Deploy from a branch）
   - 点击 Save（保存）

### 第 5 步：等待自动部署

1. **查看部署进度**
   - 点击仓库顶部的 "Actions" 标签
   - 你会看到 "Deploy GitBook to GitHub Pages" 工作流正在运行
   - 通常需要 1-3 分钟完成

2. **部署成功后**
   - Actions 页面会显示绿色的 ✓
   - 返回 Settings → Pages
   - 你会看到：
     ```
     Your site is live at https://YOUR_USERNAME.github.io/ai-medical-programming-guide/
     ```

3. **访问你的网站**
   - 点击链接或直接访问：
   - `https://YOUR_USERNAME.github.io/ai-medical-programming-guide/`

## 🔄 后续更新流程

每次修改内容后，只需要：

```bash
# 1. 查看修改
git status

# 2. 添加修改的文件
git add .

# 3. 提交修改
git commit -m "更新：描述你的修改"

# 4. 推送到 GitHub
git push
```

**推送后，GitHub Actions 会自动**：
1. 检测到代码变化
2. 运行构建流程
3. 部署到 GitHub Pages
4. 1-3 分钟后网站自动更新

## 🔧 常见问题排查

### ❌ 问题 1：推送失败，提示权限错误

**错误信息**：
```
remote: Permission to xxx denied
fatal: unable to access 'https://github.com/...'
```

**解决方法**：

**方法 A：使用 Personal Access Token（推荐）**

1. 访问 https://github.com/settings/tokens
2. 点击 "Generate new token" → "Generate new token (classic)"
3. 设置：
   - Note: `ai-book-deploy`
   - Expiration: 90 days（或 No expiration）
   - 勾选：`repo`（所有权限）
4. 点击 "Generate token"
5. **复制 token**（只显示一次！）

然后推送时：
```bash
# 使用 token 作为密码
git push

# 或者配置到远程地址
git remote set-url origin https://YOUR_TOKEN@github.com/YOUR_USERNAME/ai-medical-programming-guide.git
git push
```

**方法 B：使用 SSH**

1. 生成 SSH 密钥：
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

2. 添加到 GitHub：
   - 复制公钥：`cat ~/.ssh/id_ed25519.pub`
   - 访问 https://github.com/settings/keys
   - 点击 "New SSH key"，粘贴公钥

3. 修改远程地址：
```bash
git remote set-url origin git@github.com:YOUR_USERNAME/ai-medical-programming-guide.git
git push
```

---

### ❌ 问题 2：GitHub Actions 运行失败

**检查方法**：

1. 点击 Actions 标签
2. 点击失败的工作流
3. 查看红色 ✗ 的步骤
4. 展开查看错误信息

**常见原因**：

**原因 1：Node.js 版本问题**
- 检查 `.github/workflows/deploy.yml` 中 `node-version: '18'`
- 改成 `'16'` 或 `'20'` 试试

**原因 2：依赖安装失败**
- 查看 `package.json` 和 `package-lock.json` 是否都已提交
- 确保本地 `npm install` 能成功

**原因 3：构建失败**
- 检查本地 `npm run build` 能否成功
- 查看是否有语法错误的 markdown 文件

---

### ❌ 问题 3：网站显示 404

**原因**：Pages 还未启用或配置错误

**解决**：

1. 进入 Settings → Pages
2. 确认 Source 选择的是 **GitHub Actions**
3. 如果不是，改为 GitHub Actions 并保存
4. 重新触发部署：
```bash
git commit --allow-empty -m "触发重新部署"
git push
```

---

### ❌ 问题 4：网站访问很慢或样式丢失

**原因**：资源路径问题

**解决**：修改 `book.json`，添加：

```json
{
  "root": "./",
  "title": "AI时代医学工作者编程实战指南",
  ...
}
```

然后重新推送。

---

### ❌ 问题 5：修改后网站没更新

**检查清单**：

1. **确认代码已推送**
```bash
git log --oneline -1  # 查看最新提交
git push  # 重新推送
```

2. **检查 Actions 是否运行**
   - 访问 Actions 标签
   - 确认有新的工作流运行

3. **清除浏览器缓存**
   - Mac: `Cmd + Shift + R`
   - Windows: `Ctrl + Shift + R`

4. **等待几分钟**
   - GitHub Pages CDN 可能需要 5-10 分钟刷新

---

## 🎯 验证部署成功

访问你的网站后，检查：

- [ ] 首页正常显示
- [ ] 左侧目录可以展开
- [ ] 点击章节可以跳转
- [ ] 搜索功能正常
- [ ] 代码高亮正常
- [ ] 图片正常显示（如果有）

## 📊 部署成功后的 URL 格式

```
https://[你的用户名].github.io/[仓库名]/
```

**示例**：
- 用户名：`lizhanbing12`
- 仓库名：`ai-medical-programming-guide`
- URL：`https://lizhanbing12.github.io/ai-medical-programming-guide/`

## 🌟 进阶配置（可选）

### 1. 自定义域名

如果你有自己的域名（如 `aimedbook.com`）：

1. 在 Settings → Pages → Custom domain 输入域名
2. 在域名服务商添加 CNAME 记录：
   ```
   CNAME  www  YOUR_USERNAME.github.io
   ```
3. 等待 DNS 生效（几分钟到几小时）

### 2. 启用 HTTPS

GitHub Pages 自动提供 HTTPS，如果使用自定义域名：

1. 在 Settings → Pages
2. 勾选 "Enforce HTTPS"

### 3. 添加 README

在仓库根目录创建 `README.md`（不会影响电子书）：

```markdown
# AI时代医学工作者编程实战指南

在线阅读：https://YOUR_USERNAME.github.io/ai-medical-programming-guide/

## 简介

这是一本帮助医学生和医生学习 AI 辅助编程的实战指南...
```

## 📝 完整操作清单

复制这个清单，逐项完成：

```
□ 1. 初始化 Git 仓库（git init）
□ 2. 在 GitHub 创建仓库（不勾选任何选项）
□ 3. 添加远程仓库（git remote add origin）
□ 4. 推送代码（git push -u origin main）
□ 5. 进入 Settings → Pages
□ 6. Source 选择 "GitHub Actions"
□ 7. 等待 Actions 运行完成（1-3分钟）
□ 8. 访问 https://YOUR_USERNAME.github.io/ai-medical-programming-guide/
□ 9. 验证网站正常显示
□ 10. 后续修改只需 git add/commit/push
```

## 🎉 完成！

如果以上步骤都成功，你的电子书已经在线发布了！

**后续只需要**：
1. 修改 `.md` 文件
2. `git add .`
3. `git commit -m "更新内容"`
4. `git push`
5. 等待 1-3 分钟自动部署完成

---

## 💡 快速命令参考

```bash
# 查看状态
git status

# 添加所有修改
git add .

# 提交修改
git commit -m "更新第X章内容"

# 推送到 GitHub（触发自动部署）
git push

# 查看提交历史
git log --oneline

# 查看远程仓库
git remote -v

# 强制重新部署（空提交）
git commit --allow-empty -m "重新部署"
git push
```

---

需要帮助？
- 检查 [GitHub Actions 日志](https://github.com/YOUR_USERNAME/ai-medical-programming-guide/actions)
- 访问 [GitHub Pages 文档](https://docs.github.com/pages)
- 或联系我获取支持

**祝部署顺利！** 🚀
