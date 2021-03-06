# Binary-tree
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

// Get Height of a Binary Tree/Node

public int getHeightOfTree(Node node){
if(node == 0){
return -1;
}
return max(getHeightOfTree(node.left) , getHeightOfTree(node.right))+1;
}


// Print elements in Level order (Using Recursion)

public void LevelorderTraversalUsingRec(Node node){
if(node == null){
return;
}
int height = gatHeightOfTree(node);
for(int i=0; i<=height; i++){
PrintAtGivenLevel(node , i+1);
System.out.println();

}

// Level Order traversal without Recursion (Using Queue)

public void LevelOrdertraversalUsingQueue(Node node){
if(node == null){
return;
}
Queue<Node> q = new LinkedList<Node>();
q.add(node);
while(q.size()>null) {
Node top = q.remove();
System.out.println(top.data + " ");
if(top.left! = null) {
q.add(top.left);
}
if(top.right! = null) {
q.add(top.right);
}

//Print Reverse Level order Traversal (Using Recursion)
public void ReverseLevelOrderTraversal(Node node) {
if(node == null ) {
return;
}
int height = getHeightOfTree(node);
for(i=height; i>=0; i--){
PrintAtGivenLevel(node , i+1);
System.out.println();
}

// Reverse Level Order Traversal without using recursion

public void ReverseLevelOrderTraversalwithoutusingrecursion(Node node){
if(node == null) {
return;
}
Queue<Node> q = new LinkedList<Node();
q.add(node);
stack<Node> s= new stack<Node>();
while(q.size()>0) {
Node t = q.remove();
if(t.right! = null) ;
q.add(t.right);
}
if(t.left! = null) ;
q.add(t.left);
}
s.push(t);
}
while(s.size()>0){
System.out.println(s.pop().data + " ");
}
}

//Level Order Traversal Line by Line Without Recursion (Using Single Queue) 

punlic void LevelOrderTraversalLinebyLineWithoutRecursionUsingSingleQueue(Node node)
{
if(node == null){
return;
}
Queue<Node> q = new LinkedList<Node>();
q.add(node);
while(true){
int count = q.size();
if(count == 0) 
break;
while(count>0){
Node top = q.remove();
system.out.println(top.data + " ");

if(top.left! = null) {
q.add(top.left);
}

if(top.right! = null) {
q.add(top.right);
}
count--;
}
System.out.println();
}
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

System.out.println("Get Height of tree : " + getHeightOfTree(root));

a.LevelorderTraversalUsingRec(root);

a.LevelOrdertraversalUsingQueue(root);

a.ReverseLevelOrderTraversal(root);
a.ReverseLevelOrderTraversalwithoutusingrecursion(root);
a.LevelOrderTraversalLinebyLineWithoutRecursionUsingSingleQueue(root);
    }
}

//output - 2 7 5 2 6 9 5 11 4 

// output(ReverseLevelOrderTraversalwithoutusingrecursion) -- 5 11 9 2 6 9 7 5 2

// output(LevelOrderTraversalLinebyLineWithoutRecursionUsingSingleQueue)
2
7  5
2  2  6
9  5  11
