# LeetCode 104 — Maximum Depth of Binary Tree

## Problem
Given the `root` of a binary tree, return its maximum depth.

The maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

---

## Example

Input:
```text
root = [3,9,20,null,null,15,7]
```

Output:
```text
3
```

---

## Approach
Use recursion (DFS):

- If the node is `null`, return `0`
- Recursively calculate left and right subtree depths
- Return:
```text
1 + max(leftDepth, rightDepth)
```

---

## Java Solution

```java
class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) {
            return 0;
        }

        int left = maxDepth(root.left);
        int right = maxDepth(root.right);

        return 1 + Math.max(left, right);
    }
}
```

---

## Time Complexity
```text
O(n)
```

## Space Complexity
```text
O(h)
```

- `n` = number of nodes
- `h` = height of tree

---

## Key Concepts
- Binary Tree
- DFS
- Recursion
