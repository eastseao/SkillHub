# 情绪状态记录模板

## 章节情绪档案

```markdown
# 章节：第X章

## 基本信息
- 章节ID：
- 情绪阶段：
- 情绪类型：
- 综合情绪分：

## 主角情绪状态

| 情绪维度 | 当前值 | 变化 | 原因 |
|----------|--------|------|------|
| 恐惧 | | | |
| 愤怒 | | | |
| 压抑 | | | |
| 兴奋 | | | |
| 冷静 | | | |
| 绝望 | | | |
| 掌控感 | | | |

## 情绪变化原因

【本章发生的情绪触发事件】

## 情绪驱动决策

【情绪变化导致了什么决策/行动】

## 情绪曲线

【本章情绪曲线描述】
- 开头情绪：
- 中间变化：
- 结尾情绪：

## 下一章情绪铺垫

【为下一章留的情绪钩子】

## 情绪分值计算

EMOTION_SCORE = 
  0.30 × 情绪波动强度 +
  0.30 × 情绪冲突强度 +
  0.20 × 情绪释放强度 +
  0.20 × 情绪代入感
```

---

## 情绪报告生成

```json
{
  "chapter_id": 1,
  "emotion_score": 0,
  "protagonist_emotion": {
    "fear": 0,
    "anger": 0,
    "depression": 0,
    "excitement": 0,
    "calm": 0,
    "despair": 0,
    "control": 0
  },
  "global_emotion_tone": "",
  "emotion_change": "",
  "emotion_trigger": "",
  "emotion_driven_decision": "",
  "next_hook_emotion": ""
}
```