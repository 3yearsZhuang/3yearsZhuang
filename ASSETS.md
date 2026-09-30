# README 素材与部署说明

本目录是 GitHub Profile 仓库（**仓库名必须与用户名相同**：`3yearsZhuang`）。

## 一、部署步骤

1. 在 GitHub 新建一个**公开**仓库，名字填 `3yearsZhuang`（与用户名完全一致，大小写也要一致）。
2. 把本目录的 `README.md` 推送到该仓库的 `main` 分支根目录。
3. 访问 `https://github.com/3yearsZhuang` —— 这份 README 会自动显示在主页顶部。

```bash
cd /Users/3yearszhuang/Documents/Z-Projects/3yearsZhuang
git init -b main
git add README.md ASSETS.md
git commit -m "docs: add profile README"
git remote add origin https://github.com/3yearsZhuang/3yearsZhuang.git
git push -u origin main
```

## 二、必须替换的占位符

README 中有 **2 处占位符**，上线前请替换（目前点击会 404）：

| 占位符 | 位置 | 替换为 |
|---|---|---|
| `https://space.bilibili.com/你的UID` | 顶部徽章「Bilibili」 | 你的 Bilibili 主页，例如 `https://space.bilibili.com/12345678` |
| `https://你的博客地址` | 顶部徽章「Blog」 | 你的博客地址，例如 `https://blog.example.com` |

如果暂时没有博客，直接删掉那一个 `<a>...</a>` 徽章块即可，其余内容不受影响。

## 三、可选：本地上传 Banner（更稳、更好看）

目前顶部用的是 **readme-typing-svg** 动态打字标题（无需素材，已可用）。
如果想换成 jiyun233 / witchscottishfoldcat 那样的**立绘 Banner 图**：

1. 在本仓库建 `assets/` 目录，放入 `hero.png`（建议宽 1600–2000px，高 400–500px，深色半透明背景）。
2. 把 README 顶部那个 `<div align="center"> ... </div>` 整块替换为：

```html
<p align="center">
  <img src="https://raw.githubusercontent.com/3yearsZhuang/3yearsZhuang/main/assets/hero.png" alt="3yearsZhuang banner" />
</p>
```

> 用相对路径 `./assets/hero.png` 也可以，但绝对链接在别人 fork 或镜像站浏览时更稳。

## 四、关于第三方统计服务

| 服务 | 用途 | 状态 |
|---|---|---|
| `github-readme-stats.vercel.app` | 数据卡片、语言分布 | ✅ 已实测 200 |
| `github-readme-streak-stats.herokuapp.com` | 连续贡献天数 | ✅ 已实测 200 |
| `komarev.com/ghpvc` | 访客计数 | ✅ 已实测 200 |
| `img.shields.io` | 徽章 | ✅ 已实测 200 |
| `count.getloli.com` | 二次元访客计数器 | ⚠️ 已**移除**：该服务对直接请求返回 403，不够稳定，故未采用 |

这些统计卡片的 `count_private=true` 只会统计**你已授权的私有仓库提交**，需要在
[GitHub 授权页](https://github.com/settings/authorizations) 给对应 Vercel 应用授权后才会显示私有贡献。

## 五、内容准确性备注

README 中提到的项目均取自你本地工作区的真实工程，未做夸大：

- **Aervox ｜ 思隅** —— `Aervox-harness`，公开仓库，描述与项目 README 表述一致。
- **WitchDrawer** —— 公开仓库，技术栈 `net10.0` / WPF，已核对 `.csproj`。
- **Z.Env** —— 公开仓库，Rust + Tauri + React，已核对 `package.json` 依赖。
- **CS-Web-Project** —— 公开仓库「希望之峰学院计算机协会官网」。
- **Index 学习岛（IndexNya）** —— ⚠️ 目前**不是公开仓库**，因此只在「关于」正文中顺带提及，
  未做成带链接的项目卡片；等仓库公开后可以补一张卡片。