class Solution {
    void help(int[][] matrix,int n,int i,int j,ArrayList<String> ans,String temp){
        if(i<0 || j<0||i==n ||j==n|| matrix[i][j]==0)return;
        if(i==n-1 && j==n-1){
            ans.add(temp);
            return;
        }
        matrix[i][j]=0;
        help(matrix,n,i+1,j,ans,temp+'D');
        help(matrix,n,i-1,j,ans,temp+'U');
        help(matrix,n,i,j+1,ans,temp+'R');
        help(matrix,n,i,j-1,ans,temp+'L');
        matrix[i][j]=1;
    }
    public ArrayList<String> findPath(int[][] mat) {
        // Your code here
        ArrayList<String> ans = new ArrayList<>();
            help(mat,mat.length,0,0,ans,"");
            return ans;
        
    }
}
