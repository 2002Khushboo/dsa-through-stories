## Pseudocode

```
    set current_sum = first element
    set max_sum = first element
    for each next element:
        current_sum = max(element, current_sum + element)
        max_sum = max(max_sum, current_sum)
    return max_sum
```
