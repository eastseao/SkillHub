---
name: 12-agent-orchestrator
description: |
  AI小说工业系统的总调度核心，
  负责调度所有Agent（世界观、角色、剧情、章节、记忆、风格、平台、质检），
  控制任务流、依赖关系、执行顺序、质量门禁与系统稳定性，
  确保1000+章节小说工业化持续生成。
version: 1.0.0
author: NovelFactory

tools:
  - read
  - write
  - edit
  - call_agent

input:
  - all_skills
  - generation_request
  - system_state

output:
  - /orchestration/execution_plan.md
  - /orchestration/task_graph.json
  - /orchestration/system_status.md
  - /orchestration/final_output.md

rules:
  - 必须调度所有Agent
  - 必须管理依赖关系
  - 必须控制执行顺序
  - 必须触发质量门禁
  - 必须支持失败回滚
  - 必须支持循环生成
  - 必须防止系统死锁
  - 必须优化生产效率
  - 必须保证1000+章节稳定输出
  - 必须是唯一全局控制器

workflow:
  1. 解析生成目标
  2. 构建任务图（DAG）
  3. 分配Agent职责
  4. 设置执行顺序
  5. 启动生成流程
  6. 监控执行状态
  7. 触发质量控制
  8. 处理异常与回滚
  9. 输出最终结果