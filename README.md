# 哑铃选股策略 · 真实调仓记录

公开页面：https://marvinxu-free.github.io/barbell-portfolio/

- `index.html` 单页应用（vanilla JS + inline SVG，无外部依赖），读 `data/*.js`
- `data/live.js` 每期调仓记录 + 结算净值（由 `live/export_js.py` 生成）
- `data/data.js` 2026-11 期次筛选快照（六层漏斗 / 估值双口径 / 模拟路径）
- `data/backtest.js` 真实月线回测（仓位机制对比，已扣费）
- `history/` 原始数据：`periods/*.json`（每期筛选结果、权重、成交单）、`ledger.jsonl`（结算账本）、`state.json`

每月首个交易日自动重跑六层筛选并再平衡，页面随每次调仓更新；历史期次全部保留。
