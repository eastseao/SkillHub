# 05_master_plot 总剧情引擎

## 定位

整个 AI 小说工厂的**总导演 / 总调度 / 世界叙事 CPU**。

负责驱动：
- 1000+ 章主线不崩
- 全局矛盾推进
- 多势力战争节奏
- 人物成长节拍
- 伏笔埋设与回收
- 剧情阶段切换
- 爽点密度控制

## 调用顺序

```
01_world_builder
↓
02_character_builder
↓
03_power_system
↓
04_faction_system
↓
05_master_plot（← 本模块）
```

## 核心设计原则

| 原则 | 说明 |
|------|------|
| 主线不可中断 | 否则小说直接崩 |
| 剧情持续升级 | 不能停留在同一层世界 |
| 冲突必须递增 | 不能重复打同一类型敌人 |
| 伏笔必须跨章 | 否则没有长篇张力 |

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 总剧情引擎 | prompts/core_story_engine.md | 构建全局主线 |
| 全局冲突 | prompts/global_conflict.md | 贯穿全书的核心矛盾 |
| 分卷系统 | prompts/plot_arc_generator.md | 将主线拆分为多个Arc |
| 伏笔系统 | prompts/foreshadowing_system.md | 跨100章回收伏笔 |
| 谜题系统 | prompts/mystery_system.md | 长期未解谜团 |
| 高潮引擎 | prompts/climax_engine.md | 全书高潮节点设计 |
| 节奏控制 | prompts/pacing_controller.md | 爽点/冲突/情绪递增 |
| 世界推进 | prompts/world_stage_progression.md | 世界升级与地图扩展 |
| 角色融合 | prompts/character_integration.md | 角色与主线的绑定 |
| 势力战争 | prompts/faction_war_flow.md | 势力冲突演化 |
| 情绪线 | prompts/emotional_line_engine.md | 贯穿全文的情绪曲线 |
| 结局设计 | prompts/ending_design.md | 多结局路径设计 |

## 核心规则

### 节奏规则
- 初期（1-100章）：快速建冲突，3章内出爆点
- 中期（100-600章）：稳步升级，每50章大高潮
- 后期（600-1000+章）：持续爆发，冲突不断

### 爽点递增
- 初期：1-2个小爽点/章
- 中期：2-3个爽点/章
- 后期：3-4个爽点/章

### 冲突升级
- 初期：个人冲突
- 中期：势力冲突
- 后期：世界冲突

### 反崩规则
- 每个Arc必须改变世界状态
- 禁止静止世界
- 禁止重复同级敌人
- 每50-100章必须回收伏笔

## 输出结构

```
/plot/
├── master_plot.md       ← 总剧情蓝图
├── arcs/                ← 分卷详细结构
├── conflicts.md         ← 核心冲突列表
├── mysteries.md         ← 谜题列表
├── foreshadowing.md    ← 伏笔列表
├── emotional_lines.md   ← 情绪曲线
└── timeline.md          ← 时间线
```

## 高级系统

### 剧情压力系统
冲突密度随章节增长，敌人强度随章节增长，世界规模随章节扩展。

### 伏笔回收系统
每50-100章回收伏笔，每个Arc回收1-2个旧伏笔、埋设3-5个新伏笔。

### 世界升级系统
每个Arc世界升级一次（局部 → 区域 → 大陆 → 世界 → 多界）。