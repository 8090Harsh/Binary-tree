# Binary-tree
public class BinaryTreeApp {
// create the root node 
class Node {
    int data;
    Node left;
    Node right;
}

// insert the new node in tree 
// best case ..

class BinaryTree {
    public Node createNewNode(int k){
        Node value = new Node();
        value.data = k;
        value.left = null;
        value.right = null;
        return value;
    }
public void Inorder(Node node){
    if(node == null){
        return;
    }
    Inorder(node.left); 
    System.out.println(node.data  + " ");
    Inorder(node.right);
}


public void Preorder(Node node){
   if(node == null){
        return;
    }
    System.out.println(node.data  + " ");
    Preorder(node.left);
    Preorder(node.right);
}

public void Postorder(Node node){
    if(node == null){
        return;
    }
    Postorder(node.left);
    Postorder(node.right);
    System.out.println(node.data  + " ");
}
public int getSumOfNode(Node node){
    if(node == null){
        return 0;
    }
    return node.data + getSumOfNode(node.left) + getSumOfNode(node.right);
}
// diff.. of value of even and odd level

public int getDiffenceEvenOddValue(Node node){
if(Node == null) {
return 0;
}
return node.data-getDiffenceEvenOddValue(node.left)-getDiffenceEvenOddValue(node.right);
}

// find leaf node 

public int getNumOfLeafNode(Node node){
if(node == null ){
return 0;
}
if(node.leaf == null && node.right == null ){
return 1;
}
return getNumOfLeafNode(node.leaf) + getNumOfLeafNode(node.right);
}


//Print elements at given level in Binary Tree

public int PrintAtGivenLevel(Node node , int level)
{
if(node == null){
return -1;
}
if(level == 1)
{
System.out.println(node.data+ " ");
return;
}
PrintAtGivenLevel(node.left , level-1);
PrintAtGivenLevel(node.right , level-1);
}
}

    public class BinaryTreeApp {
   
    public static void main(String[] args){
      BinaryTree a = new BinaryTree();
      Node root = a.createNewNode(2);
      root.left = a.createNewNode(7);
      root.right = a.createNewNode(5);
      root.left.left = a.createNewNode(2);
      root.left.right = a.createNewNode(6);
      root.left.right.left = a.createNewNode(5);
      root.left.right.right = a.createNewNode(11);
      root.right.right = a.createNewNode(9); 
       root.right.right.left = a.createNewNode(4);
       System.out.println("Inorder : ");
       a.Inorder(root);
        System.out.println();
        
        System.out.println("Preorder : ");
       a.Preorder(root);
        System.out.println();
       
       
       System.out.println("Postorder : ");
       a.Postorder(root);
      
      System.out.println("Sum of nodes : " + getSumOfNode(root));

System.out.println("Sum of nodes : " + a.getDiffenceEvenOddValue(root));


System.out.println("a.getNumOfLeafNod(root));

a.PrintAtGivenLevel(root,2);
      
    }
}
