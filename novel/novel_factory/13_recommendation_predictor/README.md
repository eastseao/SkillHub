# 番茄爆款预测模拟器

## 定位

> 📊 **"在写之前就判断：这一章/这本书有没有进推荐池 + 爆款的概率"**

接在：
- `07 chapter_engine`（章节生成）
- `10 platform_adapter`（平台适配）

之后，在发布前预测爆款概率。

## 核心使命

### 1️⃣ 爆款概率预测

- CTR（点击率）预测
- 留存率预测
- 追更率预测

### 2️⃣ 推荐池模拟

番茄4阶段推荐池：
- 冷启动（500-2000曝光）
- 小流量池（1-5万曝光）
- 中流量池（10-50万曝光）
- 爆款池（100万+曝光）

### 3️⃣ 章节级评分

预测每一章能否进入下一轮推荐。

## 与系统的结合

```
07_chapter_engine
↓
13_recommendation_predictor（爆款预测）
↓
11_quality_control（质量审核）
↓
10_platform_adapter（多平台分发）
```

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 预测核心 | prompts/core_predictor.md | 统一入口，综合评分 |
| CTR模型 | prompts/ctr_model.md | 点击率预测 |
| 留存模型 | prompts/retention_model.md | 留存率预测 |
| 3秒钩子 | prompts/hook_strength_analyzer.md | 开头3秒分析 |
| 爆点检测 | prompts/rage_point_detector.md | 爽点密度检测 |
| 推荐池模拟 | prompts/recommendation_simulator.md | 4阶段路径模拟 |
| 流量层级 | prompts/traffic_tier_model.md | S/A/B+/B/C/D分级 |
| 标题评分 | prompts/title_score_engine.md | 标题黄金公式 |
| 开头分析 | prompts/opening_3s_analyzer.md | 开头3秒判断 |
| 传播潜力 | prompts/virality_estimator.md | 病毒传播评估 |

## 综合评分公式

```
FINAL_SCORE =
  0.25 × CTR
+ 0.25 × RETENTION
+ 0.20 × HOOK
+ 0.20 × RAGE
+ 0.10 × TITLE
```

## 5档推荐等级

| 等级 | 总评分 | 推荐池 | 预期曝光 |
|------|--------|--------|----------|
| S | 90-100 | 爆款池 | 100万+ |
| A | 80-89 | 大流量池 | 30-100万 |
| B+ | 75-79 | 中流量池 | 10-30万 |
| B | 65-74 | 小流量池 | 1-10万 |
| C | 50-64 | 冷启动 | <1万 |
| D | <50 | 死亡 | 0 |

## 番茄爆款核心规则

### 🔥 必须满足

- 前3秒有冲突
- 每2000字一个爽点
- 情绪持续波动
- 有明确对立关系

### ❌ 直接死亡

- 无冲突开局
- 信息铺垫过长
- 没有情绪释放点

## 输出

每一章你都会得到：

```
✔ 是否能进推荐池
✔ 是否有爆款潜力
✔ 哪一段会导致弃书
✔ 哪一句是爆点
✔ 如何改成爆款版本
```

## 下一步升级

- `14_reader_retention_model` — 读者弃书点预测
- `15_auto_rewriter` — 把70分改成90分
- `16_fully_auto_fanqie_factory` — 全自动番茄日更爆款工厂