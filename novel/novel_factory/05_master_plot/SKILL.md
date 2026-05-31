---
name: 05-master-plot
description: |
  生成长篇网络小说的总剧情系统，
  控制主线、冲突、节奏、伏笔、
  多势力战争、角色成长与结局设计，
  支持1000+章节持续推进。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - 世界观设定
  - 力量体系
  - 角色体系
  - 势力系统
  - 小说类型
  - 目标章节数

output:
  - /plot/master_plot.md
  - /plot/arcs/*.md
  - /plot/conflicts.md
  - /plot/mysteries.md
  - /plot/foreshadowing.md
  - /plot/emotional_lines.md
  - /plot/timeline.md

rules:
  - 主线必须贯穿全局
  - 必须存在阶段性目标
  - 必须存在递进冲突
  - 必须存在伏笔与回收
  - 禁止剧情断裂
  - 禁止无意义重复冲突
  - 必须支持1000+章节
  - 必须支持多势力战争演化
  - 必须支持角色成长驱动剧情
  - 必须控制节奏递进

workflow:
  1. 构建全局主线
  2. 设定核心矛盾
  3. 生成阶段剧情结构
  4. 设计多卷Arc
  5. 构建伏笔系统
  6. 构建谜题系统
  7. 设计情绪曲线
  8. 设计高潮节点
  9. 构建结局路径
  10. 输出完整剧情蓝图