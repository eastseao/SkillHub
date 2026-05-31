# 08_memory_manager 记忆管理器

## 定位

> 🧠 **"不会遗忘的小说大脑系统（工业级记忆中枢）"**

如果说：
- `07 chapter_engine` = 写"这一章"
- `06 arc_designer` = 写"这一卷"
- `05 master_plot` = 写"整本书"

那么：
- `08 memory_manager` = 让整本书"不会忘事、不崩设定、不人格分裂"的大脑

## 核心使命

管理长篇小说中的**长期记忆系统**，确保1000+章节不崩设定、不忘伏笔、不人格分裂。

## 调用顺序

```
07_chapter_engine
↓
08_memory_manager
↓
（回写）
07_chapter_engine
```

形成闭环：**写作 → 记忆 → 校验 → 再写作**

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 记忆核心引擎 | prompts/memory_core_engine.md | 统一入口 |
| 角色记忆系统 | prompts/character_memory.md | 记录角色状态/性格/关系 |
| 世界记忆系统 | prompts/world_memory.md | 记录地图/法则/环境变化 |
| 势力记忆系统 | prompts/faction_memory.md | 记录势力消长/战争/联盟 |
| 力量记忆系统 | prompts/power_memory.md | 记录境界/技能/装备变化 |
| 剧情记忆系统 | prompts/plot_memory.md | 记录Arc进度/伏笔/未解谜题 |
| 事件记忆系统 | prompts/event_memory.md | 按时间线记录所有关键事件 |
| 关系记忆系统 | prompts/relationship_memory.md | 记录角色间关系变化 |
| 矛盾检测器 | prompts/contradiction_detector.md | 检测设定漂移/战力崩坏 |
| 记忆更新引擎 | prompts/memory_update_engine.md | 增量更新，不覆盖历史 |
| 记忆压缩系统 | prompts/memory_compression.md | 防止记忆爆炸 |
| 记忆检索系统 | prompts/memory_retrieval_engine.md | 按需调用历史信息 |
| 时间轴系统 | prompts/timeline_manager.md | 事件按时间线排列 |
| 因果链系统 | prompts/causality_chain.md | 事件可追溯原因 |
| 状态锁系统 | prompts/state_lock_system.md | 核心设定不可覆盖 |

## 四大核心原则

| 原则 | 说明 |
|------|------|
| **记忆必须"可追溯"** | 否则无法修复崩坏 |
| **记忆必须"增量更新"** | 否则信息丢失 |
| **记忆必须"结构化"** | 否则无法检索 |
| **记忆必须"可压缩"** | 否则1000章后爆炸 |

## 输出结构

```
/memory/
├── character_memory.json    ← 角色状态/性格/关系
├── world_memory.json        ← 世界地图/法则/环境
├── faction_memory.json      ← 势力消长
├── power_memory.json        ← 境界/技能/装备
├── plot_memory.json         ← Arc进度/伏笔
├── event_memory.json        ← 事件时间线
├── relationship_memory.json ← 关系网络
└── contradictions.md        ← 矛盾检测报告
```

## 矛盾检测体系

| 严重程度 | 处理方式 |
|----------|----------|
| Critical | 立即修复（逻辑崩坏） |
| High | 必须修复（明显矛盾） |
| Medium | 警告+记录（轻微问题） |
| Low | 仅记录（潜在问题） |

## 触发时机

- 每章生成完成后
- 每个Arc完成后
- 关键事件发生时

## 高级系统

### 时间轴系统
所有事件按时间线记录，标注Arc/章节。

### 因果链系统
每个结果有原因，每个原因有来源，因果链不断裂。

### 状态锁系统
锁定核心设定（世界法则/力量上限/关键NPC），防止意外覆盖。

### 记忆压缩系统
每50章或文件>10MB时压缩，保留关键事件，删除冗余描述。

## 一致性检查

### 角色一致性
- 性格是否漂移
- 能力是否跳跃
- 记忆是否矛盾

### 世界一致性
- 法则是否统一
- 地理是否矛盾
- 时间线是否正确

### 势力一致性
- 实力是否平衡
- 关系是否合理
- 行动是否符合逻辑