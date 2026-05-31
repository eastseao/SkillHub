---
name: 14-auto-viral-rewriter
description: |
  自动将中等质量小说章节（60-75分）重写为高爆款章节（85-95分），
  在不改变主线剧情的前提下，优化冲突密度、爽点结构、节奏与钩子，
  提升番茄小说推荐系统通过率。
version: 1.0.0

input:
  - chapter
  - qc_score
  - prediction_report

output:
  - rewritten_chapter
  - improved_score_report

rules:
  - 不得改变主线剧情
  - 必须增强冲突密度
  - 必须强化开头3秒钩子
  - 必须强化结尾悬念
  - 必须提升情绪波动
  - 必须减少无效描述
  - 必须增加爽点密度
  - 必须优化节奏结构
  - 必须保持角色一致性
  - 禁止过度润色