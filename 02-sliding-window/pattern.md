## Pattern: SHRINK GRADUALLY

Sliding Window works like a rubber band:

- Right pointer expands the window
- Left pointer shrinks the window

### Rule:
> When the condition breaks,
> keep removing from the left
> until the condition is satisfied again.

This keeps the window **valid at all times**.
