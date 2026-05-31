# 11_quality_control 质量控制系统

## 定位

> 🧪 **"AI小说工业生产线的最终质检门禁系统（发布前最后一道防线）"**

如果说：

- `07 chapter_engine` = 写作生产线
- `08 memory_manager` = 记忆系统
- `09 style_system` = 风格统一
- `10 platform_adapter` = 多平台输出

那么：

- `11 quality_control` = **编辑部 + 审核部 + 数据分析中心**

## 核心使命

检查、打分、纠错、回滚、封装发布——是整条生产线的**最后一道防线**。

## 调用顺序

```
07_chapter_engine
↓
11_quality_control
↓
（失败）→ 07重写
（通过）→ 10_platform_adapter
```

## 两大检测级别

| 级别 | 触发时机 | 作用 |
|------|----------|------|
| 章节QC | 每章完成 | 单章质量把关 |
| Arc QC | 每Arc完成 | 整体结构把关 |
| 发布门 | 发布前 | 最终门禁 |

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| QC核心引擎 | prompts/qc_core_engine.md | 统一入口，多维汇总 |
| 剧情一致性检测 | prompts/plot_consistency_checker.md | 逻辑断裂/偏离主线 |
| 角色一致性检测 | prompts/character_consistency_checker.md | OOC/性格漂移 |
| 力量平衡检测 | prompts/power_balance_checker.md | 战力崩坏/数值膨胀 |
| 世界逻辑检测 | prompts/world_logic_checker.md | 法则崩坏/地图矛盾 |
| 节奏质量检测 | prompts/pacing_quality_checker.md | 拖沓/过快/爽点密度 |
| 情绪质量检测 | prompts/emotional_quality_checker.md | 平淡/爆点无效 |
| 风格一致性检测 | prompts/style_compliance_checker.md | 风格漂移 |
| 读者留存评分 | prompts/engagement_score_engine.md | 钩子强度/追更欲 |
| 水文检测器 | prompts/water_content_detector.md | 冗余内容/无意义描写 |
| 钩子质量检测 | prompts/cliffhanger_quality_checker.md | 悬念强度 |
| 发布审核门 | prompts/final_publish_gate.md | PASS/FAIL最终判定 |

## 多维评分体系（100分制）

| 维度 | 分值 | 及格线 |
|------|------|--------|
| 剧情一致性 | 25 | 15 |
| 角色一致性 | 20 | 12 |
| 世界逻辑 | 15 | 9 |
| 节奏质量 | 15 | 9 |
| 情绪质量 | 10 | 6 |
| 风格一致性 | 10 | 6 |
| 读者留存 | 5 | 3 |

**发布门阈值：≥80分**

## 严重性分级

| 级别 | 处置 | 示例 |
|------|------|------|
| Critical | 立即修复，阻塞发布 | 剧情断裂/角色崩坏/世界崩坏 |
| High | 必须修复 | 节奏拖沓/战力失衡/水文超标 |
| Medium | 建议修复 | 描写冗余/钩子不够强 |
| Low | 可选优化 | 细节/语言精炼 |

## 三大核心原则

| 原则 | 说明 |
|------|------|
| **QC不是评价，是"生产控制器"** | 结构化评分，不是主观感受 |
| **必须结构化，不允许感性评价** | 每项问题必须有依据 |
| **必须能回滚写作系统** | FAIL → 07重写，形成闭环 |

## 高级系统

### 1、自动回滚系统

```
QC失败 → 回滚07 chapter_engine重写
```

### 2、发布门禁系统

```
低于80分不能发布
必须通过所有核心检测
无严重逻辑错误
```

### 3、崩坏预警系统

提前发现剧情崩坏趋势，在崩溃前修复。

## 输出结构

```
/qc/
├── report.md         ← 总报告
├── scorecard.md      ← 评分卡
├── issues.md         ← 问题列表
├── fix_suggestions.md ← 修复建议
└── publish_gate.md   ← 发布门判定
```

## 驱动系统

| 结果 | 流向 |
|------|------|
| PASS | → 10_platform_adapter |
| FAIL | → 07_chapter_engine 重写 |

## 最终效果

输入：`章节内容`

输出：`/qc/` 下一整套质量报告，附带 PASS/FAIL 判定，决定是否发布或回滚重写。