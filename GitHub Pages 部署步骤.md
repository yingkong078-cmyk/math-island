# GitHub Pages 公网部署步骤

> 你要上传的是 `GitHub-Pages-部署包.zip` 解压后的 `github-pages` 文件夹**里的内容**，不是整个压缩包，也不是 `math-island` 外层文件夹。

## 一、准备

1. 下载并解压 `GitHub-Pages-部署包.zip`
2. 解压后应该看到：
   - `index.html`
   - `qr-public.html`
   - `assets/`
   - `css/`
   - `js/`
3. 注册 / 登录 GitHub：<https://github.com>

> 如果不想公开孩子的照片：上传前把 `assets/avatar.jpg` 换成一张方形卡通图，文件名仍然是 `avatar.jpg`。网页不需要改代码。

## 二、新建仓库

1. 登录 GitHub，点右上角 `+` → `New repository`
2. 仓库名填一个英文名，例如 `math-island`
3. 选择 **Public**（免费 Pages 需要公开仓库）
4. 不需要勾选 README、.gitignore、license
5. 点 `Create repository`

## 三、上传文件（网页上传，最简单）

1. 进入刚建好的仓库
2. 点 `Add file` → `Upload files`
3. 打开解压后的 `github-pages` 文件夹
4. 全选里面的内容：`index.html`、`qr-public.html`、`assets`、`css`、`js`
5. 直接拖进 GitHub 的上传区域
6. 确认页面上能看到 `index.html`，并且它**在仓库根目录**，不是在 `github-pages/` 子目录里
7. 下面填写提交说明，例如 `deploy math island`
8. 点 `Commit changes`

> 如果拖拽文件夹失败，可以用 GitHub Desktop：
> 安装 GitHub Desktop → 登录 → File → Add local repository → 选择 `github-pages` 文件夹 → 按提示创建仓库 → Publish repository（取消勾选 private）。

## 四、开启 GitHub Pages

1. 进入仓库的 `Settings`
2. 左侧点 `Pages`
3. `Build and deployment` 的 `Source` 选择 **Deploy from a branch**
4. `Branch` 选择 `main`，文件夹选择 `/ (root)`
5. 点 `Save`
6. 等待 1～3 分钟，刷新页面
7. 顶部会出现网址，例如：

```text
https://你的用户名.github.io/math-island/
```

8. 用浏览器打开这个网址，检查首页、头像、声音、动画是否正常

## 五、生成公网二维码

部署成功后，在同一个网址后面加上 `qr-public.html`：

```text
https://你的用户名.github.io/math-island/qr-public.html
```

打开后会自动生成当前公网网址的二维码。截图保存、打印，或直接让家人扫码即可。

> 如果二维码页提示“当前是本地文件预览”，说明还没有通过 `https://...github.io/...` 打开，请确认 Pages 已上线。

## 六、以后更新内容

- 修改本地网页后，在 GitHub 仓库里重新上传改动的文件，提交即可
- Pages 会自动重新发布，通常 1 分钟左右生效
- 如果页面没变化，按 `Ctrl + F5` 强制刷新，或等一会儿

## 七、常见问题

### 打开是 404

- 确认 `index.html` 在仓库根目录
- 确认 Settings → Pages 已选择 `main` 和 `/ (root)`
- 刚开启 Pages 需要等 1～3 分钟

### 页面没有样式 / 动画

- 检查仓库里是否有 `css/style.css`、`js/app.js` 等文件
- 必须保持 `css/`、`js/`、`assets/` 文件夹结构与 `index.html` 同级

### 仓库必须公开吗

- 免费账号的 GitHub Pages 通常要求公开仓库
- 如果不想公开源码，可以改用带访问控制的托管方案

### 照片隐私

- 公网页面和公开仓库里的 `assets/avatar.jpg` 任何人都能看到
- 最稳妥的做法是上传前换成卡通头像
- 不要把公网链接发到公开群聊、论坛或社交平台

### 学习进度会同步吗

不会自动同步。三台设备各自保存在本机浏览器中。  
在“成长 → 设置与数据”里可以导出 JSON 备份，再到另一台设备导入。
