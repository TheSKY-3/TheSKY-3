# 吴柏高

**广东财经大学 · 统计学硕士在读 ｜ 求职方向：数据分析 · 经营分析 · 数据策略**

把业务问题拆成可验证的口径，把重复的分析流程做成可复现的系统。

广州 ｜ [个人网站](https://thesky-3.github.io) ｜ [邮箱](mailto:1525546469@qq.com) ｜ [GitHub](https://github.com/TheSKY-3)

---

## 简介

- **经营分析**：在出行平台运营中心分析 1015 万+ 订单的渠道、补贴与履约，输出四渠道策略矩阵（单渠道最高补贴 ROI 4.17）。
- **分析工程化**：把司机日报做成 AI 工作流（连续 60 期，单期 2 小时 → 5 分钟）；把三方结算口径写成 21 项标准字段；把月度财务对账做成自动化程序（1 天 → 10 分钟，部门实测）。
- **研究**：第一作者论文在投（TC-CCR 框架）。在 IEEE-CIS 与 BAF 约 159 万条样本上，研究复核容量与错误代价约束下的报警名单决策；10% 复核容量下，OOF 成本最优阈值相对默认阈值降低未来测试总成本 40.37%–48.60%。
- **开源**：两个可运行的 Agent 原型，一个管电商结算对账，一个管商品评论证据。共同原则：确定性代码负责事实，LLM 只负责解释，输出可回查、可复核。

## 主要项目

### 01 电商结算对账 Agent ｜ [代码](https://github.com/TheSKY-3/ecom-settlement-recon) · [案例](https://thesky-3.github.io/projects/settlement-recon)

**产品价值**：把三方对账从「逐笔翻账 + 手工写说明」变成「看结论 + 抽查引用」，每个数字都能点回账本。

**做法**：确定性规则树 + 独立验证器 + 审计链；LLM 只组织语言，答案里的数字与编号必须命中事实单白名单，违规自动降级为模板。

**结果**：约 2.5 秒扫完 9.9 万单；1,750 条注入差异召回 100%、真误报 0；同一套匹配思想跑 BenchRec 银行对账，精度 99.67%（官方 ChatGPT 基线 95.20%）。

**技术 / 状态**：Python · FastAPI · SQLite · DeepSeek（可选）；本地原型 + 合成数据评测，未使用公司真实账单。

### 02 电商评论证据 Agent ｜ [代码](https://github.com/TheSKY-3/ecom-review-intelligence) · [案例](https://thesky-3.github.io/projects/ecom-review-agent)

**产品价值**：把海量评论从「翻页拼证据」变成「可回查的证据卡 + 可执行的核查顺序」，运营能复核，而不是拿一段无法溯源的总结。

**做法**：本地证据引擎（SQLite/FTS5）+ 逐字段 Verifier；模型只拿运行期别名与聚合卡；AI 深入分析四道机器校验，任一条不过整段丢弃。

**结果**：仓库自带 3 商品、11,958 条评论的演示子集，克隆即跑；Windows 单文件版双击即用，无 key 时全链路离线确定性模式。

**技术 / 状态**：Python · FastAPI · LangGraph · DeepSeek（可选）；阶段性工程验证完成，真人试用尚未进行。

### 03 经营分析案例

- **[Olist 电商履约与口碑](https://thesky-3.github.io/projects/olist)** ｜ 9.6 万笔订单：准时送达评分 4.29，迟到 6 天以上 1.74——差评治理的抓手在履约时效。MySQL · Python · Power BI · Docker
- **[GA4 转化漏斗与增长实验](https://thesky-3.github.io/projects/ga4-growth)** ｜ 429 万事件 / 27 万用户：三阶段购买转化 6.05%；稳定窗口浏览→加购流失 78.1%，资源应先投商品详情页与加购引导。17 条 BigQuery SQL 全部可审计。
- **[Criteo 营销增量与投放策略](https://thesky-3.github.io/projects/criteo-uplift)** ｜ 约 1398 万行随机实验数据：ITT → Uplift → AUUC/Qini → 覆盖策略模拟；固定配置下 S-Learner 的 AUUC 领先，明确停在「离线分析完成，线上验证未开始」。

> 代码未公开；完整方法、图表与边界见各案例页。

### 04 研究：金融欺诈报警的代价风险评估（TC-CCR）

第一作者 · 论文在投。把「一个评分模型」变成「一份受复核容量与错误代价约束的报警名单预算」。IEEE-CIS + BAF 约 159 万条样本，时间一致验证；10% 复核容量下，OOF 成本最优阈值使未来测试总成本相对默认阈值降低 **40.37%–48.60%**。 [研究详情](https://thesky-3.github.io/research)

## 工具栈

- **分析**：Python（Pandas / NumPy / Matplotlib）· SQL（MySQL、窗口函数）· Power BI / DAX · Excel
- **工程**：FastAPI · SQLite / FTS5 · Docker · pytest · GitHub Actions
- **AI**：LangGraph · 结构化输出 · 受约束 Agent · 评测与校验（Verifier）

## 联系

广州 ｜ [thesky-3.github.io](https://thesky-3.github.io) ｜ [1525546469@qq.com](mailto:1525546469@qq.com)
