Project : Implementation of Binary tree 

import java.util.Scanner;

class Node {
    int data;
    Node left, right;

    Node(int val) {
        data = val;
        left = right = null;
    }
}

class BST {
    Node root;

    BST() {
        root = null;
    }

    Node insert(Node node, int val) {
        if (node == null) {
            return new Node(val);
        }
        if (val < node.data) {
            node.left = insert(node.left, val);
        } else if (val > node.data) {
            node.right = insert(node.right, val);
        }
        return node;
    }

    Node search(Node node, int val) {
        if (node == null || node.data == val) {
            return node;
        }
        if (val < node.data) {
            return search(node.left, val);
        }
        return search(node.right, val);
    }

    Node findMin(Node node) {
        while (node != null && node.left != null) {
            node = node.left;
        }
        return node;
    }

    Node deleteNode(Node root, int val) {
        if (root == null) return root;

        if (val < root.data) {
            root.left = deleteNode(root.left, val);
        } else if (val > root.data) {
            root.right = deleteNode(root.right, val);
        } else {
            if (root.left == null) {
                Node temp = root.right;
                return temp;
            } else if (root.right == null) {
                Node temp = root.left;
                return temp;
            }
            Node temp = findMin(root.right);
            root.data = temp.data;
            root.right = deleteNode(root.right, temp.data);
        }
        return root;
    }

    void inOrder(Node node) {
        if (node == null) return;
        inOrder(node.left);
        System.out.print(node.data + " ");
        inOrder(node.right);
    }

    void preOrder(Node node) {
        if (node == null) return;
        System.out.print(node.data + " ");
        preOrder(node.left);
        preOrder(node.right);
    }

    void postOrder(Node node) {
        if (node == null) return;
        postOrder(node.left);
        postOrder(node.right);
        System.out.print(node.data + " ");
    }
}

public class Nodes{
    public static void main(String[] args) {
        BST tree = new BST();
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the number of elements: ");
        int n = scanner.nextInt();
        System.out.println("The printing array is:");
        int[] values = new int[100];
        for (int i = 0; i < n; i++) {
            values[i] = scanner.nextInt();
        }

        for (int i = 0; i < n; i++) {
            tree.root = tree.insert(tree.root, values[i]);
        }

        System.out.print("InOrder traversal: ");
        tree.inOrder(tree.root);
        System.out.println();

        System.out.print("PreOrder traversal: ");
        tree.preOrder(tree.root);
        System.out.println();

        System.out.print("PostOrder traversal: ");
        tree.postOrder(tree.root);
        System.out.println();

        System.out.print("Enter the number to search: ");
        int s = scanner.nextInt();
        System.out.println("Search: " + (tree.search(tree.root, s) != null ? "Found" : "Not Found"));

        System.out.print("Enter the number to delete: ");
        int d = scanner.nextInt();
        System.out.println("Delete");
        tree.root = tree.deleteNode(tree.root, d);
        System.out.print("InOrder traversal after deletion: ");
        tree.inOrder(tree.root);
        System.out.println();

        scanner.close();
    }
}

Overview:

The project involves implementing a Binary Search Tree (BST) in java. The BST is a fundamental data structure in computer science used for efficient data storage, retrieval, 
and manipulation. The project includes the core functionalities of a BST: insertion, search, and deletion of nodes. Additionally, it includes methods for in-order, pre-order, 
and post-order tree traversals to display the elements in different sequences.
Features and Functionalities:

Node Structure:
Represents each node in the BST.
Contains integer data and pointers to left and right children.

BST Class:
Manages the root of the tree and provides methods for various operations:
Insertion: Adds a new value while maintaining BST properties.
Searching: Finds a value and returns the corresponding node.
Deletion: Removes a node based on three possible cases (no children, one child, two children).
Traversal Methods:
In-Order: Outputs values in ascending order.
Pre-Order: Outputs values in root-first order.
Post-Order: Outputs values in leaf-first order.

Main Class (Nodes):
Handles user input for the number of elements and their values.
Executes operations like insertion, traversal, searching, and deletion based on user input.
