# 多Agent协调案例

## 场景：同时生成Arc 1结尾3章

## 并行执行策略

```
Agent池：
  - Agent_A: 07_chapter_engine
  - Agent_B: 08_memory_manager
  - Agent_C: 11_quality_control

DAG:
  Chapter 48 [07] ──┐
                    ├──→ QC聚合 ──→ Chapter 50
  Chapter 49 [07] ──┤
                    │
  Chapter 47 [07] ──┘

同一时刻：
  Agent_A: 生成 Chapter 47, 48, 49（串行）
  Agent_B: 实时同步记忆状态
  Agent_C: 等待Chapter 47完成后QC（与07并行）
```

## 协调冲突

```
冲突：Chapter 47 QC失败需要回滚
处理：
  1. Agent_C 报告 QC FAIL
  2. Agent_A 暂停 Chapter 48, 49
  3. Agent_A 回滚重写 Chapter 47
  4. Agent_B 保持 Chapter 47 之前状态
  5. Agent_C 重新QC Chapter 47
  6. PASS → 继续 Chapter 48, 49
```

## 优先级解决

```
Agent_B（记忆）优先级 > Agent_A（写作）
Agent_C（QC）优先级 > Agent_A（写作）

当冲突时：
  - QC结果优先
  - 记忆同步优先
  - 写作服从调度