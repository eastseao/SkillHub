# 全流水线执行示例

## 目标

生成1000章工业修仙小说

## 初始化

```
接收目标：修仙题材 / 1000章 / 升级流
初始化Agent注册表
构建DAG任务图
```

## Phase 1（基础构建）

```
[并行] 01_world_builder     → 修仙世界观
[并行] 02_character_builder → 主角+配角
[并行] 03_power_system      → 筑基-金丹-元婴体系
[串行] 04_faction_system    → 宗门+势力
```

## Phase 2（剧情设计）

```
[串行] 05_master_plot       → 主线：废物逆袭→飞升
[串行] 06_arc_designer      → Arc1-20设计
```

## Phase 3-6（单章循环）

```
Arc 1（50章）：
  [循环 50次]
    07_chapter_engine → 08_memory_sync → 09_style → 11_qc
    QC PASS → 10_platform_adapter → 输出
    QC FAIL → 回滚07重写
  [Arc级QC]
  Arc PASS → 下一Arc
```

## 输出结构

```
/novel/
├── world/
├── characters/
├── arcs/
│   ├── arc_01/
│   ├── arc_02/
│   └── ...
├── platform/
│   ├── qidian/
│   ├── fanqie/
│   └── ...
└── qc/
    ├── chapter_001_qc.md
    └── ...
```

## 监控状态

- 已完成：Phase 1-2（初始化）
- 进行中：Arc 1 Chapter 23/50
- QC通过率：95%（22/23）
- 系统稳定性：98%