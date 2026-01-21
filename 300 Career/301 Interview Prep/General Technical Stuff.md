## [[Time Complexity]]

- O(n) + O(n) = O(2n) = O(n)
- Helper calls like `isAlphaNumeric` and `toLowerCase` are constant time per character.

## [[Space Complexity]]

- O(n) + O(n) = O(2n) = O(n)
- If the input is restricted to a fixed alphabet (e.g., lowercase English letters only), the **space complexity becomes O(1)**, since the maps can never exceed a constant size.