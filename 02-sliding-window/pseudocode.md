## Pseudocode
```
left = 0
for right in array:
    add array[right] to window
    while rule is broken:
        remove array[left] from window
        left++
    update best answer
```
## Example in code:
```
int longestSubarray(vector<int> arr, int k) 
{
    int left = 0, sum = 0, maxLen = 0;
    for (int right = 0; right < arr.size; right++) 
    {
        sum += arr[right];
        // Shrink until rule is satisfied
        while (sum > k) 
        {
            sum -= arr[left];
            left++;
        }
        maxLen = max(maxLen, right - left + 1);
    }
    return maxLen;
}
```
