# 全小说生成流水线

## 完整阶段（12步）

```
Phase 1: 基础构建
  01_world_builder     → 世界观
  02_character_builder → 角色
  03_power_system      → 力量体系
  04_faction_system    → 势力体系

Phase 2: 剧情设计
  05_master_plot       → 主线剧情
  06_arc_designer      → Arc设计

Phase 3: 内容生成
  07_chapter_engine    → 章节生成

Phase 4: 保障系统
  08_memory_manager   → 记忆同步
  09_style_system     → 风格控制

Phase 5: 输出分发
  10_platform_adapter → 平台适配

Phase 6: 质检发布
  11_quality_control  → 质量检测

Phase 7: 循环控制
  12_loop_control     → 循环生成
                       ↓
              ┌─────────────────┐
              │  QC PASS → 下一章 │
              │  QC FAIL → 回滚  │
              └─────────────────┘
```

## 初始化阶段

1. 接收生成目标（题材/字数/风格）
2. 初始化所有Agent注册表
3. 构建DAG任务图
4. 分配执行优先级

## 执行原则

- Phase 1 必须全部完成才能进入 Phase 2
- Phase 2 必须全部完成才能进入 Phase 3
- Phase 3-7 每个章节循环执行
- QC FAIL 触发回滚，不进入下一阶段