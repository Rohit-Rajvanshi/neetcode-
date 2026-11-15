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

### Remove Element — 2026-11-15
- **Pattern:** two pointers (read/write, in-place)
- **Key insight:** Use a read pointer to scan and a write pointer (`idx`) to overwrite the front of the array with elements that aren't `val`. `idx` ends up as the new length. First time seeing the two-pointer method.
- **Tripped me up:** First attempt called `.remove()` on the list while iterating over it, which shifted elements mid-loop and caused bugs. Second attempt iterated over a copy (`nums[:]`), which fixed it but was O(n²) time with extra memory (`.remove()` is O(n), and the copy costs O(n) space).
- **Complexity:** O(n) time, O(1) space
- **How:** hint (two hints: `[:]` copy, then two pointers)
- **File:** `problems/course/remove_element.py`
