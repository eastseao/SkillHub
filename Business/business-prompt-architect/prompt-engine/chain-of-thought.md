# Chain-of-Thought Prompting

## Basic Chain-of-Thought

Question: [problem]
Answer: Let's think step by step.
[Step 1: ...]
[Step 2: ...]
[Step 3: ...]
Therefore, [answer]

## Zero-Shot CoT

Q: [problem]
A: Let's think step by step.

## Few-Shot CoT

Include worked examples with explicit reasoning:

Q: [example problem]
A: [detailed reasoning steps leading to answer]

Q: [example problem]
A: [detailed reasoning steps leading to answer]

Q: [actual problem]
A:

## Self-Consistency CoT

1. Generate multiple reasoning paths
2. Sample different Chain-of-Thoughts
3. Select most consistent answer

## Tree of Thought

                    Root
           /        |         \
        Branch A  Branch B  Branch C
           ||        ||         ||
        Thought   Thought    Thought
           ||        ||         ||
        Thought   Thought    Thought
                    |
               Best Path

## When to Use CoT
- Complex reasoning tasks
- Multi-step calculations
- Logical deduction
- Strategic planning
- Problem solving with multiple variables

## CoT Pitfalls
- Overconfidence in flawed reasoning
- Circular logic
- Adding irrelevant steps
- Forgetting the question
