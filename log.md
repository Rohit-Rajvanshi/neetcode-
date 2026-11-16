# Pattern log

One entry per problem, grouped by NeetCode topic. Written with `/log` right after solving.

## Arrays

### Max Consecutive Ones — 2026-11-15
- **Pattern:** single pass with a running counter (reset on break)
- **Key insight:** Simple problem: keep a running count of 1s, reset it on a 0, and track the best with `max()`. Using `max()` keeps the code less verbose.
- **Tripped me up:** Nothing.
- **Complexity:** O(n) time, O(1) space
- **How:** alone
- **File:** `problems/course/max_consecutive_ones.py`

### Replace Elements with Greatest Element on Right Side — 2026-11-15
- **Pattern:** reverse traversal with a running max (suffix max)
- **Key insight:** Start from the right side. Keep a running max of everything to the right, write it into the current slot, then update the max with the original value.
- **Tripped me up:** Wouldn't have thought to go right-to-left without the hint (it would have taken hours). Even after that, hit many problems getting the implementation right. Doesn't count it as solving it on my own.
- **Complexity:** O(n) time, O(1) space (in place)
- **How:** watched solution (hint was close to full pseudocode)
- **File:** `problems/course/replace_elements.py`

### Concatenation of Array — 2026-11-16
- **Pattern:** building a dynamic array (append in a loop)
- **Key insight:** It's about the time complexity. Each `append` is amortized O(1), and passing over the array twice is 2n, but we drop the constant 2, so it's O(n). Big-O tracks how the cost grows as n grows, not the exact count of operations.
- **Tripped me up:** Nothing.
- **Complexity:** O(n) time, O(n) space (the 2n output)
- **How:** alone
- **File:** `problems/course/concatenation_of_array.py`

## Two Pointers

### Remove Element — 2026-11-15
- **Pattern:** two pointers (read/write, in-place)
- **Key insight:** Use a read pointer to scan and a write pointer (`idx`) to overwrite the front of the array with elements that aren't `val`. `idx` ends up as the new length. First time seeing the two-pointer method.
- **Tripped me up:** First attempt called `.remove()` on the list while iterating over it, which shifted elements mid-loop and caused bugs. Second attempt iterated over a copy (`nums[:]`), which fixed it but was O(n²) time with extra memory (`.remove()` is O(n), and the copy costs O(n) space).
- **Complexity:** O(n) time, O(1) space
- **How:** hint (two hints: `[:]` copy, then two pointers)
- **File:** `problems/course/remove_element.py`
