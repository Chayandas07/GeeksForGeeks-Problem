class Solution {
    int cs = 0;
  public:
    void transformTree(Node *root) {
        if(!root)return;
        int d = root->data;
        transformTree(root->right);
        root->data = cs;
        cs += d;
        transformTree(root->left);
    }
};
