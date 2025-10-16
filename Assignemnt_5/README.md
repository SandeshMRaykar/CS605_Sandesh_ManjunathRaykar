 CSCI 605 - Assignment_5: Implementing a Binary Search Tree (BST)
 Goal of this assignment is to implement a Binary Search Tree (BST) data structure where each node stores a key-value pair. The BST acts as a phone book, using a name (string) as the key and a phone number (number) as the value. The BST node content is maintained by comparing names lexicographically (alphabetically).

The implementation includes BST functionalities: insertion, searching, deletion and in-order traversal. 

1.  Prerequisites: You need a working Python interpreter (version 3.x is recommended).
2.  File Name: The source code should be saved as a single Python file (e.g. BST.py).
3.  Execution: To run the file and execute the included example usage and test cases, use the following command in your terminal:

    bash
    python BST.py
    
The solution is contained within two main classes: TreeNode and BinarySearchTree.

TreeNode Class :
Represents a single node in the tree.

Node contents and discription :
key : Stores the name (string) 
value : Stores the phone number (number)
left : Reference to the left child node
right : Reference to the right child node

BinarySearchTree
Manages the tree structure 

Methods : 
__init__: Initializes the tree with an empty root
insert(name, phone_number): Inserts a new contact into the correct position based on the name's lexicographical order
search(name) :  Returns the phone number associated with the given name (key). Returns None if the name is not found
inorder_traversal() : Performs an in-order traversal of the tree and prints all contact names and phone numbers in alphabetically sorted order
delete(name) : Removes the node associated with the given name. Handles all three deletion cases: no children, one child, and two children
Returns True if deletion was successful, False otherwise. 

Example :

The following sequence demonstrates how to initialize the tree and use the primary methods:
python
1. Initialize the tree
bst = BinarySearchTree()

2. Insert new records
bst.insert("Alice", "555-1234")
bst.insert("Bob", "555-2345")
bst.insert("Charlie", "555-3456")
bst.insert("David", "555-4567")

3. Search for phone numbers
print(bst.search("Alice"))     # Output: 555-1234 
print(bst.search("Frank"))     # Output: None (Name not found)

4. In-Order Traversal 
bst.inorder_traversal()
 Output:
Alice: 555-1234 
Bob: 555-2345
Charlie: 555-3456 
David: 555-4567

5. Delete a node 
print(bst.delete("Frank"))  # Output: False
print(bst.search("Charlie"))  # Output: True
