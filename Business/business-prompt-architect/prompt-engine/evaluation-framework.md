# Prompt Evaluation Framework

## Evaluation Dimensions

### 1. Task Completion
- Does it answer the question?
- Are all required elements present?
- Is the output format correct?
- Are there gaps or omissions?

### 2. Accuracy
- Are facts correct?
- Are sources cited?
- Is reasoning sound?
- Are calculations accurate?

### 3. Relevance
- Does it address the actual question?
- Is context properly applied?
- Are examples appropriate?
- Is the level of detail appropriate?

### 4. Coherence
- Logical flow of ideas
- Clear structure
- Consistent terminology
- Smooth transitions

### 5. Helpfulness
- Actionable insights
- Practical recommendations
- Clear explanations
- Appropriate tone

## Evaluation Methods

### Human Evaluation
- Expert review
- User feedback
- A/B testing
- Rubric scoring

### Automated Evaluation
- Exact match
- Semantic similarity
- BLEU/ROUGE scores
- Custom metrics

## Scoring Template

| Dimension | Weight | Score (1-5) | Notes |
|-----------|--------|-------------|-------|
| Task Completion | 30% | | |
| Accuracy | 30% | | |
| Relevance | 20% | | |
| Coherence | 10% | | |
| Helpfulness | 10% | | |
| **Weighted Total** | 100% | | |

## Test Case Development
- Cover edge cases
- Include ambiguous inputs
- Test for common failure modes
- Include gold standard outputs
