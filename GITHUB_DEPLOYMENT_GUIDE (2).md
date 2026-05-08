# 🚀 GitHub Pages 部署指南

## ⚡ 快速部署（3 步）

### 第一步：准备文件
1. 将 `index.html` 放在你本地电脑的一个文件夹中
2. 文件名**必须**是 `index.html`（你的文件是 `tear-healing-v3.html`，要改名）

### 第二步：创建 GitHub 仓库
1. 登录 GitHub: https://github.com
2. 点击右上角 **+** → **New repository**
3. 仓库名可以取：`tear-healing` 或任意名称
4. **Public**（公开）
5. 点击 **Create repository**

### 第三步：上传文件到 GitHub
有两种方法：

#### **方法 A：用网页界面（最简单）**
1. 打开你刚创建的仓库
2. 点击 **Add file** → **Upload files**
3. 拖拽 `index.html` 上传
4. 下面 Commit message 填写：`Deploy tear-healing`
5. 点击 **Commit changes**

#### **方法 B：用 Git 命令（推荐）**
```bash
# 1. 克隆仓库
git clone https://github.com/YOUR_USERNAME/tear-healing.git
cd tear-healing

# 2. 复制 index.html 到这个文件夹
# （Windows 用文件管理器拖拽，Mac/Linux 用：）
cp ~/Downloads/index.html .

# 3. 提交并推送
git add index.html
git commit -m "Deploy tear-healing"
git push origin main
```

### 第四步：启用 GitHub Pages
1. 打开你的仓库设置：`https://github.com/YOUR_USERNAME/tear-healing/settings`
2. 左侧菜单找到 **Pages**
3. **Source** 下选择：**Deploy from a branch**
4. 选择分支：**main**（默认）
5. 点击 **Save**
6. 等待 1-3 分钟

### ✅ 部署完成！
访问你的网站：`https://YOUR_USERNAME.github.io/tear-healing`

> 注意：将 `YOUR_USERNAME` 替换为你的 GitHub 用户名

---

## 🔍 如果显示空白页面

### 1. 检查 URL 是否正确
```
https://YOUR_USERNAME.github.io/tear-healing
```

### 2. 打开浏览器控制台检查错误
- **Windows/Linux**: 按 `F12`
- **Mac**: 按 `Cmd + Option + I`
- 查看 **Console** 标签，看有没有红色错误

### 3. 最常见的问题

**❌ 显示 404 或空白页**
- 检查 URL 中的用户名是否正确
- 确认 `index.html` 已上传到仓库
- 等待 3-5 分钟让 GitHub 完成部署

**❌ 页面加载但无内容**
- 打开控制台看外部资源（MediaPipe、Google Fonts）是否加载失败
- 如果是 CDN 错误，刷新页面重试

**❌ 摄像头不工作**
- 点击地址栏左边的摄像头权限图标
- 选择 **Allow** 允许网页访问摄像头

### 4. 清除缓存重试
- **Windows/Linux**: `Ctrl + Shift + Delete`
- **Mac**: `Cmd + Shift + Delete`

---

## 📁 推荐的文件结构

```
tear-healing/
├── index.html          ← 你的文件
├── README.md           ← 可选：项目说明
└── .gitignore          ← 可选：忽略配置
```

---

## 🔄 以后如何更新网站

编辑 `index.html` 后：

```bash
git add index.html
git commit -m "Update: 你的修改说明"
git push origin main
```

等待 1-2 分钟，刷新网页就能看到更新。

---

## 💡 重要提示

✅ **文件名必须是** `index.html`
✅ **GitHub Pages 需要 Public 仓库**
✅ **文件内容完全不改，只是上传**
✅ **CDN 资源（MediaPipe、Google Fonts）会自动从网络加载**

---

## 🎯 遇到问题？

1. **检查控制台错误** (F12 → Console)
2. **确认文件名是 index.html**
3. **确认 GitHub Pages 已启用**
4. **清除浏览器缓存后重试**
5. **等待 3-5 分钟重新部署**

---

**祝你部署成功！** 🎉

如有疑问，请告诉我具体的错误信息。
