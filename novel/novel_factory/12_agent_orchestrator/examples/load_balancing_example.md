# 负载均衡示例

## 场景：同时维护3个Arc的生产

```
系统负载：
  Arc 1: Chapter 200-210（活跃生产）
  Arc 2: Chapter 80-90（活跃生产）
  Arc 3: Chapter 1-10（初期验证）

Agent分配：
  Agent_1: 专责 Arc 1（高速通道）
  Agent_2: 专责 Arc 2（中速通道）
  Agent_3: 专责 Arc 3（低速通道）
  Agent_QC: 共享QC资源池

调度策略：
  - Arc 1 最优先（已验证质量）
  - Arc 2 次优先（新Arc，质量待验证）
  - Arc 3 最低优先级（验证阶段）
  - QC资源优先Arc 2（新人设需要更多检测）
```

## 资源调度

```
高峰期：
  - 3个07_chapter_engine并行
  - 2个QC并行（1个专门Arc 2）
  - 1个08_memory_manager监控全局

低峰期：
  - 1个07_chapter_engine生产
  - 1个QC等待
  - 1个08_memory_manager整理记忆

限流：
  - 单Agent最大并发: 3个章节生成
  - QC队列最大等待: 5分钟
  - 内存同步间隔: 每10章强制同步