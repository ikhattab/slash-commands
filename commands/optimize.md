---
id: optimize
name: Optimize Performance
slug: optimize
category: code-quality
description: Find and fix performance bottlenecks.
---

# Optimize Performance

Analyze the selected code for performance issues and optimize:

Look for:

- Unnecessary re-renders or recomputations
- N+1 queries or redundant API calls
- Memory leaks or excessive memory usage
- Inefficient algorithms (O(n²) when O(n) is possible)
- Blocking operations that could be async

For each issue found:

1. Explain why it's a performance problem
2. Show the optimized solution
3. Estimate the performance improvement

Only suggest changes that provide meaningful improvements.
