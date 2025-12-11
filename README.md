# 鼹鼠 & 甲鱼 击打游戏 - 部署指南

这是一个简单的单文件HTML游戏，包含所有CSS和JavaScript代码，无需额外依赖，部署非常简单。

## 部署选项

### 选项1：GitHub Pages（推荐，免费）

1. **创建GitHub账号**
   - 访问 https://github.com 并注册账号

2. **创建新仓库**
   - 登录后，点击右上角的「+」按钮，选择「New repository」
   - 仓库名称可以是 `whack-game` 或其他您喜欢的名称
   - 选择「Public」（公共仓库）
   - 点击「Create repository」

3. **安装Git**
   - 下载并安装Git：https://git-scm.com/downloads
   - 安装完成后，打开命令提示符或终端

4. **上传文件到GitHub**
   - 在命令提示符中，导航到项目文件夹：
     ```bash
     cd c:\Users\m1550\Documents\trae_projects\start
     ```
   - 初始化Git仓库：
     ```bash
     git init
     ```
   - 配置Git用户信息：
     ```bash
     git config --global user.name "您的GitHub用户名"
     git config --global user.email "您的GitHub邮箱"
     ```
   - 添加文件到暂存区：
     ```bash
     git add whack_game.html README.md
     ```
   - 提交文件：
     ```bash
     git commit -m "Initial commit"
     ```
   - 关联到GitHub仓库（替换为您的仓库URL）：
     ```bash
     git remote add origin https://github.com/您的用户名/whack-game.git
     ```
   - 推送文件到GitHub：
     ```bash
     git push -u origin master
     ```

5. **启用GitHub Pages**
   - 进入您的GitHub仓库
   - 点击「Settings」选项卡
   - 向下滚动到「GitHub Pages」部分
   - 在「Source」下拉菜单中，选择「master branch」
   - 点击「Save」
   - 几分钟后，您的网站将在 `https://您的用户名.github.io/whack-game/whack_game.html` 可用

### 选项2：Vercel（免费，更简单）

1. **创建Vercel账号**
   - 访问 https://vercel.com 并使用GitHub账号登录

2. **部署项目**
   - 登录后，点击「New Project」
   - 选择「Import Git Repository」
   - 选择您刚刚创建的GitHub仓库
   - 点击「Import」
   - 保持默认配置，点击「Deploy」
   - 部署完成后，您将获得一个URL，如 `https://whack-game.vercel.app`

### 选项3：Netlify（免费，类似Vercel）

1. **创建Netlify账号**
   - 访问 https://www.netlify.com 并使用GitHub账号登录

2. **部署项目**
   - 登录后，点击「New site from Git」
   - 选择GitHub，并授权Netlify访问您的仓库
   - 选择您的仓库
   - 保持默认配置，点击「Deploy site」
   - 部署完成后，您将获得一个URL，如 `https://whack-game.netlify.app`

### 选项4：本地服务器（仅用于测试）

如果您只想在本地测试，可以使用Python的内置HTTP服务器：

```bash
cd c:\Users\m1550\Documents\trae_projects\start
python -m http.server 8000
```

然后在浏览器中访问 http://localhost:8000/whack_game.html

## 自定义部署

### 修改URL路径

如果您想让游戏在根路径访问（如 `https://您的域名.com/` 而不是 `https://您的域名.com/whack_game.html`），可以将 `whack_game.html` 重命名为 `index.html`。

```bash
ren whack_game.html index.html
```

然后重新上传文件并重新部署。

### 添加自定义域名

大多数托管服务都支持添加自定义域名，您需要：
1. 购买一个域名（如在阿里云、腾讯云、GoDaddy等）
2. 在托管服务的设置中添加自定义域名
3. 在域名注册商处配置DNS记录

具体步骤请参考各托管服务的文档。

## 技术说明

- 这是一个纯前端项目，不需要后端服务器
- 所有代码都包含在一个HTML文件中
- 支持响应式设计，适配不同屏幕尺寸
- 兼容现代浏览器（Chrome、Firefox、Safari、Edge）

## 游戏功能

- 两个可爱的Q版角色：鼹鼠和甲鱼
- 点击按钮或直接点击角色进行击打
- 每次击打获得10分，实时显示分数
- 击打时触发动画效果

祝您游戏愉快！