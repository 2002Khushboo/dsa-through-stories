## Edge Case
What if profits could be negative, and K is small?

Does sliding window always work?

## Instinct
“My task is maximum length, irrespective of profits.
I just need profit ≤ K, negatives are fine.”

That sounds reasonable on paper.

And if all numbers were non-negative, you’d be 100% right.

But negatives quietly destroy one key assumption.

## Hidden Assumption
Sliding window works only if this is true:

When I expand the window, the condition becomes worse

When I shrink the window, the condition becomes better

This must be monotonic.

## Example
One small counterexample 

Profits: [5, -10, 5]
K = 3

Try sliding window thinking

Start expanding:

[5] → sum = 5 ❌ (>3) → shrink
(window becomes empty)

[-10] → sum = -10 ✅

[-10, 5] → sum = -5 ✅
length = 2 (good)

So sliding window finds length = 2

But what is the correct answer?

The full window: [5, -10, 5]
Sum = 0 ≤ 3
Length = 3

👉 Longer window exists, but sliding window never considers it

## WHY sliding window failed (this is the core insight)

Because with negative numbers:

Expanding the window can improve the condition

Shrinking the window can make it worse

So this logic breaks:

“If sum > K, remove from left and we’re safe”

You might remove a positive that was needed to offset a future negative.

## Key takeaway (memorize this rule)
✅ Sliding Window works when:

All numbers are non-negative

Or the condition behaves monotonically

❌ Sliding Window fails when:

Negative numbers are allowed

And the condition depends on sum / balance

## What pattern works instead?

This becomes a Prefix Sum + Hashing or Binary Search on Prefix Sums problem.

Why?

Prefix sums remember past states

You don’t throw away information too early
