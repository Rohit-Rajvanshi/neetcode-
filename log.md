# Pattern log

One entry per problem, grouped by NeetCode topic. Written with `/log` right after solving.

## Arrays & Hashing

### Max Consecutive Ones — 2026-11-15
- **Pattern:** single pass with a running counter (reset on break)
- **Key insight:** Simple problem: keep a running count of 1s, reset it on a 0, and track the best with `max()`. Using `max()` keeps the code less verbose.
- **Tripped me up:** Nothing.
- **Complexity:** O(n) time, O(1) space
- **How:** alone
- **File:** `problems/course/max_consecutive_ones.py`
