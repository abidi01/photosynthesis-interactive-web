# GitHub 上传指南

## 📋 准备工作

你的项目已经完成了本地Git初始化，现在需要上传到GitHub。

### ✅ 已完成的步骤
- [x] 创建了 README.md（项目说明文档）
- [x] 创建了 .gitignore（忽略不必要的文件）
- [x] 创建了 LICENSE（MIT开源许可证）
- [x] 初始化了Git仓库
- [x] 添加了所有文件到Git
- [x] 创建了初始提交（36个文件，8090行代码）

---

## 🚀 上传到GitHub的步骤

### 步骤1：在GitHub上创建新仓库

1. **登录GitHub**
   - 访问 https://github.com
   - 登录你的账号

2. **创建新仓库**
   - 点击右上角的 `+` 号
   - 选择 `New repository`（新建仓库）

3. **填写仓库信息**
   - **Repository name**（仓库名称）：`photosynthesis-interactive-web`
     - 或者使用中文名：`光合作用原理探索交互网页`
   - **Description**（描述）：`一个基于纯前端技术开发的交互式生物教学工具，帮助高中生深入理解光合作用的原理和经典实验`
   - **Public/Private**（公开/私有）：选择 `Public`（公开）
   - **⚠️ 重要**：不要勾选以下选项（因为我们已经在本地创建了）：
     - ❌ Add a README file
     - ❌ Add .gitignore
     - ❌ Choose a license

4. **点击 `Create repository`**（创建仓库）

### 步骤2：连接本地仓库到GitHub

创建完仓库后，GitHub会显示一个页面，找到 **"…or push an existing repository from the command line"** 部分。

在你的项目文件夹中打开命令行（CMD或PowerShell），执行以下命令：

```bash
# 添加远程仓库（将下面的 YOUR_USERNAME 替换为你的GitHub用户名）
git remote add origin https://github.com/YOUR_USERNAME/photosynthesis-interactive-web.git

# 设置主分支名称为main（GitHub的默认分支名）
git branch -M main

# 推送到GitHub
git push -u origin main
```

**示例**（假设你的用户名是 `zhangsan`）：
```bash
git remote add origin https://github.com/zhangsan/photosynthesis-interactive-web.git
git branch -M main
git push -u origin main
```

### 步骤3：输入GitHub凭据

首次推送时，系统会要求你输入GitHub凭据：

**方法A：使用Personal Access Token（推荐）**
1. 在GitHub上生成Token：
   - 点击头像 → Settings → Developer settings → Personal access tokens → Tokens (classic)
   - 点击 `Generate new token (classic)`
   - 勾选 `repo` 权限
   - 生成并复制Token
2. 在命令行中：
   - Username: 输入你的GitHub用户名
   - Password: 粘贴刚才复制的Token（不是你的GitHub密码）

**方法B：使用GitHub Desktop（更简单）**
1. 下载并安装 GitHub Desktop
2. 登录你的GitHub账号
3. 选择 `Add` → `Add existing repository`
4. 选择你的项目文件夹
5. 点击 `Publish repository`

### 步骤4：验证上传成功

1. 刷新你的GitHub仓库页面
2. 你应该能看到：
   - ✅ 所有HTML文件
   - ✅ 图片和视频文件夹
   - ✅ CSS和JS文件夹
   - ✅ README.md（会自动显示在页面下方）
   - ✅ LICENSE文件
   - ✅ 技术文档

---

## 🎯 快速命令参考

### 完整的上传命令（复制粘贴使用）

```bash
# 1. 添加远程仓库（替换YOUR_USERNAME为你的用户名）
git remote add origin https://github.com/YOUR_USERNAME/photosynthesis-interactive-web.git

# 2. 重命名分支为main
git branch -M main

# 3. 推送到GitHub
git push -u origin main
```

### 后续更新项目时使用

```bash
# 1. 查看修改的文件
git status

# 2. 添加所有修改
git add .

# 3. 提交修改（修改提交信息）
git commit -m "更新说明"

# 4. 推送到GitHub
git push
```

---

## 📝 常见问题解决

### Q1: 提示 "remote origin already exists"
**解决方法**：
```bash
# 删除现有的远程仓库
git remote remove origin

# 重新添加
git remote add origin https://github.com/YOUR_USERNAME/photosynthesis-interactive-web.git
```

### Q2: 推送失败，提示认证错误
**解决方法**：
- 确保使用Personal Access Token而不是密码
- 或者使用GitHub Desktop

### Q3: 文件太大无法上传
**解决方法**：
- GitHub单个文件限制100MB
- 视频文件如果超过100MB，需要使用Git LFS或者放到其他地方

### Q4: 中文文件名显示乱码
**解决方法**：
```bash
git config --global core.quotepath false
```

---

## 🌟 上传后的操作

### 1. 设置GitHub Pages（可选）

如果你想让别人直接在线访问你的网页：

1. 进入仓库的 `Settings`
2. 找到 `Pages` 选项
3. 在 `Source` 中选择 `main` 分支
4. 点击 `Save`
5. 等待几分钟，你的网页就会发布到：
   `https://YOUR_USERNAME.github.io/photosynthesis-interactive-web/main.html`

### 2. 添加项目标签（Topics）

在仓库首页点击 `Add topics`，添加：
- `education`
- `biology`
- `photosynthesis`
- `interactive`
- `html5`
- `javascript`
- `chinese`

### 3. 编辑仓库描述

在仓库首页点击 `About` 旁边的齿轮图标，添加：
- Description（描述）
- Website（如果设置了GitHub Pages）
- Topics（标签）

### 4. 分享你的项目

复制仓库链接分享给：
- 👨‍🏫 其他老师
- 📚 学生
- 🌐 教育社区

---

## 📊 项目统计

你的项目包含：
- **36个文件**
- **8090行代码**
- **8个HTML实验页面**
- **完整的图片和视频资源**
- **详细的技术文档**
- **MIT开源许可证**

---

## 🎉 恭喜！

完成上传后，你的项目就可以：
- ✅ 在GitHub上公开展示
- ✅ 让其他人下载使用
- ✅ 接受其他人的改进建议
- ✅ 通过GitHub Pages在线访问
- ✅ 版本控制和历史记录

---

## 📞 需要帮助？

如果遇到问题：
1. 查看GitHub官方文档：https://docs.github.com
2. 在仓库中创建Issue
3. 搜索相关错误信息

---

**祝你上传顺利！🚀**