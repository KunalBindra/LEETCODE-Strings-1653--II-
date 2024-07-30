# LEETCODE-Strings-1653--II-
**Explanation:**

1. **Initialization:**
   - `n`: Stores the length of the input string `s`.
   - `count`: Keeps track of the number of deletions.
   - `st`: A stack to store characters of the string.

2. **Iterating through the string:**
   - For each character `c` in the string:
     - If the stack is not empty and the current character is 'a' and the top of the stack is 'b', it means we can eliminate an 'a' and a 'b' pair.
       - Pop the 'b' from the stack.
       - Increment the `count` of deletions.
     - Otherwise, push the current character onto the stack.

3. **Return the count:**
   - After processing the entire string, return the `count` of deletions.

**Dry Run:**

Let's take an example string: `s = "aabab"`

- **Iteration 1:**
  - `i = 0`, `c = 'a'`.
  - Stack: `[a]`
  - `count` remains 0.

- **Iteration 2:**
  - `i = 1`, `c = 'a'`.
  - Stack: `[a, a]`
  - `count` remains 0.

- **Iteration 3:**
  - `i = 2`, `c = 'b'`.
  - Stack: `[a, a, b]`
  - `count` remains 0.

- **Iteration 4:**
  - `i = 3`, `c = 'a'`.
  - Stack: `[a, a]` (Pop 'b')
  - `count` becomes 1.

- **Iteration 5:**
  - `i = 4`, `c = 'b'`.
  - Stack: `[a, a, b]`
  - `count` remains 1.

**Final `count` is 1.**

This means we need to delete one character (the 'b' at index 3) to make the string either "aaaa" or "bbbb".

**Time Complexity:** O(n)
**Space Complexity:** O(n)

