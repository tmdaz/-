# 成长星球 · GitHub Pages 部署说明（永久免费 · 网址固定）

> 这份说明教你把 `index.html` 发布成**永久免费、网址固定**的网站。
> GitHub Pages 对 **Public（公开）仓库**永久免费，无需租服务器、无需信用卡。
> 数据仍存在每个访问者的浏览器本地（老师一人手机即主数据），页面本身不含任何密码/密钥，可安全公开。

---

## 方法 A：网页版上传（最简单，推荐给不熟 Git 的人）

### 1. 注册 / 登录 GitHub
打开 https://github.com ，没有账号就免费注册一个（邮箱注册即可）。

### 2. 新建一个 Public 仓库
- 右上角 `+` → `New repository`
- `Repository name`：随便填，例如 `growth-planet`
- **可见性选 Public（公开）** —— 这是关键，Public 才永久免费
- **不要**勾选 `Add a README file`
- 点 `Create repository`

### 3. 上传文件
进入刚建的仓库页 → `Add file` → `Upload files`：
- 把 **`index.html`** 拖进去（可同时拖入这个 `README.md`）
- 点 `Commit changes`

### 4. 开启 Pages
- 仓库页 → `Settings`（设置）→ 左侧 `Pages`
- `Build and deployment` → `Source` 选择 **`Deploy from a branch`**
- `Branch` 选 **`main`**、目录 `/ (root)` → `Save`

### 5. 得到网址
等 1–2 分钟，刷新 Pages 页面，会显示网址：
```
https://你的用户名.github.io/growth-planet/
```
> 注意：仓库是 Private（私有）时，GitHub Pages 需要升级付费（Pro）。**一定要用 Public 仓库才是免费。**

### 6. 手机打开
老师手机浏览器打开上面的网址即可。数据存在手机浏览器本地，刷新不丢，无需登录就能建造/兑换。

---

## 方法 B：git 命令行（可选，本机已装 Git 才用）

```bash
# 1. 本机新建仓库并提交
git init growth-planet
cd growth-planet
# 把 index.html 放进来
git add index.html
git commit -m "成长星球 v2：8组星球/自定义加分/绘画建造/游客消费-老师加分"

# 2. 关联你刚在 GitHub 建的仓库
git branch -M main
git remote add origin https://github.com/<你的用户名>/<仓库名>.git

# 3. 推送（首次会让你登录 GitHub）
git push -u origin main
```

推送后回到第 4 步：开启 Pages。

---

## 🔁 以后更新怎么发布？
改好 `index.html` 后，GitHub 网页版：进仓库 → `Add file` → `Upload files`，把新文件拖进去覆写 → `Commit`。等 1 分钟，网址不变、内容更新，**老师手机上的数据不会丢**（网址没变）。

---

## ❓ 常见问题
- **网址会失效吗？** GitHub Pages 免费且长期有效，网址固定，适合长期课堂使用（相比临时免费托管不担心到期）。
- **自定义域名？** 可以，但需要在域名商花钱买域名（约 ¥60/年），非必需。
- **学生能看到老师数据吗？** 不能共享——每个人数据存在自己设备本地；老师手机上是班级主数据。
- **数据会丢吗？** 只要老师手机浏览器不清除网站数据就一直在；建议老师定期用「导出报表」备份。
