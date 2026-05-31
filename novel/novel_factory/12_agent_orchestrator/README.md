# 12_agent_orchestrator 总调度器

## 定位

> 🧠 **"AI小说工业系统的唯一总控制器（操作系统级调度内核）"**

如果说：

- `01-06` = 故事设计层
- `07 chapter_engine` = 写作生产线
- `08 memory_manager` = 记忆系统
- `09 style_system` = 风格统一
- `10 platform_adapter` = 多平台输出
- `11 quality_control` = 质检系统

那么：

- `12 agent_orchestrator` = **统治所有模块的"AI小说操作系统内核"**

## 核心使命

控制整条AI小说生产线所有Agent的**唯一全局调度核心**，确保1000+章节小说工业化持续生成。

## 调用顺序（唯一入口）

```
12_agent_orchestrator
↓调度所有系统↓
01 → 02 → 03 → 04 → 05 → 06 → 07 → 08 → 09 → 10 → 11
                         ↑___________________________↓
                              loop control（循环生成）
```

## 7大阶段流水线

| 阶段 | Agent | 作用 |
|------|-------|------|
| Phase 1 | 01-04 | 基础构建（世界/角色/力量/势力） |
| Phase 2 | 05-06 | 剧情设计（主线/Arc） |
| Phase 3 | 07 | 内容生成（章节写作） |
| Phase 4 | 08-09 | 保障系统（记忆/风格） |
| Phase 5 | 10 | 输出分发（多平台） |
| Phase 6 | 11 | 质检发布（QC门禁） |
| Phase 7 | 12 | 循环控制（持续推进） |

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 总调度核心 | prompts/orchestrator_core_engine.md | 唯一入口，全局控制 |
| Agent注册中心 | prompts/agent_registry.md | 所有Agent注册与状态 |
| 工作流调度器 | prompts/workflow_scheduler.md | 并行/串行执行控制 |
| 任务路由器 | prompts/task_router.md | 任务分配到Agent |
| 依赖管理器 | prompts/dependency_manager.md | 管理依赖关系 |
| 记忆同步控制 | prompts/memory_sync_controller.md | 协调08记忆系统 |
| 质量门控制 | prompts/quality_gate_controller.md | 调用11质检 |
| 循环控制引擎 | prompts/loop_control_engine.md | 支持1000+章循环 |
| 冲突解决引擎 | prompts/conflict_resolution_engine.md | Agent冲突处理 |
| 优先级调度器 | prompts/priority_scheduler.md | 执行优先级控制 |
| 系统健康监控 | prompts/system_health_monitor.md | 监控运行状态 |
| 流水线控制 | prompts/production_pipeline_controller.md | 全流程控制 |

## DAG任务图

```
01_world_builder ─┐
02_character ─────┼──→ 05_master_plot ──→ 06_arc_designer
03_power_system ──┤         ↑                  │
04_faction ───────┘         │                  ↓
                     07_chapter_engine ←┐  [循环]
                            ↓            │
                     08_memory_manager  │
                            ↓            │
                     09_style_system    │
                            ↓            │
                     11_quality_control ┘
                            ↓
                     10_platform_adapter
```

## 优先级体系

| 优先级 | Agent |
|--------|-------|
| Critical | 11 QC / 08 记忆 |
| High | 05 剧情 / 06 Arc / 07 章节 |
| Medium | 09 风格 / 10 平台 |
| Low | 01-04 基础构建 |

## 四大高级系统

### 1、DAG任务图系统

所有Agent形成有向无环图，依赖关系明确，不可逆向执行。

### 2、失败自动修复系统

```
QC失败 → 回滚07重写（最多3次）
超出重试 → 应急修复流程 → 人工干预
```

### 3、并行Agent执行系统

最多3个Agent并行，支持多个章节同时生成。

### 4、循环生成系统

```
QC PASS → 推进下一章
QC FAIL → 回滚重写
Arc结束 → 下一Arc
```

## 输出结构

```
/orchestration/
├── execution_plan.md     ← 执行计划
├── task_graph.json      ← DAG任务图
├── system_status.md      ← 系统状态
└── final_output.md      ← 最终输出
```

## 四大核心原则

| 原则 | 说明 |
|------|------|
| **唯一大脑** | 不是工具，是控制系统；所有Agent必须受控 |
| **依赖有序** | 必须遵循DAG，不能逆向执行 |
| **QC门禁** | 质量不通过则阻断全流程 |
| **可恢复** | 支持失败回滚、任务重试、死锁打破 |

## 应急修复

| 问题类型 | 修复Agent | 回滚点 |
|----------|-----------|--------|
| 剧情断裂 | 05/07 | 最近QC通过章节 |
| 角色崩坏 | 02/07 | 最近角色一致章节 |
| 战力崩坏 | 03/07 | 最近战力一致章节 |
| 记忆冲突 | 08 | 冲突点之前状态 |
| 风格漂移 | 09 | 最近风格一致章节 |

## 最终效果

输入：
```
写一部1000章工业修仙小说
```

输出：
```
/orchestration/
├── execution_plan.md
├── task_graph.json
└── final_output.md
```

并驱动整个系统自动运行，从01到12完整流水线，循环生成直到1000章完成。

---

> 🏭 **Novel OS v1.0 — AI工业级长篇小说生产操作系统**