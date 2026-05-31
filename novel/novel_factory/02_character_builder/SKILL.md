---
name: 02-character-builder
description: |
  生成适用于长篇网络小说的完整角色系统，
  包含主角、反派、女主、配角、NPC、
  性格锁定、人物弧光、关系网、
  对话风格与成长路线。
version: 1.0.0
author: eastseao

tools:
  - read
  - write
  - edit

input:
  - 世界观设定
  - 小说题材
  - 主线类型
  - 故事风格
  - 势力体系
  - 力量体系

output:
  - /characters/protagonist.md
  - /characters/villains.md
  - /characters/heroines.md
  - /characters/supporting_roles.md
  - /characters/npc_database.md
  - /characters/relationships.md
  - /characters/dialogue_styles.md
  - /characters/growth_arcs.md
  - /characters/personality_locks.md

rules:
  - 所有角色必须拥有核心欲望
  - 所有角色必须拥有缺陷
  - 主角必须存在成长弧线
  - 反派必须拥有合理动机
  - 禁止角色工具人化
  - 禁止角色性格随机变化
  - 必须存在角色关系演化
  - 对话风格必须可区分
  - 必须支持1000章以上成长
  - 必须支持长期情绪积累

workflow:
  1. 生成主角
  2. 生成主要反派
  3. 生成核心配角
  4. 生成关系网络
  5. 生成对话风格
  6. 生成成长路线
  7. 生成人格锁定规则
  8. 输出角色数据库