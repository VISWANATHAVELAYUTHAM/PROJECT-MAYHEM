class Solution {
    public int findCoverage(int[][] matrix) {
        // code here
        int n= matrix.length;
        int m= matrix[0].length;
        int count=0;
        for(int i=0;i<matrix.length;i++){
            for(int j=0;j<matrix[0].length;j++){
                if(matrix[i][j]==0){
                    if(j+1<m && matrix[i][j+1]==1) count++;
                    if(j-1>=0 && matrix[i][j-1]==1) count++;
                    if(i-1>=0 && matrix[i-1][j]==1) count++;
                    if(i+1<n && matrix[i+1][j]==1) count++;
                } 
            }
        }
        return count;
    }
}
