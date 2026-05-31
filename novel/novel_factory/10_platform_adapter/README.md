# 10_platform_adapter 平台适配器

## 定位

> 🌐 **"一稿多平台爆款适配引擎（商业级小说分发系统）"**

如果说：

- `07 chapter_engine` = 写"这一章"
- `08 memory_manager` = 让整本书"不崩设定"
- `09 style_system` = 决定"这本书读起来像谁写的"
- 那么
- `10 platform_adapter` = 把同一部小说"自动适配成不同平台的爆款版本"

## 核心使命

把同一部小说内容，**一次输入，多平台输出爆款版本**。

## 调用顺序

```
07_chapter_engine
↓
09_style_system
↓
10_platform_adapter
```

## 五大平台适配

| 平台 | 风格 | 节奏 | 字数 | 钩子强度 |
|------|------|------|------|----------|
| 起点 | 长铺垫+世界观 | 中慢 | 3000-5000 | 中 |
| 番茄 | 强冲突+快节奏 | 快 | 1500-2500 | 极强 |
| 晋江 | 情绪+心理 | 细腻 | 2000-4000 | 中 |
| Webnovel | 国际化+简洁 | 清晰 | 2000-3000 | 高 |
| 短内容 | 极压缩+高冲击 | 爆发 | 500-1000 | 极端 |

## 核心模块

| 模块 | 文件 | 作用 |
|------|------|------|
| 平台核心引擎 | prompts/platform_core_engine.md | 统一入口 |
| 起点适配器 | prompts/qidian_adapter.md | 适配起点 |
| 番茄适配器 | prompts/fanqie_adapter.md | 适配番茄 |
| 晋江适配器 | prompts/jinjiang_adapter.md | 适配晋江 |
| Webnovel适配器 | prompts/webnovel_adapter.md | 适配国际版 |
| 短内容适配器 | prompts/short_form_adapter.md | 适配短视频 |
| 标题优化器 | prompts/title_optimizer.md | 生成爆款标题 |
| 钩子优化器 | prompts/hook_optimizer.md | 强化各位置钩子 |
| 节奏重写器 | prompts/pacing_rewriter.md | 调整节奏密度 |
| 语言简化器 | prompts/language_simplifier.md | 降低认知成本 |
| 情绪放大器 | prompts/emotional_amplifier.md | 放大爽点冲突 |
| 商业化优化器 | prompts/monetization_optimizer.md | 提升转化率 |

## 三大核心原则

| 原则 | 说明 |
|------|------|
| **剧情不能变** | 只改"表达"，不改"内容" |
| **平台优先** | 不是文学优先，是转化率优先 |
| **钩子优先** | 所有平台都强化"继续读欲望" |

## 高级系统

### 1、平台策略映射系统

不同平台对应不同写作策略（节奏/语言/钩子）

### 2、爆款钩子强化系统

自动生成"点击欲"，前3秒必须抓人

### 3、推荐算法适配系统

适配平台分发机制，最大化推荐量

### 4、多平台并行适配

一次输入，并行输出5个平台版本

## 输出结构

```
/platform/
├── qidian/
│   └── ch_xxx.md
├── fanqie/
│   └── ch_xxx.md
├── jinjiang/
│   └── ch_xxx.md
├── webnovel/
│   └── ch_xxx.md
└── short/
    └── ch_xxx.md
```

## 各平台核心差异

### 番茄（爆款核心）

- 开头3秒必须抓人
- 每300字一个冲突
- 短句为主
- 情绪爆发
- 结尾强悬念

### 起点（长线运营）

- 世界观铺垫
- 逻辑完整
- 节奏中慢
- 延迟满足
- 长期钩子

### 晋江（情绪向）

- 情绪细腻
- 人物关系
- 心理描写丰富
- 暧昧推进
- 细腻冲突

### Webnovel（国际化）

- 英文友好表达
- 简洁直接
- 文化障碍消除
- 信息清晰

### 短内容（病毒传播）

- 极度压缩
- 3秒钩子
- 情绪峰值
- 适合短视频改编

## 驱动下游

- 分发 Agent
- 爆款优化 Agent
- 标题生成 Agent
- 推荐策略 Agent