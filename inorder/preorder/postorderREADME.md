# Binary-tree
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
}

// left root right 
public void Inorder(Node node){
    if(node == 0){
        return;
    }
    Inorder(node.left);
    System.out.println(node.data: +" ");
    Inorder(node.right);
}

// root left right 
public void Preorder(Node node){
    if(node == 0){
        return;
    }
    System.out.println(node.data: +" ");
    Preorder(node.left);
    Preorder(node.right);
}

// left right root
public void Postorder(Node node){
    if(node == 0){
        return;
    }
    Postorder(node.left);
    Postorder(node.right);
    System.out.println(node.data: +" ");
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
      
    }
}
