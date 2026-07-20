# Toolchive 运营

工作目录：网站前端 + 工具页面源码
PM：运营平台
全局交接入口：`../../交接总手册.md` ｜ 运营任务清单：`../toolchive-ops/CURRENT-TASKS.md`

---

## ✅ 已完成（2026-07-10 ~ 07-14）

1. **GA4 全站装配** — 59/59 页已装 `G-20L9E9M9KL`，后台已验证有数据（07-13 首次周报：周活 7 用户/38 事件）
2. **AdSense** — 代码 `ca-pub-3907469815607655` 全站已装；**审核已在进行中（"已请求审核"），无需重申**，等 Google 结果
3. **Top10 高曝光页（占全站 78% 曝光）全部优化** — 4 旗舰页功能升级（gravel/pace/insulation/siding）+ 7 页信任块；详见 `../toolchive-ops/竞品审计-2026-07-13.md` 执行记录

## 🔵 当前状态：观察期（2026-07-15 起，2-4 周）

- **不再做 on-page 优化**（线以下 45 页低曝光，低 ROI，见 `../toolchive-ops/页面杠杆地图.md`）
- 每周五 GSC 检查，对比基线（3个月 2,020 曝光 / 0 点击 / 排名 78.4），节奏见 `../toolchive-ops/观察期节奏.md`
- 决策门约 07-29~08-12：旗舰页排名上移 → 评估加码；没动 → 重新诊断
- 外链只用免费功夫（客座文/HARO），不买付费链接

## 🔧 本地开发

- 预览：`python3 -m http.server 8080`（或 .claude/launch.json 的 toolchive-site）
- 发布：push 到 GitHub main → 自动部署 toolchive.com
- 项目级工作流命令：`.claude/commands/`（seo-check / deploy-check / adsense-check 等）

## 质量红线

- 文案承诺的功能必须真实存在（L2 一致性）
- 方法论/来源真实可查，署名用 "Toolchive Team" 不虚构专家
- 新内容上线前过 `../../通用质量检测框架.md` 六层检查

---

**更新：** 2026-07-15
