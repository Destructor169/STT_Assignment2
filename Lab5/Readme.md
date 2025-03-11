# Lab 5: Code Coverage Analysis and Test Generation

## 1. Introduction
- **Repository**: keon/algorithms
- **Commit Hash**: cad4754bc71742c2d6fcbd3b92ae74834d359844
- **Tools Used**: pytest, pytest-cov, pynguin

## 2. Test Suite A Analysis
- **Overall Coverage**: 70%
- **Files with Low Coverage**: Generated tests focused on these modules:
  - algorithms.arrays.delete_nth
  - algorithms.dp.longest_common_subsequence
  - algorithms.graph.dijkstra
  - algorithms.tree.path_sum

## 3. Test Suite B Generation Process
- Used Pynguin with DYNAMOSA algorithm
- Modified generated tests to fix import issues and assertions
- Focused on covering specific low-coverage modules


- Complex data structures remain difficult to test automatically
- Exception handling code is often missed
- Generated tests focus on simple input/output relationships

## 6. Conclusion and Recommendations

### Effectiveness of Automated Test Generation

- **Coverage Achievement**:
  - Successfully generated tests for previously uncovered modules
  - Achieved 100% coverage for simple algorithmic functions
  - Overall coverage (23.11%) significantly lower than manual tests (70.06%)

- **Strengths**:
  - Effective for straightforward algorithms with clear inputs/outputs
  - Excellent for covering utility functions and simple operations
  - Generated tests for multiple modules in minutes

- **Limitations**:
  - Poor handling of complex data structures (trees, graphs)
  - Limited understanding of algorithm semantics
  - Required manual modification to fix imports and test structure

### Recommendations

1. **Hybrid Testing Approach**:
   - Use automated generation for initial coverage of simple functions
   - Apply manual testing for complex algorithms and data structures
   - Focus human testing effort on edge cases and error conditions

2. **Tool Improvements**:
   - Better support for complex object generation
   - Improved handling of dependencies
   - More intelligent edge case detection

3. **Best Practices for Testing**:
   - Design code with testability in mind (dependency injection, etc.)
   - Provide type hints to help automated tools
   - Create specialized test fixtures for complex data structures

This lab demonstrated that while automated test generation tools have value, they work best as a complement to traditional testing approaches rather than a replacement.

## 7. Visualizations

```
Coverage Comparison: Original vs Generated Tests

Test Suite A: ██████████████████████████████████████████████████████████████████████████ 70.06%
Test Suite B: ████████████████████████ 23.11%

Module Coverage (Generated Tests):
delete_nth.py:          ████████████████████████████████████████████████████████████████ 100%
longest_common_seq.py:  ████████████████████████████████████████████████████████████████ 100%
dijkstra.py:            ██████████████ 23.08%
path_sum.py:            ███████████████ 25.71%
n_sum.py:               █ 1.56%
```

*Figure 1: Text-based visualization of coverage metrics*

