# 07_chapter_engine 章节引擎

## 定位

> 🧠 **"逐帧拍摄 + 写作执行器"**

如果说：
- `05 master_plot` = 总导演
- `06 arc_designer` = 分镜脚本

那么：
- `07 chapter_engine` = 逐帧拍摄 + 写作执行器

## 核心使命

将 Arc 级剧情拆分为**可直接发布**的网文章节文本。

## 调用顺序

```
05_master_plot（总剧情）
↓
06_arc_designer（卷级结构）
↓
07_chapter_engine（← 本模块：章节正文）
```

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 章节核心引擎 | prompts/chapter_core_engine.md | 生成章节框架 |
| 场景构建器 | prompts/scene_builder.md | 构建3~6个递进场景 |
| 冲突执行器 | prompts/conflict_executor.md | 即时/潜在/升级冲突 |
| 情绪节拍器 | prompts/emotional_beats.md | 情绪曲线控制 |
| 节奏控制器 | prompts/pacing_controller.md | 快慢节奏交替 |
| 对话引擎 | prompts/dialogue_engine.md | 推动冲突的对话 |
| 动作引擎 | prompts/action_engine.md | 战斗与行为描写 |
| 结尾钩子引擎 | prompts/cliffhanger_engine.md | 悬念结尾 |
| 信息控制系统 | prompts/information_control.md | 分层信息释放 |
| 视角管理器 | prompts/perspective_manager.md | 叙事视角控制 |
| 章节连续性 | prompts/chapter_continuity.md | 防崩检查 |
| 防水文控制 | prompts/anti_water_control.md | 删除冗余 |

## 章节生成流程

```
1. 读取Arc目标
2. 分析章节任务
3. 构建冲突
4. 构建场景
5. 构建对话
6. 构建动作
7. 控制信息释放
8. 控制节奏
9. 生成结尾钩子
10. 输出章节
```

## 章节类型

| 类型 | 适用场景 | 节奏要求 |
|------|---------|----------|
| 战斗章节 | 高潮/对抗 | 高强度快节奏 |
| 情感章节 | 感情戏 | 情绪波动大 |
| 剧情揭示章节 | 身世/秘密揭露 | 信息密度高 |
| 过渡章节 | 上下Arc衔接 | 快过渡 |

## 章节结构

```
├── ch_001.md     ← 第1章
├── ch_002.md     ← 第2章
├── ch_003.md     ← 第3章
└── ch_map.md     ← 章节总地图
```

## 核心设计原则

| 原则 | 说明 |
|------|------|
| 每章必须有冲突 | 没有冲突 = 水文 |
| 每章必须有推进 | 否则没有意义 |
| 每章必须有钩子 | 否则读者流失 |
| 每章必须有情绪变化 | 不能平淡如水 |
| 每章必须受Arc约束 | 否则系统崩坏 |

## 高级扩展系统

### 章节压缩系统

自动删减无效内容。

### 情绪曲线系统

章节内部必须有起伏。

### 伏笔植入系统

每章至少1个伏笔。

### 钩子强化系统

每章结尾必须让人想继续看。

## 质量检查

- [ ] 有无冲突？
- [ ] 有无推进？
- [ ] 有无钩子？
- [ ] 有无情绪波动？
- [ ] 有无角色互动？
- [ ] 描写占比≤15%？
- [ ] 有无冗余内容？

## 驱动Agent

生成章节后驱动：
- 战斗Agent
- 剧情Agent
- 角色Agent
- QA Agent
- 记忆Agent