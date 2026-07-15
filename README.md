[README_3.md](https://github.com/user-attachments/files/29875327/README_3.md)
# VIP Admin Prototype

商户财务/出款审核后台 与 VIP 客户端页面的交互原型及产品需求文档合集。

所有 `.html` 文件均为可直接在浏览器中打开的静态原型（含模拟数据与交互逻辑），无需安装依赖。GitHub 本身不会直接渲染 HTML，如果想**点击即预览**而不是看源码，可以用下面「预览」列的链接（通过 [htmlpreview.github.io](https://htmlpreview.github.io) 转发渲染）。

## 📄 文件目录

| 分类 | 文件 | 说明 | 源码 | 预览 |
| --- | --- | --- | --- | --- |
| VIP 客户端 | `VIP客户端页面迭代原型0707改.html` | VIP 客户端页面迭代原型（0707 更新版） | [查看源码](./VIP客户端页面迭代原型0707改.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/VIP客户端页面迭代原型0707改.html) |
| VIP 客户端 | `VIP客户端页面迭代原型PRD.html` | VIP 客户端页面迭代原型对应的产品需求文档 | [查看源码](./VIP客户端页面迭代原型PRD.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/VIP客户端页面迭代原型PRD.html) |
| 管理后台 | `VIP管理后台交互设计稿0707改.html` | VIP 管理后台交互设计稿（0707 更新版） | [查看源码](./VIP管理后台交互设计稿0707改.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/VIP管理后台交互设计稿0707改.html) |
| 管理后台 | `VIP管理后台产品需求文档PRD0707改.html` | VIP 管理后台产品需求文档（0707 更新版） | [查看源码](./VIP管理后台产品需求文档PRD0707改.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/VIP管理后台产品需求文档PRD0707改.html) |
| 出款/代付 | `merchant_finance_app_1.html` | 商户财务管理后台原型：待审核出款订单 / 已审核出款订单 / 总出款记录 / 提现管理（自动代付配置）/ 代付商户管理，五个页面整合在同一个文件中 | [查看源码](./merchant_finance_app_1.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/merchant_finance_app_1.html) |
| 出款/代付 | `withdrawal_and_autopay_PRD.html` | 上述出款与自动代付模块对应的产品需求文档（PRD） | [查看源码](./withdrawal_and_autopay_PRD.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/withdrawal_and_autopay_PRD.html) |
| 返水 | `rebate_prototype.html` | 返水（Rebate）模块交互原型：返水首页（场馆列表 + 进度条）/ 场馆返水详情页 / Receber 领取确认弹窗 / 历史记录页，并支持「次日领取」「实时领取」两种后台配置模式预览切换 | [查看源码](./rebate_prototype.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/rebate_prototype.html) |
| 返水 | `rebate_prd.html` | 返水（Rebate）模块产品需求文档 | [查看源码](./rebate_prd.html) | [在线预览](https://htmlpreview.github.io/?https://github.com/kyobatian-wq/vip-admin-prototype/blob/main/rebate_prd.html) |

> 「预览」链接依赖第三方服务 htmlpreview.github.io 实时拉取仓库文件渲染，仓库需保持 **Public**，且文件更新后预览会自动同步（可能有几分钟缓存延迟）。

## 🗂 模块说明（出款/代付部分）

`merchant_finance_app_1.html` 内部通过顶部标签页 + 左侧菜单在以下 5 个子页面间切换：

1. **待审核出款订单** — 审核员处理会员提现申请的工作台（锁定/拒绝/罚没/人工完成/代付）
2. **已审核出款订单** — 已完结订单的查询、统计汇总与导出
3. **总出款记录** — 全量出款流水，供财务对账
4. **提现管理（提现条件配置）** — 免审风控开关、自动代付开关、金额范围、代付失败自动驳回、渠道配置
5. **代付商户管理** — 第三方代付渠道基础资料维护

对应的完整需求说明见 `withdrawal_and_autopay_PRD.html`。

## 🎁 模块说明（返水部分）

`rebate_prototype.html` 包含三个界面，通过场馆卡片 / 操作按钮 / 顶部 Tab 相互跳转：

1. **返水首页** — 顶部一级 Tab + 额度汇总条 + 左侧游戏类型（Slot / Cassino）与操作按钮（Receber / Histórico）+ 右侧场馆列表；每张场馆卡片内置按“距下一档”公式计算的返水进度条
2. **场馆返水详情页（Taxa de reembolso）** — 按 Modalidade（Slot / Esportes）、Fornecedor 两个维度筛选查看投注阶梯与对应返水比例
3. **历史记录页（Histórico）** — 按 Hoje / Ontem / Últimos 7 Dias / Últimos 30 Dias 筛选返水领取流水，切换周期时重新请求接口获取数据

页面顶部另有一个「次日领取 / 实时领取」预览切换按钮，用于对比两种后台可配置的结算模式（仅供评审预览，非客户端正式控件）。三类空状态（Cassino 场馆为空 / Esportes 阶梯为空 / 历史记录周期无数据）统一使用同一套「Sem Registros」缺省页。

对应的完整需求说明见 `rebate_prd.html`。

## 🕒 更新记录

- 2026-07-07：VIP 客户端 / 管理后台交互设计稿与 PRD 初版
- 2026-07-10：新增商户财务出款审核与自动代付模块原型（`merchant_finance_app_1.html`）及对应 PRD（`withdrawal_and_autopay_PRD.html`），并将「免审风控开关」「首次出款强制人工审核」等确认后的业务规则同步落地
- 2026-07-15：新增返水（Rebate）模块原型（`rebate_prototype.html`）及对应 PRD（`rebate_prd.html`），涵盖返水首页、场馆详情页、领取弹窗、历史记录页，并确认了返水进度条计算公式、Receber 快照领取逻辑、「次日领取/实时领取」两种结算模式配置等关键规则
