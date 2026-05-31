---
name: 04-faction-system
description: |
  生成长篇网络小说中的完整势力系统，
  包含国家、宗门、商会、组织、联盟、
  内部结构、经济体系、军事体系、
  权力结构、势力冲突与长期演化。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - 世界观设定
  - 地理结构
  - 历史背景
  - 力量体系
  - 核心冲突

output:
  - /factions/empire.md
  - /factions/sects.md
  - /factions/guilds.md
  - /factions/hidden_orgs.md
  - /factions/alliances.md
  - /factions/relationships.md
  - /factions/conflict_map.md
  - /factions/economy.md
  - /factions/military.md

rules:
  - 所有势力必须有明确目标
  - 所有势力必须有经济来源
  - 所有势力必须有军事能力
  - 所有势力必须有内部矛盾
  - 禁止无意义组织
  - 势力之间必须存在冲突
  - 必须存在隐藏势力
  - 必须存在势力演化路径
  - 必须支持1000章以上扩展
  - 必须支持权力更替

workflow:
  1. 生成势力类型体系
  2. 生成主要势力
  3. 生成内部结构
  4. 生成经济系统
  5. 生成军事系统
  6. 生成势力关系网
  7. 生成冲突系统
  8. 生成隐藏势力
  9. 生成势力演化路径
  10. 输出完整势力体系