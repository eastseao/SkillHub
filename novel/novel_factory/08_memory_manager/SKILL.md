---
name: 08-memory-manager
description: |
  管理长篇小说中的长期记忆系统，
  包括人物状态、世界状态、势力变化、
  战力变化、剧情进度、伏笔、关系网络，
  并负责一致性校验与冲突修复。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - chapter_output
  - arc_state
  - master_plot
  - character_system
  - faction_system
  - power_system

output:
  - /memory/character_memory.json
  - /memory/world_memory.json
  - /memory/faction_memory.json
  - /memory/plot_memory.json
  - /memory/event_memory.json
  - /memory/relationship_memory.json
  - /memory/contradictions.md

rules:
  - 必须记录所有关键事件
  - 必须更新角色状态
  - 必须更新势力变化
  - 必须更新世界状态
  - 必须检测逻辑冲突
  - 必须压缩旧信息
  - 禁止信息丢失
  - 禁止设定漂移
  - 必须支持1000+章节
  - 必须可追溯所有变化

workflow:
  1. 解析章节内容
  2. 提取关键事件
  3. 更新角色记忆
  4. 更新世界记忆
  5. 更新势力记忆
  6. 更新剧情状态
  7. 检测逻辑冲突
  8. 压缩旧记忆
  9. 写入长期存储