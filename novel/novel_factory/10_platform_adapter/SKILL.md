---
name: 10-platform-adapter
description: |
  将同一小说内容自动适配不同平台的写作风格，
  包括起点、番茄、晋江、Webnovel等，
  自动调整节奏、语言密度、标题、爽点表达方式，
  实现"一稿多平台爆款分发"。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - chapter_output
  - arc_output
  - style_system
  - target_platform

output:
  - /platform/qidian/*.md
  - /platform/fanqie/*.md
  - /platform/jinjiang/*.md
  - /platform/webnovel/*.md
  - /platform/short/*.md

rules:
  - 必须保持剧情一致
  - 必须调整语言风格
  - 必须优化平台阅读习惯
  - 必须强化平台核心爽点逻辑
  - 必须调整节奏结构
  - 必须优化标题与钩子
  - 禁止改变主线剧情
  - 禁止改变人物设定
  - 必须最大化平台留存率
  - 必须适配推荐算法逻辑

workflow:
  1. 识别目标平台
  2. 分析平台阅读习惯
  3. 分析当前章节结构
  4. 重写语言风格
  5. 重构节奏密度
  6. 强化钩子与冲突
  7. 优化标题与开头
  8. 输出平台版本