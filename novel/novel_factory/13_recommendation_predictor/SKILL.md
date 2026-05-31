---
name: 13-recommendation-predictor
description: |
  模拟番茄小说推荐算法系统，
  对小说章节进行CTR预测、留存预测、爆款概率评估，
  并模拟进入推荐池后的流量增长路径。
version: 1.0.0

input:
  - chapter
  - title
  - hook
  - style_system

output:
  - prediction_report.md

rules:
  - 必须输出数值评分（0-100）
  - 必须模拟推荐路径
  - 必须预测是否进入爆款池
  - 必须给优化建议