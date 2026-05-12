---
name: aicb-weekly-news
description: Generate weekly AI business news roundup scripts for the WeChat video channel "AI时代的'反共识'商业局". Use when asked to produce AI商业新闻榜, 反共识商业局选题, 本周AI商业新闻, or any request related to Gary's weekly AI business news video script. The skill scans Chinese hot searches (Baidu, Weibo, Douyin, Zhihu, Bilibili, Toutiao), filters news events, and outputs 5 contrarian takes with video scripts for marketing/brand/PR leaders.
---

# AI商业新闻周榜 (AICB Weekly News)

Generate weekly AI business news roundup scripts for Gary's WeChat Channels show "AI时代的'反共识'商业局".

## Core Workflow

1. **Scan Chinese hot searches** (优先级顺序):
   - 一级入口：中国公域热榜 — 百度热搜、微博热搜、抖音热榜、知乎热榜、B站热榜、头条热榜
   - 二级入口：中国科技商业媒体 — 36氪、IT之家、量子位、机器之心、极客公园、钛媒体、财联社、晚点、虎嗅
   - 三级入口：国内AI/商业主体 — 百度、阿里、腾讯、字节、华为、小米、DeepSeek、Kimi、MiniMax、智谱、阶跃、月之暗面、宇树、地平线等
   - 辅助入口：国际新闻（仅用于解释中国市场趋势，不作为主入口）

2. **Filter for news events** — 必须是有明确主体、动作、进展、公共后果的事件。跳过泛话题、搜索词、纯情绪梗、不可核实爆料、政治敏感话题。

3. **Score each candidate** (满分100，低于75分不推):
   | 维度 | 权重 |
   |---|---:|
   | 中国热搜上升势能 | 20 |
   | 市场营销人损益感 | 20 |
   | 反共识强度 | 20 |
   | blue-dot权威适配 | 15 |
   | 前5秒爆发力 | 15 |
   | 风险可控 | 5 |

4. **Output 5 news events** per weekly episode with script format.

## Output Format

```
## 本周AI商业新闻榜 AICB-WEEK-YYYYMMDD

总标题：
备选标题：
前5秒总开场：

### 01
推荐指数：
国内热榜/媒体来源：
链接：
事件一句话：谁做了什么，发生了什么变化
为什么市场部要知道：
反共识判断：
市场部该怎么做：

### 02...

结尾钩子：
风险提示：
```

## Script Structure (90-120秒视频)

| 时间 | 内容 |
|---|---|
| 0-5s | 总开场：本周5件AI商业新闻，停止滑动 |
| 5-20s | 事件1：新闻+判断+行动 |
| 20-35s | 事件2 |
| 35-50s | 事件3 |
| 50-65s | 事件4 |
| 65-85s | 事件5 |
| 85-110s | 总结主线+评论区钩子 |

## 标题公式

主公式：大众正在狂热/忽视的现象 + Gary的致命反问/反常识结论

可用标题壳：
- 《别再___了，___正在偷偷吃掉你的客户》
- 《你以为___，其实___》
- 《所有人都在___，但真正危险的是___》
- 《老板们最该停下来的，不是___，而是___》
- 《___又刷屏了，但90%公司看错了重点》
- 《如果你公司还在___，2026年会非常危险》
- 《___不是机会，是一次管理压力测试》

禁用词（不能出现在标题/前5秒）：全面解读、底层逻辑、趋势分析、如何提升、一文看懂、深度拆解

## 前5秒开场模板

**A. 撕毁共识法**
```
现在全网都在教你___，我建议你先停下来。
因为在2026年，真正决定你生死的已经不是___，而是___。
```

**B. CEO交底法**
```
作为一家AI-native营销公司的CEO，我今天给老板们交个底：
你们花钱买的___，很可能不是资产，而是新的管理负债。
```

**C. 热点反转法**
```
昨晚___刷屏了，所有人都在说___。
但我看完只看到一件事：未来三年，很多B2B公司会因为___被淘汰。
```

**D. 数据惊吓法**
```
如果你发现官网线索突然变少，不一定是销售不努力。
更可能是你的客户已经被AI在搜索结果页截走了。
```

## Key References

- **Agent系统Prompt**: See [AI时代反共识商业局-Agent操作系统.md](references/AI时代反共识商业局-Agent操作系统.md) — 完整评分模型、选题原则、反馈闭环
- **Runtime Prompt**: See [agent-runtime-prompt.md](references/agent-runtime-prompt.md) — 每次运行的完整指令
- **Automation Config**: See [automation-config.md](references/automation-config.md) — 心跳调度配置快照
- **Feedback Log**: See [feedback-log.csv](feedback-log.csv) — Gary的历史反馈记录

## 受众定位

- **主受众**：市场营销传播总监、品牌总监、公关总监、数字营销负责人、内容负责人、增长负责人、市场运营负责人、一线市场营销人
- **次级受众**：CEO/老板、销售负责人、企业数字化负责人

## 节目策略

- **特洛伊木马策略**：标题和前5秒必须有冲突、悬念、痛点；正文必须进入真正的商业洞察，落到GEO、AI-native管理、OGSM、Moltbot、B2B营销增长
- **人设**：内向、理性、克制，但观点锋利；不是情绪主播，而是"冷静的商业手术刀"
- **不做**：泛AI科普、只借势不判断、只给焦虑不给可执行建议

## Feedback Loop

Gary的反馈格式：
```
AICB-20260511-02：选这个，标题更狠一点，脚本保守了。
AICB-20260511-04：不要，太像泛AI博主。
AICB-20260511-05：保留方向，但换成GEO角度。
```

Agent记录6类反馈：topic_id, decision, title_feedback, angle_feedback, risk_feedback, performance。每周复盘更新爆款标题库、高留存开场库、Gary个人反共识观点库。
