# Toolchive 运营

工作目录：网站前端 + 工具页面源码  
PM：运营平台  
上一级任务清单：`../toolchive-ops/CURRENT-TASKS.md`

---

## 🔴 当前优先任务

### GA4 全站装配 + AdSense 内容充实

**状态：进行中** (2026-07-10)

**关键目标：**
1. **GA4 装配** — 在所有 HTML 页面 `<head>` 末尾装入追踪代码
   - 测量ID：`G-20L9E9M9KL`
   
2. **AdSense 内容充实** — 优先页面（按 GSC 曝光排序）
   - pace-calculator (~72 曝光)
   - gravel-calculator (~64 曝光)
   - insulation-calculator (21 曝光)
   - siding-calculator (21 曝光)

   每页充实内容：长尾变体 + How-to + FAQ + 成本表格 + JSON-LD schema（500+ 字）

**完成后：** Commit + push → 通知 PM → 用户检查 GA4 数据 → AdSense 重新申请

---

## 📂 快速导航

- **网站源码：** `./` (HTML/CSS/JS)
- **任务详情：** `../toolchive-ops/CURRENT-TASKS.md`
- **运营数据：** `../toolchive-ops/`（配置、脚本、数据监控）

---

## 🔧 本地开发

```bash
# 启动本地服务器（如配置）
npm run dev

# 查看所有工具和页面
ls -la ./
```

---

**更新：** 2026-07-10  
**PM：** 等待 GA4 + 内容充实完成后的 AdSense 重申
