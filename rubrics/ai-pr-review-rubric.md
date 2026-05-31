# AI PR Review Rubric

## Score: 1-5 (1=Critical, 5=Excellent)

### Correctness (weight: 30%)
| Score | Criteria |
|-------|----------|
| 1 | Logic errors, crashes, data loss |
| 2 | Edge cases missed, inconsistent behavior |
| 3 | Core logic correct, minor edge case gaps |
| 4 | All cases handled, minor style issues |
| 5 | Bulletproof logic, comprehensive error handling |

### Test Quality (weight: 25%)
| Score | Criteria |
|-------|----------|
| 1 | No tests or tests don't run |
| 2 | Tests pass but miss important cases |
| 3 | Good coverage of happy path |
| 4 | Comprehensive including edge cases |
| 5 | Property-based tests, mutation testing |

### Security (weight: 20%)
| Score | Criteria |
|-------|----------|
| 1 | Vulnerabilities introduced |
| 2 | Missing validation in some paths |
| 3 | Basic security measures present |
| 4 | Defense in depth, input validated |
| 5 | Threat model considered, security tested |

### Performance (weight: 15%)
| Score | Criteria |
|-------|----------|
| 1 | Significant performance regression |
| 2 | Minor inefficiencies |
| 3 | Acceptable performance |
| 4 | Optimized with benchmarks |
| 5 | Measured improvement with data |

### Maintainability (weight: 10%)
| Score | Criteria |
|-------|----------|
| 1 | Unreadable, deeply nested |
| 2 | Inconsistent style |
| 3 | Clear and follows conventions |
| 4 | Well-structured, documented |
| 5 | Exemplary, could be reference code |
