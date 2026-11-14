---
description: Show re-solves due today and update the queue after each attempt
---

1. Get today's date with `date +%F`. Read `review.md`.
2. List every row with Status `due` and a Due date on or before today, oldest first. Show only the problem name and pattern. **Don't show any code or the log entry.**
3. Rohit re-solves each one from scratch in `scratch/<slug>.py` (create `scratch/` if missing; it's git-ignored). He tells you **pass** or **fail** for each.
   - If he asks, you may check his scratch solution against the problem; still no full solutions.
4. Update that row:
   - **pass** → next interval = 3 → 14 → 30 → `done` (move up one step). Set Due = today + new interval. After passing at 30, set Status to `done`.
   - **fail** → Interval = 3, Due = today + 3. Add one line to that problem's entry in `log.md`: `- Re-solve failed <date>: <what he forgot, in his words>`.
5. When the queue for today is empty, say so in one line and tell him he can move on to new problems.
6. Commit: `git add -A && git commit -m "review: <date>"`.

If nothing is due, say "Nothing due today" and stop.
