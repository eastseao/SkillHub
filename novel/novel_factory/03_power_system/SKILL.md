---
name: 03-power-system
description: |
  生成适用于长篇网络小说的完整力量体系，
  包含修炼体系、境界、技能、装备、
  血脉、资源、怪物、战斗规则、
  力量限制与成长路线。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - 世界观设定
  - 小说题材
  - 文明等级
  - 世界规则
  - 核心冲突

output:
  - /power/cultivation_system.md
  - /power/realm_system.md
  - /power/combat_rules.md
  - /power/skills.md
  - /power/equipment.md
  - /power/bloodlines.md
  - /power/talents.md
  - /power/resources.md
  - /power/monsters.md
  - /power/forbidden_powers.md
  - /power/advancement_rules.md
  - /power/power_limits.md

rules:
  - 力量体系必须自洽
  - 境界差距必须明确
  - 必须存在力量限制
  - 必须存在成长代价
  - 必须支持长期扩展
  - 禁止后期战力崩坏
  - 技能必须存在克制关系
  - 资源必须稀缺
  - 装备必须存在等级体系
  - 必须支持1000章成长

workflow:
  1. 生成力量来源
  2. 生成境界体系
  3. 生成战斗规则
  4. 生成技能系统
  5. 生成装备体系
  6. 生成血脉与天赋
  7. 生成怪物系统
  8. 生成资源系统
  9. 生成禁忌力量
  10. 输出完整力量体系