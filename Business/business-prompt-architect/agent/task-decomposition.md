# Task Decomposition

## Decomposition Strategies

### Sequential Decomposition
Breaking into ordered steps:
Task -> Subtask A -> Subtask B -> Subtask C -> Output

### Hierarchical Decomposition
Breaking into nested levels:
Task
├── Component 1
|   ├── Sub-component 1.1
|   └── Sub-component 1.2
└── Component 2
    ├── Sub-component 2.1
    └── Sub-component 2.2

### Parallel Decomposition
Breaking into independent tasks:
Task -> [A || B || C] -> Integration

## When to Decompose

### Signs You Need Decomposition
- Task too complex for single prompt
- Multiple distinct skill sets required
- Steps have dependencies
- Quality degrades with complexity
- Latency unacceptable if sequential

### Signs You Do not Need Decomposition
- Simple, single-step task
- Well-defined and bounded
- No special tooling needed
- Fast execution required

## Decomposition Principles

### Atomic Tasks
Each subtask should be:
- Self-contained
- Clearly scoped
- Testable independently
- Assignable to one agent

### Dependency Management
- Identify which tasks must complete before others start
- Plan for parallel execution where possible
- Handle cross-cutting concerns (context passing)

### Context Passing
- What information does each subtask need?
- What information does each subtask produce?
- Minimize redundant work
- Avoid context window bloat

## Human-in-the-Loop
- Decision checkpoints for high-stakes steps
- Approval gates for irreversible actions
- Quality sampling for validation
- Escalation paths for edge cases
