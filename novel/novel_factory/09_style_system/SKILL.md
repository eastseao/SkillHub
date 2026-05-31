---
name: 09-style-system
description: |
  控制长篇小说的整体写作风格，包括叙事语气、
  对话风格、动作描写方式、情绪表达节奏、
  信息密度控制与爽点表达方式，
  确保1000+章节风格统一且稳定。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - genre
  - world_build
  - character_system
  - power_system
  - master_plot

output:
  - /style/style_profile.md
  - /style/narration_rules.md
  - /style/dialogue_rules.md
  - /style/action_rules.md
  - /style/emotional_rules.md
  - /style/pacing_rules.md

rules:
  - 全书风格必须统一
  - 不同角色对话必须区分风格
  - 战斗描写必须风格一致
  - 情绪表达必须符合基调
  - 禁止风格随机变化
  - 必须符合题材类型
  - 必须适配长篇节奏
  - 必须服务爽点结构
  - 必须可机器执行
  - 必须支持1000+章节

workflow:
  1. 定义整体风格基调
  2. 定义叙事语气规则
  3. 定义对话风格规则
  4. 定义动作描写风格
  5. 定义情绪表达方式
  6. 定义节奏控制方式
  7. 定义信息密度规则
  8. 定义禁用风格
  9. 输出风格系统