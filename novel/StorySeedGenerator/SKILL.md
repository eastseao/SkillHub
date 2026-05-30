---
name: StorySeedGenerator
version: 1.0
author: Gervas
description: >
  随机小说大纲生成器：根据题材文件随机生成小说故事大纲。
  输入题材列表（txt 或 markdown），随机抽取主角、金手指、世界观、冲突、反派和结局，
  组合输出完整故事大纲，支持短篇（~1000字）、中篇（~3000字）、长篇（~8000字）三种模式。
  触发词：「生成小说大纲」「随机故事」「给我一个故事创意」「小说种子」「故事生成器」「换个故事」
---

# StorySeedGenerator — 随机小说大纲生成器

## 快速开始

1. 用户提供题材文件（可选，txt 或 markdown，每行一个题材），或直接指定题材
2. 选择模式：`random`（纯随机）、`weighted_random`（加权随机）、`hybrid`（混合）
3. 选择篇幅：`short`（短篇）、`medium`（中篇）、`long`（长篇）
4. 依次调用各生成器模块，组合输出完整大纲

## 模式说明

| 模式 | 说明 |
|------|------|
| `random` | 所有元素等概率抽取 |
| `weighted_random` | 热门元素加权，爆款优先 |
| `hybrid` | 主角/金手指用加权，其他随机 |

## 篇幅字数参考

- `short`：~1000 字（五幕简化版）
- `medium`：~3000 字（五幕完整展开）
- `long`：~8000 字（五幕详细 + 爽点设计 + 伏笔体系）

## 工作流

### Step 1：加载题材文件（可选）

读取用户提供的题材文件，每行为一个题材关键词。

### Step 2：生成各元素

按顺序调用以下生成器：

| 生成器 | 读取文件 | 说明 |
|--------|----------|------|
| 主角 | `generators/protagonist.md` | 6大类·30+ 模板 |
| 金手指 | `generators/golden_finger.md` | 14种系统 |
| 世界观 | `generators/world.md` | 13种世界观 |
| 核心冲突 | `generators/conflict.md` | 11种主线冲突 |
| 最终反派 | `generators/villain.md` | 10种反派类型 |
| 终局目标 | `generators/ending.md` | 10种结局走向 |

### Step 3：组合大纲

调用 `generators/plot_engine.md` 中的模板引擎，将各元素组合成故事大纲。

### Step 4：格式化输出

应用 `templates/outline_template.md` 模板，输出结构化 Markdown 大纲。

## Generator 文件格式

每个 generator 文件结构：

```yaml
---
name: xxx_generator
description: xxx
inputs: []      # 或 [param1, param2]
outputs:
  - name: xxx
    type: string
---
# 数据内容（每行一个候选项）
```

## 自定义题材池

用户可提供 `genre_file.txt`，每行一个题材关键词，格式示例：

```
都市
玄幻
科幻
悬疑
历史
武侠
```

提供题材文件时，从文件中读取；未提供时使用内置默认题材。

## 输出质量要求

- 五幕结构完整（第一幕获得力量 → 第五幕最终决战）
- 各元素之间有逻辑关联，避免元素冲突
- 结局与前面伏笔呼应
- 字数符合所选篇幅要求
