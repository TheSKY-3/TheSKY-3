# 吴柏高

**广东财经大学 · 统计学硕士在读 ｜ 求职方向：数据分析 · 经营分析 · 数据策略**

把业务问题拆成可验证的指标，把重复的分析流程做成可复现的系统。

广州 ｜ [个人网站](https://thesky-3.github.io) ｜ [邮箱](mailto:1525546469@qq.com) ｜ [GitHub](https://github.com/TheSKY-3)

---

## 简介

📊 统计学硕士在读，方向：经营分析 / 数据分析 / 数据策略；项目集中在出行与电商。

🛠️ 比较擅长的两件事：

- **把业务问题拆成能算、能对得上的指标。** 在出行平台分析过 1015 万+ 订单的渠道、补贴与履约，最后做成一张分渠道的策略矩阵；在 Olist 电商公开数据里用 9.6 万笔订单定位到“履约延迟是差评头号杀手”。
- **把重复的分析做成能复用的系统。** 司机运营日报从 2 小时压到 5 分钟、连续跑了 60 期；把三方结算的 21 项规则固化成标准字段；月度财务对账从 1 天缩到 10 分钟。

比起“图很漂亮”，更在意数字能不能回到原始表，所以愿意在指标定义和校验上多花时间。

🤖 目前在做一个电商结算对账原型和一个商品评论证据原型，共同原则是“确定性代码负责事实，大模型只负责解释”，每个结论都能回到原始数据。

🔍 研究关注金融欺诈报警的优先级排序：在有限复核人力下，哪些报警该优先查。第一作者论文在投。

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

| 案例 | 规模 | 关键结论 |
| --- | --- | --- |
| **[Olist 电商履约与口碑](https://thesky-3.github.io/projects/olist)**<br><sub>MySQL · Power BI · Docker</sub> | 9.6 万笔订单 | 准时送达评分 **4.29**，迟到 6 天以上 **1.74**——差评治理的抓手在履约时效。 |
| **[GA4 转化漏斗与增长实验](https://thesky-3.github.io/projects/ga4-growth)**<br><sub>BigQuery · SQL</sub> | 429 万事件 / 27 万用户 | 三阶段购买转化 **6.05%**；稳定窗口浏览→加购流失 **78.1%**，资源应先投商品详情页与加购引导；17 条 SQL 全部可审计。 |
| **[Criteo 营销增量与投放策略](https://thesky-3.github.io/projects/criteo-uplift)**<br><sub>Python · Uplift</sub> | 约 1398 万行 | ITT → Uplift → AUUC/Qini → 覆盖策略模拟；固定配置下 S-Learner 的 AUUC 领先；明确停在「离线分析完成，线上验证未开始」。 |

> 代码未公开；完整方法、图表与边界见各案例页。

### 04 研究：金融欺诈报警的代价风险评估（TC-CCR）

第一作者 · 论文在投。把「一个评分模型」变成「一份受复核容量与错误代价约束的报警名单预算」。IEEE-CIS + BAF 约 159 万条样本，时间一致验证；10% 复核容量下，OOF 成本最优阈值使未来测试总成本相对默认阈值降低 **40.37%–48.60%**。 [研究详情](https://thesky-3.github.io/research)

## 工具栈

- **分析**：Python（Pandas / NumPy / Matplotlib）· SQL（MySQL、窗口函数）· Power BI / DAX · Excel
- **工程**：FastAPI · SQLite / FTS5 · Docker · pytest · GitHub Actions
- **AI**：LangGraph · 结构化输出 · 受约束 Agent · 评测与校验（Verifier）

## 联系

广州 ｜ [thesky-3.github.io](https://thesky-3.github.io) ｜ [1525546469@qq.com](mailto:1525546469@qq.com)
