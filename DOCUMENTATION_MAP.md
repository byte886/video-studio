# 文档地图（DOCUMENTATION MAP）

> **文档类型**：Reference（参考资料 — 文档索引）
> **更新频率**：每次新增/删除/移动文档时
> **维护者**：AI 自动维护
> **读者**：AI 代理（快速定位文档）+ 人类（查文档去哪找）

> 本文档是 video-studio 全仓文档的导航入口（llms.txt 作用）：告诉 AI 和人"先读什么、去哪找什么"。
> 配合 `README.md`（给人看的概览）+ `AGENTS.md`（给 AI 的命令式操作手册）使用。

---

## 快速入口（按场景）

### 开始新任务前（冷启动）
1. `AGENTS.md` — AI 操作手册（核心规则/禁止事项/恢复路径 A·B，强制先读）
2. `00_项目总纲.md` — 通用生产纲领与当前状态
3. `03_进行中的任务/TASK_STATUS.md`（到哪/下一步）+ `03_进行中的任务/ISSUES.md`（未核实项/做不通方向）

### 问"为什么这样定"
- `02_决策记录/README.md` — ADR 索引（先查历史避免冲突）；正文 `02_决策记录/ADR-NNN_*.md`（只增不改）
- `02_决策记录/治理卡.md` — 决策权限/暂停重评触发条件

### 做珠宝出图/出视频前
- 行业总 SOP：`domains/jewelry/国内AI生成珠宝实操SOP.md`
- 无模特版分步执行：`domains/jewelry/无模特版出片SOP.md`
- 通用导演/分镜：`01_结论与产出/导演思维与分镜生成SOP.md`
- 音频配方：`01_结论与产出/音频选择与生成SOP.md`（讲货片不作音频来源，见 ADR-003 末节）
- 工具选型/成本/参数：`01_结论与产出/工具选型参考.md`
- 质量门禁：`01_结论与产出/全链路质量门禁_v2.0.md`（G1–G5 可勾选）+ `02_决策记录/评估迭代机制.md`

### 找调研证据 / 来源
- `01_结论与产出/来源索引.md` — 外部链接证据库
- `09_调研底稿与素材/` — 只读存档（四路调研/收藏视频分析/单条视频分析/SOP精炼评估/郭颖B级对标83卡）
- 对标卡片索引：`09_调研底稿与素材/郭颖B级对标_20261012/README_对标卡片索引.md`

### 看评审/治理记录
- `project-management/reviews/README.md` — 评审报告索引（含本仓历次评审落位）

---

## 全仓文档清单（按层）

### 根层（导航/事实/章程/台账）
| 文档 | 类型 | 一句话职责 |
|---|---|---|
| `README.md` | Concept | 仓库概览 + 文档边界表 + 快速开始 + 目录结构（给人看） |
| `AGENTS.md` | Governance | AI 命令式操作手册（目录约定/禁止事项/恢复路径/OKF 规范） |
| `PROFILE.md` | Reference | 项目事实层（产品/工具栈/已验证结论/外部指针），易变状态不写这 |
| `00_项目总纲.md` | Concept | 通用生产纲领（目标/全链路能力/IO门禁/成功标准/里程碑/当前状态） |
| `DOCUMENTATION_MAP.md` | Reference | 本文件（文档导航地图） |
| `CHANGELOG.md` | Active | 仓库显著变更倒序留痕（只增不改） |

### 01_结论与产出/（通用层最终交付物）
| 文档 | 类型 | 职责 |
|---|---|---|
| `导演思维与分镜生成SOP.md` | SOP | 拆解动机→分镜→提示词框架 |
| `音频选择与生成SOP.md` | SOP | 配音/BGM/拟音通用框架 + 珠宝特化参数 |
| `工具选型参考.md` | Reference | 各模型实测结论 + 成本/参数 + UI vs API |
| `来源索引.md` | Reference | 外部链接证据库 |
| `全链路质量门禁_v2.0.md` | Standard | G1–G5 五阶段可勾选检查项 |
| `博主成片逐帧核实SOP.md` | SOP | 效果断言逐帧核实方法（分型矩阵/降级路径/证据档升降） |
| `仓库评审报告_20261012.md` | Review | 白天全仓治理评审（video-studio+content-pipeline+control-tower） |
| `独立旁观评审报告_20261012-晚间.md` | Review | 晚间独立旁观者复评（本轮） |

### 02_决策记录/（ADR + 治理机制）
| 文档 | 类型 | 职责 |
|---|---|---|
| `README.md` | Reference | ADR 索引（含 superseded 标注） |
| `ADR-001_项链嵌蓝宝石方案选择.md` | Decision | 嵌蓝宝石改款方案（**已被 ADR-004 取代**） |
| `ADR-002_视频路线与工具选型.md` | Decision | 先无模特版后模特版；Seedance 2.0 Fast 默认 |
| `ADR-003_音频复听决策与保守执行规则.md` | Decision | 音频保守配方 + 复听实验结果演进注记 |
| `ADR-004_方案A改款定稿_足金O字链单颗5.5mm蓝宝石居中.md` | Decision | 现行设计基线（取代 ADR-001） |
| `治理卡.md` | Governance | 决策权限/暂停重评触发/碰节奏 |
| `评估迭代机制.md` | Standard | G1–G5 五道门禁框架 |
| `珠宝设计评估_方案3_20261006.md` | Research | 方案3 设计评估留档 |

### 03_进行中的任务/（动态台账 + 过程件）
| 文档 | 类型 | 职责 |
|---|---|---|
| `TASK_STATUS.md` | Active | 进度唯一权威源（到哪/下一步/开放问题计数） |
| `ISSUES.md` | Active | 未核实项 + resolved + Won't Fix 生命周期 |
| `ISSUE-003_博主成片逐帧核实报告_20261012.md` | Research | 10 条逐帧核实汇总 |
| `ISSUE-003_逐帧核实/` | Research | 10 篇逐帧笔记（已关闭工单留档） |
| `质量评估与迭代机制/` | Process | SOP精炼评估/验证报告/调研协作机制（过程件） |

### domains/（行业实例层）
| 位置 | 职责 |
|---|---|
| `domains/jewelry/README.md` | 珠宝实例导航（行业覆盖/文件清单/运行规则） |
| `domains/jewelry/国内AI生成珠宝实操SOP.md` | 珠宝出图/出视频总 SOP |
| `domains/jewelry/无模特版出片SOP.md` | 无模特版分步执行 |
| `domains/jewelry/广告叙事与故事塑造SOP.md` | 叙事结构/母题/音画映射 |
| `domains/jewelry/数字人平台矩阵.md` / `故事塑造平台选型参考.md` | B2/C 路结论 |
| `domains/jewelry/小红书*SOP.md`（起号运营/AI标注/合规清单/私域引流） | 发布合规与运营 |
| `domains/jewelry/首条成片方案_蓝宝石O字链_20261012.md` | 方案A定稿首条成片制作方案（draft·待执行确认） |
| `domains/jewelry/收藏素材体系总纲_rev20261006.md` | 收藏素材能力地图（rev 权威版） |
| `domains/jewelry/方案效果图/` | 方案1-3 + 改款A/B/C 对比 + 模特版佩戴图 |

### 09_调研底稿与素材/（只读存档，不改原文）
按子目录归位：`20261006_四路调研/`（A/B1/B2/C 路底稿）、`20261006_收藏视频分析/`、`20261009_单条视频分析/`（含 remotion-minimal-template）、`SOP精炼评估_20261006/`、`郭颖B级对标_20261012/`（83 卡 + 索引）；根目录散篇调研笔记（tool_api_research / industry_cases_research 等）。行业归位说明见 `domains/jewelry/README.md`。

### project-management/reviews/（评审记录）
| 文档 | 职责 |
|---|---|
| `project-management/reviews/README.md` | 评审报告索引（登记本仓历次评审落位） |
| `project-management/reviews/2026-10-12-修正轮记录.md` | 2026-10-12 晚间拍板项修正轮留痕 |

---

*新增/删除/移动文档时必须同步本清单。*
