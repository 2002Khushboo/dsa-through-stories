## Pattern Used: RESET (not sliding window)

Kadane is NOT sliding window.

Why?

- We are not maintaining a rule
- We are not shrinking gradually

Instead:
- We **reset completely** when the sum becomes negative

### Rule:
> If current sum < 0, drop it entirely.

This is a **greedy decision**:
we locally choose the best option at each step.
