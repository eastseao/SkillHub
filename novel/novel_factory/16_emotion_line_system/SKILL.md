---
name: 16-emotion-line-system
description: |
  管理小说中的情感发展系统，包括主角情感曲线、人物关系情感网络、情绪驱动剧情设计，
  用于增强读者持续阅读动力与情绪黏性。
version: 1.0.0

input:
  - chapter_output
  - character_system
  - plot_system

output:
  - emotion_state.json
  - emotion_graph.json
  - emotion_report.md

rules:
  - 情感必须贯穿全书
  - 每章必须有情绪变化
  - 情感必须影响剧情决策
  - 禁止无情绪章节
  - 情感必须可量化
  - 情绪驱动剧情，非装饰
  - 每章必须有情绪变化，否则判水文