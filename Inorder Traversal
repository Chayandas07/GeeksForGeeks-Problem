class Solution {
    private:
    void inorderTraversal(Node* root, vector<int> &ans){
        if(root==nullptr){
            return;
        }
        
        inorderTraversal(root->left, ans);
        ans.push_back(root->data);
        inorderTraversal(root->right, ans);
        
    }
  public:
    // Function to return a list containing the inorder traversal of the tree.
    vector<int> inOrder(Node* root) {
        if(root==nullptr){
            return {};
        }
      vector<int>ans;
      inorderTraversal(root, ans);
      return ans;
    }
};
