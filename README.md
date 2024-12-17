### GitHub README  

## Problem Description  

Given the root of a binary tree, determine the **lowest common ancestor (LCA)** of two given nodes `p` and `q`. The **LCA** is defined as the lowest node in the binary tree that has both `p` and `q` as descendants, where a node can also be a descendant of itself.  

---  

### Solution Approach  

The solution involves **recursive traversal** to identify the lowest common ancestor by checking subtrees for the presence of the given nodes `p` and `q`.  

---  

### Key Points  

1. **Base Case**:  
   - If the current node is `null` or matches either `p` or `q`, it is a potential candidate for the LCA and is returned directly.  

2. **Recursive Subtree Traversal**:  
   - Traverse both left and right subtrees to search for nodes `p` and `q`.  

3. **Determine LCA**:  
   - If both left and right recursive calls return non-null values, the current node is the LCA.  
   - If only one subtree contains both nodes, propagate that result upward.  

4. **Result Propagation**:  
   - The recursion ultimately bubbles up the LCA to the root level.  

---  

### Time and Space Complexity  

- **Time Complexity**: O(n), where `n` is the total number of nodes in the binary tree. Each node is visited once.  
- **Space Complexity**: O(h), where `h` is the height of the tree, for the recursion stack.  

---  

For a detailed explanation of the code, visit the [description here](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/).  
