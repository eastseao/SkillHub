---
name: 07-chapter-engine
description: |
  长篇工业级章节生成引擎，
  负责根据Arc、剧情状态、角色状态、
  世界状态与风格系统生成完整章节内容。

  强制要求：
  - 每章最低3500中文字符
  - 不设字数上限
  - 必须具备完整节奏结构
  - 必须包含冲突推进
  - 必须包含情绪变化
  - 必须包含章节钩子

version: 2.0.0

author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - current_arc
  - master_plot
  - memory_system
  - style_system
  - faction_system
  - power_system

output:
  - /chapters/chapter_xxx.md

rules:
  - 每章不少于3500中文字符
  - 不设字数上限
  - 禁止短章节
  - 禁止无冲突章节
  - 禁止无剧情推进
  - 禁止流水账
  - 必须有节奏变化
  - 必须有情绪变化
  - 必须有结尾钩子
  - 必须符合style_system
  - 必须符合memory_manager
  - 必须通过quality_control

workflow:
  1. 读取剧情状态
  2. 读取Arc目标
  3. 读取memory状态
  4. 读取style规则
  5. 规划章节结构
  6. 生成正文
  7. 自动扩写
  8. 检查字数
  9. 检查节奏
  10. 输出章节