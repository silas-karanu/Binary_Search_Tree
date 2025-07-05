## Binary Search Tree (BST) - README


This project implements a basic Binary Search Tree (BST) in Python with operations including insertion, searching, deletion, and inorder traversal.

## 📁 Files

`bst.py:` Contains the TreeNode and BinarySearchTree classes and test code.

---
## 📚 Features

- Insert nodes in a binary search manner

- Search for a key in the BST

- Delete a key from the BST

- Inorder traversal to view keys in sorted order

---

## 🛠️ How It Works

Class Definitions

**TreeNode**

Represents a node with a key, left, and right child.

```python
class TreeNode:
    def __init__(self, key):
        self.key = key
        self.left = None
        self.right = None
```

**BinarySearchTree**

Main class that handles all operations.

```Python
class BinarySearchTree:
    def __init__(self):
        self.root = None
```

**Inserting Nodes**
```python
def insert(self, key):
    self.root = self._insert(self.root, key)
```
Recursively finds the correct place to insert the new key.

**Searching for a Key**
```python
def search(self, key):
    return self._search(self.root, key)
```
Recursively traverses the tree to find the key.

**Deleting a Node**
```python
def delete(self, key):
    self.root = self._delete(self.root, key)
```
Handles 3 cases:

- Node with no children

- Node with one child

- Node with two children

**Inorder Traversal**
```python
def inorder_traversal(self):
    result = []
    self._inorder_traversal(self.root, result)
    return result
```
Returns keys in ascending order.

---

## 🚀 Example Usage
```python
bst = BinarySearchTree()
nodes = [50, 30, 20, 40, 70, 60, 80]
for node in nodes:
    bst.insert(node)

print('Search for 80:', bst.search(80))
print('Inorder traversal:', bst.inorder_traversal())
bst.delete(40)
print('Search for 40:', bst.search(40))
```
---

## ✅ Expected Output

Search for 80: <TreeNode object or key>
Inorder traversal: [20, 30, 40, 50, 60, 70, 80]
Search for 40: None

---

## 🧠 To Improve

- Add a visual tree printer

- Implement preorder and postorder traversals

- Convert to a GUI version using tkinter or web framework

---

## 📜 License

This project is licensed under the MIT License. Feel free to use and modify.

---
