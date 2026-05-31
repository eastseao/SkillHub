# 14_auto_viral_rewriter 自动爆款改写器

## 定位

> 🔥 **"把60-75分的章节，改写成85-95分的爆款章节"**

如果说：

- `07 chapter_engine` = 写小说
- `13 recommendation_predictor` = 预测爆款概率

那么：

- `14 auto_viral_rewriter` = **爆款结构重写引擎（不是修辞，是重构叙事）**

## 核心使命

把"能看（60~75分）"的章节 → 改写成"容易爆（85~95分）"的章节

**在不改变主线剧情的前提下，重构"爽点密度 + 钩子结构 + 情绪曲线"**

## 调用顺序

```
07 chapter_engine
↓
13 recommendation_predictor
↓
14 auto_viral_rewriter  ←  🔥（新增）
↓
11 quality_control
↓
10 platform_adapter
```

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 爆款重写核心 | prompts/core_rewriter_engine.md | 统一入口，结构重组 |
| 开头钩子强化 | prompts/hook_enhancer.md | 3秒抓人 |
| 冲突增强 | prompts/conflict_amplifier.md | 提升冲突密度 |
| 节奏优化 | prompts/pacing_optimizer.md | 加快事件密度 |
| 情绪峰值构建 | prompts/emotional_peak_builder.md | 打脸/逆袭/反转 |
| 场景重构 | prompts/scene_restructure_engine.md | 重排场景顺序 |
| 无聊段落杀手 | prompts/boring_section_killer.md | 删除无效内容 |
| 对话锐化 | prompts/dialogue_sharpening.md | 强化冲突对话 |
| 结尾悬念增强 | prompts/ending_cliffhanger_booster.md | 强化钩子 |
| 病毒传播改写 | prompts/virality_transformer.md | 增加传播点 |
| 改写后评分预测 | prompts/score_predict_after_rewrite.md | 预测新评分 |

## 三重提升

| 提升目标 | 方法 | 预期提升 |
|----------|------|----------|
| CTR（点击率） | 标题优化+开头钩子强化 | +15~30 |
| Retention（留存率） | 增加冲突频率+减少信息堆叠 | +10~25 |
| Rage/爽点（情绪爆发） | 打脸增强+权力反转+利益冲突强化 | +20~40 |

## 核心设计原则

### 1️⃣ 改写≠润色

是"结构重组"，不是文字润色。

### 2️⃣ 爽点优先于文学性

平台优先，不是文学优先。

### 3️⃣ 冲突密度是核心指标

没有冲突 = 直接失败。

### 4️⃣ 结尾钩子必须强制存在

否则不进入推荐池。

## 改写效果

输入：
```
一章70分普通章节
```

输出：
```
一章90分番茄爆款章节
```

并自动具备：

- 推荐池通过率提升
- 留存率提升
- 爆点增强
- 追更欲望增强

## 配置文件说明

### rewrite_rules.yaml

基本改写规则，包括：
- 基本原则（不得改变主线剧情等）
- 必须增强项（开头钩子、冲突密度等）
- 必须删减项（环境描写、内心独白等）
- 改写优先级
- 目标评分

### boost_weights.yaml

各维度提升权重，包括：
- 维度提升权重（CTR/留存/爽点/钩子/标题）
- 改写方法权重
- 提升效果预估
- 改写后评分预测

### forbidden_changes.yaml

禁止更改项，包括：
- 绝对禁止更改的内容
- 允许更改的内容
- 改写边界

## 完整爆款闭环

```
写章节
↓
预测（70分）
↓
改写（90分）
↓
QC审核
↓
发布
```

## 下一步升级

### 🚀 15：全自动"冲番茄榜单AI工厂"（无人写作+自动优化+自动日更）

### 🚀 16：爆款标题生成器（点击率预测版）

### 🚀 17：读者弃书预测系统（精准定位流失点）

只要你说一句：

> "做自动冲榜系统"

我可以把这套直接升级成**番茄小说自动上榜工厂级系统**。