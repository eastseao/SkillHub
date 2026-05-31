---
name: 01-world-builder
description: |
  生成适用于长篇网络小说的完整世界观系统，
  包含地理、历史、文明、政治、宗教、经济、
  势力、禁区、时间线与基础规则。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - 小说题材
  - 世界类型
  - 故事风格
  - 文明等级
  - 核心冲突
  - 是否存在超凡力量

output:
  - /world/world_overview.md
  - /world/geography.md
  - /world/history.md
  - /world/civilization.md
  - /world/religion.md
  - /world/politics.md
  - /world/economy.md
  - /world/technology.md
  - /world/forbidden_rules.md
  - /world/glossary.md

rules:
  - 世界规则必须自洽
  - 时间线不得冲突
  - 文明等级必须统一
  - 禁止出现逻辑矛盾
  - 所有势力必须有动机
  - 历史事件必须影响当前世界
  - 地理与文明必须互相关联
  - 必须保留未解之谜
  - 必须支持1000章以上扩展

workflow:
  1. 生成世界基础规则
  2. 生成地理结构
  3. 生成文明体系
  4. 生成历史时间线
  5. 生成政治与宗教
  6. 生成经济与科技
  7. 生成禁忌规则
  8. 输出术语表