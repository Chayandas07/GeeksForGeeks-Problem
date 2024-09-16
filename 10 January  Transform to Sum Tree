class Solution {
  public:
  
    // Convert a given tree to a tree where every node contains sum of values of
    // nodes in left and right subtrees in the original tree
   int check(Node* root){
      if(root==NULL){
          return 0;
      }
      int left=check(root->left);
      int right=check(root->right);
     int x= root->data;
     root->data=left+right;
     return root->data+x;
    
      
  }
    void toSumTree(Node *node)
    {
        check(node);   // Your code here
    }
};
