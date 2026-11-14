---
description: Log a solved problem to log.md and schedule re-solves in review.md
argument-hint: <problem file or name> [notes]
---

Rohit just solved: $ARGUMENTS

1. Find and read the solution file in `problems/` (match the name if he didn't give a path). Don't edit it.
2. Ask him ONE short question if his notes didn't already cover it:
   "In your words: what was the key insight, and what tripped you up?"
   Also ask how he solved it if unclear: **alone**, **with a hint**, or **watched the solution**.
   Wait for his answer before writing anything.
3. Work out the time and space complexity from his code. If his code has a bug or misses an edge case, tell him in chat; don't fix it.
4. Append to `log.md` under the right topic heading (create the heading if missing), in this format:

   ### <Problem name> — <date YYYY-MM-DD>
   - **Pattern:** <e.g. sliding window>
   - **Key insight:** <his words, lightly cleaned up>
   - **Tripped me up:** <his words>
   - **Complexity:** O(?) time, O(?) space
   - **How:** alone / hint / watched solution
   - **File:** `problems/<topic>/<slug>.py`

5. Add a row to the table in `review.md`. Get today's date with `date +%F`. First due date:
   - watched solution → today + 1 day
   - with a hint → today + 3 days
   - alone → today + 3 days
   Set Interval to that number of days and Status to `due`.
6. Commit: `git add -A && git commit -m "log: <problem name>"`. Don't push unless he asks.
7. Reply in 2–3 lines: the pattern, when it's next due, and nothing else.
