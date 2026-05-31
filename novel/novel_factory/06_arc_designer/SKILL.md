---
name: 06-arc-designer
description: |
  将小说总剧情拆分为可执行"卷级结构（Arc）"，
  每个Arc具备明确目标、冲突、BOSS、高潮、
  奖励、世界升级与角色成长，
  支持1000+章节工业级小说结构设计。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - master_plot.md
  - world_build
  - character_system
  - faction_system
  - power_system
  - target_chapters

output:
  - /arcs/arc_001.md
  - /arcs/arc_002.md
  - /arcs/arc_003.md
  - /arcs/arc_map.md

rules:
  - 每个Arc必须有明确目标
  - 每个Arc必须有冲突升级
  - 每个Arc必须有最终Boss
  - 每个Arc必须改变世界状态
  - 每个Arc必须推动主角成长
  - 每个Arc必须有奖励机制
  - 禁止Arc重复结构
  - 禁止无意义过渡Arc
  - 必须支持1000+章节
  - Arc之间必须递进升级

workflow:
  1. 解析主线结构
  2. 切分故事阶段
  3. 设计Arc目标
  4. 设计Arc冲突
  5. 设计Arc Boss
  6. 设计Arc高潮
  7. 设计Arc奖励
  8. 设计世界变化
  9. 设计角色成长
  10. 输出Arc地图