## STORY 1: Lost Socks 🧦 (Pair matching)

You have socks lying on the bed with different sizes (numbers).
You want to find two socks whose sizes add up to exactly K.

What do you do?

You sort them by size

Put one finger on the smallest

Put one finger on the largest

Now:

If the sum is too small → move the small finger forward

If the sum is too big → move the big finger backward

You don’t recheck everything.
You move with intention.

That’s two pointers.

---

## STORY 2: Elevator Weight Limit 🛗

People are standing in a line with weights (sorted).

You want to check:

“Can any two people ride together without exceeding the limit?”

You try:

Lightest person

Heaviest person

Too heavy?
→ Replace the heaviest.

Too light?
→ Replace the lightest.

You never try random pairs.

---

## STORY 3: Book Shelf Cleanup 📚

Books are arranged by thickness.

You want to remove books from both ends so the total thickness becomes ≤ K.

You:

Look at the leftmost (thin)

Look at the rightmost (thick)

Depending on excess:

Remove from the side that hurts more

Two ends. Two decisions.

---

## STORY 4: Dating App Matches ❤️

Profiles are sorted by age.

You want to find pairs with age difference ≤ D.

One pointer:

younger person

Other pointer:

older person

If difference too big → move older back
If difference acceptable → record & move forward

You slide relative to each other.

---

## STORY 5: Boat Rescue Problem 🚤

People have weights.
A boat can carry at most 2 people under limit W.

Strategy:

Pair lightest + heaviest

If they fit → send them

If not → send heaviest alone

Two ends. Smart elimination.
