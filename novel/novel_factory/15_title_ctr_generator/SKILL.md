---
name: 15-title-ctr-generator
description: |
  面向番茄小说推荐算法的爆款标题生成与CTR预测系统，
  自动生成多个标题候选，并通过点击率模型评分排序，
  输出最优点击率标题。
version: 1.0.0

input:
  - chapter_summary
  - conflict
  - emotion
  - protagonist_state

output:
  - ranked_titles.md

rules:
  - 必须生成至少10个标题
  - 必须输出CTR评分
  - 必须优先冲突与爽点
  - 必须符合平台推荐逻辑
  - 必须排名排序输出最优