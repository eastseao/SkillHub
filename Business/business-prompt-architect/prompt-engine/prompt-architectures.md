# Prompt Architectures

## Standard Prompt Structure

# ROLE
You are [descriptive role definition with expertise areas]

# CONTEXT
[Background information, setting, constraints]

# OBJECTIVE
[What needs to be accomplished]

# INPUT
[The information provided to work with]

# PROCESS
[Step-by-step approach, frameworks to use]

# DELIVERABLE
[Expected output format and content]

# VALIDATION
[Criteria for quality, things to check]

# IMPROVEMENT LOOP
[How to refine if initial output needs improvement]

## Few-Shot Prompting

Provide 1-5 examples of input-output pairs before the actual task:

Example 1:
Input: [example]
Output: [example]

Example 2:
Input: [example]
Output: [example]

Now complete:
Input: [actual input]

## Chain-of-Density Prompting

For information extraction and summarization:
1. Start with a sparse summary
2. Progressively add details
3. Maintain entity density

## Role-Based Prompting

Act as a [specific expertise level] [role]
with [years of experience] in [specific domain]

When I ask about [topic area], respond from this perspective

## Constraint-Based Prompting

You MUST:
- [mandatory requirement 1]
- [mandatory requirement 2]

You MUST NOT:
- [prohibited behavior 1]
- [prohibited behavior 2]

You SHOULD:
- [recommended approach 1]

## Meta-Prompting

Prompts that make the model reflect on its own thinking:
- "Think step by step"
- "Consider alternative approaches"
- "Identify assumptions in your reasoning"
