## The Core Intuition

Sliding Window answers this question:

👉 “Can I fix the problem by removing some earlier elements?”

If YES → shrink gradually  
If NO → reset (not sliding window)

Why not reset here?

Because:
- earlier elements might still be useful
- only the rule is broken, not the whole window
