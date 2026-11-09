# 部署到 GitHub Pages（你的部分 ≈ 5 分钟）

> 本目录（`pivot/cmm/site/`）就是仓库根目录，已是完整的 Jekyll 站点：GitHub Pages 原生渲染，无需本地装任何东西。
> 免费额度（官方 soft limit）：带宽 100GB/月、站点 ≤1GB、每小时 10 次构建——对现在的流量是天文数字。

## 方式 A：零命令行（推荐第一次）

1. 注册/登录 **github.com**
2. 右上角 **+** → **New repository**：
   - 名称：`china-model-monitor`（Public，免费要求公开仓库）
   - 不要勾选 README 初始化
3. 仓库页点 **"uploading an existing file"** 链接 → 把 `site/` 文件夹里的**全部内容**（含 `_config.yml`、`_layouts`、各子文件夹）拖进去 → **Commit changes**
4. **Settings → Pages** → Build and deployment → Source 选 **Deploy from a branch** → Branch 选 `main` / `(root)` → Save
5. 等 1–2 分钟，回到 Pages 页顶部会显示网址：`https://你的用户名.github.io/china-model-monitor/`

## 方式 B：git 命令（以后更新更快）

```bash
cd D:\work\doIT\pivot\cmm\site
git init && git add -A && git commit -m "launch"
git branch -M main
git remote add origin https://github.com/你的用户名/china-model-monitor.git
git push -u origin main
```

以后每周五扫描出变更后，更新只需：

```bash
git add -A && git commit -m "weekly sweep" && git push
```

## 绑定你自己的域名（推荐，免费 + 自动 HTTPS）

1. 域名 DNS 面板加 4 条 **A 记录**（根域 `@`）：
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
   （或加一条 CNAME：`www` → `你的用户名.github.io`）
2. 在仓库根目录建一个文件 `CNAME`（无扩展名），内容一行：`你的域名.com`
3. Settings → Pages → Custom domain 填入域名 → 勾选 **Enforce HTTPS**（证书签发要等几分钟）

## 上线检查

- [ ] 打开首页，表格六行齐全，Kimi/SiliconFlow 显示 ⚠️ TBD（这是特性不是 bug）
- [ ] `/providers/`、`/changes/`、`/about/`、两篇 `/guides/...` 都能打开
- [ ] 每个页面底部有 "Last verified" 日期
- [ ] （绑域名后）HTTPS 锁标志正常

## 注意（诚实条款）

GitHub ToS 规定 Pages 不得用于"以商业交易为主"的网站（电商等）。纯信息站 + 少量 affiliate 标注链接在实践里普遍托管于 Pages，但**若未来把站做成重商业形态，建议迁到 Cloudflare Pages（同样免费）**——迁移 = 换个仓库平台，文件不变。
