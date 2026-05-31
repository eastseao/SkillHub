# 06_arc_designer 卷纲生成器

## 定位

> 🧠 **"切割1000章小说结构的骨架设计器"**

负责把总剧情（05）切成"可执行的卷（Arc）"，每卷50~200章，每卷都有爽点闭环 + 升级 + 冲突 + 结算。

## 调用顺序

```
05_master_plot（总剧情）
↓
06_arc_designer（← 本模块：卷级结构）
↓
07_chapter_engine（章节生成）
```

## 核心设计原则

| 原则 | 说明 |
|------|------|
| Arc必须有结算 | 没有结算 = 水文 |
| Arc必须改变世界 | 否则没有长篇意义 |
| Arc必须升级冲突 | 否则会重复 |
| Arc必须服务主线 | 否则偏题崩盘 |

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| Arc核心生成 | prompts/arc_core.md | 生成卷级结构 |
| Arc目标系统 | prompts/arc_goal_system.md | 主目标/子目标/隐藏目标 |
| Arc冲突系统 | prompts/arc_conflict_system.md | 势力/资源/人物/价值观冲突 |
| Arc Boss系统 | prompts/arc_boss_system.md | 最终对手/镜像设定 |
| Arc高潮系统 | prompts/arc_climax_system.md | 情绪爆发/战力爆发/反转 |
| Arc奖励系统 | prompts/arc_reward_system.md | 战力/资源/技能/新目标 |
| 世界扩展系统 | prompts/arc_world_expansion.md | 新地图/新势力/世界升级 |
| 角色成长系统 | prompts/arc_character_progression.md | 主角/女主/反派/关系变化 |
| 势力变化系统 | prompts/arc_faction_shift.md | 势力格局重组 |
| Arc过渡系统 | prompts/arc_transition_system.md | 前后Arc衔接/悬念点 |

## Arc链式生成规则

每个Arc结束时检查：
- [ ] 世界是否升级？
- [ ] 敌人是否更强？
- [ ] 奖励是否推动下一Arc？
- [ ] 伏笔是否回收？
- [ ] 新伏笔是否埋下？
- [ ] 悬念是否延续？

## 长篇Arc分布

| 阶段 | Arc数量 | 每Arc章节 | Boss等级 |
|------|---------|-----------|----------|
| 初期 | 1-3个 | 30-50章 | 底层势力代表 |
| 中期 | 3-5个 | 50-100章 | 势力领袖 |
| 后期 | 2-3个 | 100-200章 | 终极Boss |

## 升级规则

- 每一Arc敌人比上一Arc强至少30%
- 每一Arc世界范围扩大至少50%
- 每一Arc奖励提升至少一个档次
- 冲突规模：个人 → 势力 → 帝国 → 世界 → 多界

## 输出结构

```
/arcs/
├── arc_001.md     ← 第1卷详细结构
├── arc_002.md     ← 第2卷详细结构
├── arc_003.md     ← 第3卷详细结构
└── arc_map.md     ← Arc总地图（所有卷一览）
```

## 高级系统

### Arc动态升级系统
Arc会随剧情自动拆分或合并。

### Arc难度递增系统
后期Arc强度必须指数级提升。

### Arc世界层级系统
每个Arc提升世界层级（局部→大陆→世界→多界）。