# 吴柏高

**广东财经大学 · 统计学硕士在读 ｜ 专注领域：Agent 工程 · LLM 应用**

做可验证的 LLM Agent：算得对、说得清、错了能降级。

广州 ｜ [个人网站](https://thesky-3.github.io) ｜ [邮箱](mailto:1525546469@qq.com) ｜ [GitHub](https://github.com/TheSKY-3)

---

## 简介

专注 Agent 工程 / LLM 应用。核心原则是“确定性代码负责事实，模型负责规划与解释”，每个结论都能回到原始数据。

关注点不是 Demo 能不能跑，而是算得对不对、错了能不能降级。

## 主要项目

两个开源 Agent 原型，加一个作品集站：

| 项目 | 一句话介绍 | 主要技术 |
| --- | --- | --- |
| **[电商结算对账 Agent](https://github.com/TheSKY-3/ecom-settlement-recon)**<br><sub>[案例](https://thesky-3.github.io/projects/settlement-recon)</sub> | 把三方对账从逐笔翻账变成看结论、抽查引用，每个数字都能点回账本。<br>9.9 万单 / 2.5 秒；1,750 条合成差异召回 100%、真误报 0；跨域 BenchRec 99.67%，高于官方 ChatGPT 基线 95.20%。 | Python · FastAPI · SQLite<br>确定性规则树 · 独立验证器 · 受约束 LLM |
| **[电商评论证据 Agent](https://github.com/TheSKY-3/ecom-review-intelligence)**<br><sub>[案例](https://thesky-3.github.io/projects/ecom-review-agent)</sub> | 让运营不翻几千条评论，也能拿到可回查、能复核的问题证据。<br>3 商品 / 11,958 条评论；四道机器校验，任一条不过整段作废。 | Python · FastAPI · LangGraph<br>SQLite/FTS5 · Verifier |
| **[个人作品集站](https://thesky-3.github.io)** | 把项目、方法和证据边界整理成可阅读的案例页。 | Astro · TypeScript<br>GitHub Actions |

> 两个 Agent 均为本地原型：结算用公开电商数据 + 合成差异评测，评论用 3 商品演示子集；完整边界见项目页。

## 业务分析案例

| 案例 | 规模 | 关键结论 |
| --- | --- | --- |
| **[Olist 电商履约与口碑](https://thesky-3.github.io/projects/olist)**<br><sub>MySQL · Power BI · Docker</sub> | 9.6 万笔订单 | 准时送达评分 **4.29**，迟到 6 天以上 **1.74**——差评治理的抓手在履约时效。 |
| **[GA4 转化漏斗与增长实验](https://thesky-3.github.io/projects/ga4-growth)**<br><sub>BigQuery · SQL</sub> | 429 万事件 / 27 万用户 | 三阶段购买转化 **6.05%**；稳定窗口浏览→加购流失 **78.1%**，资源应先投商品详情页与加购引导；17 条 SQL 全部可审计。 |
| **[Criteo 营销增量与投放策略](https://thesky-3.github.io/projects/criteo-uplift)**<br><sub>Python · Uplift</sub> | 约 1398 万行 | ITT → Uplift → AUUC/Qini → 覆盖策略模拟；固定配置下 S-Learner 的 AUUC 领先；明确停在「离线分析完成，线上验证未开始」。 |

> 代码未公开；完整方法、图表与边界见各案例页。

## 研究：金融欺诈报警的代价风险评估（TC-CCR）

**风控团队不缺模型分数，缺的是“先查谁、查多少”。** TC-CCR 不止于 AUC，而是用代价敏感决策把评分模型变成一份受复核容量与错误代价约束的报警名单预算：在 10% 复核容量下，OOF 成本最优阈值把未来测试总成本降低 **40.37%–48.60%**，让有限的复核人力优先落在更值得查的报警上。IEEE-CIS + BAF 约 159 万条样本，时间一致验证；第一作者，论文在投。 [研究详情](https://thesky-3.github.io/research)

## 技术栈

- **Agent / LLM**：LangGraph · 结构化输出 · 受约束 Agent · 评测与校验（Verifier）· 合成评测 · 降级策略
- **工程**：Python · FastAPI · SQLite / FTS5 · Docker · pytest · GitHub Actions
- **分析**：SQL（MySQL、窗口函数）· Power BI / DAX · Pandas / NumPy

## 联系

广州 ｜ [thesky-3.github.io](https://thesky-3.github.io) ｜ [1525546469@qq.com](mailto:1525546469@qq.com)
