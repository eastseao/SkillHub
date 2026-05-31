---
name: 11-quality-control
description: |
  对小说章节、Arc、整体剧情进行质量检测，
  包括剧情一致性、人物一致性、力量体系平衡、
  节奏质量、情绪质量、风格一致性、爽点密度、
  水文检测与最终发布审核。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit

input:
  - chapter_output
  - arc_output
  - memory_system
  - style_system
  - platform_adapter

output:
  - /qc/report.md
  - /qc/scorecard.md
  - /qc/issues.md
  - /qc/fix_suggestions.md

rules:
  - 必须检测所有核心维度
  - 必须给出评分
  - 必须标记问题等级
  - 必须提供修复建议
  - 必须支持回滚机制
  - 禁止主观评价
  - 必须结构化输出
  - 必须支持1000+章节系统
  - 必须服务工业写作系统
  - 必须可自动化执行

workflow:
  1. 解析输入内容
  2. 多维度质量检测
  3. 生成评分系统
  4. 生成问题列表
  5. 生成修复建议
  6. 判断是否通过发布
  7. 输出QC报告