class Solution {
    ArrayList<ArrayList<Integer>>list;
    int[][] board;
    public ArrayList<ArrayList<Integer>> nQueen(int n) {
        // code here
        list=new ArrayList<>();
        board=new int[n][n];
        solveNQueen(0,n);
        return list;
        
    }
    private boolean isSafe(int row,int col,int N){
        for(int i=0;i<col;i++){
            if(board[row][i]==1){
                return false;
            }
        }
        for (int i = row, j = col; i >= 0 && j >= 0; i--, j--) {
            if (board[i][j] == 1) {
                return false;
            }
        }

        for (int i = row, j = col; i < N && j >= 0; i++, j--) {
            if (board[i][j] == 1) {
                return false;
            }
        }
        return true;
    }
    private void solveNQueen(int col,int N){
        if(col>=N){
            printSolution(N);
            return;
        }
        for(int i=0;i<N;i++){
            if(isSafe(i,col,N)){
                board[i][col]=1;
                solveNQueen(col+1,N);
                board[i][col]=0;
            }
        }
    }
    private void printSolution(int N) {
        ArrayList<Integer>ll=new ArrayList<>();
        for (int i = 0; i < N; i++) {
            for (int j = 0; j < N; j++) {
                if(board[i][j]==1){
                    ll.add(j+1);
                }
                // System.out.print((board[i][j] == 1 ? "Q " : "- "));
            }
        }
        list.add(ll);
    }
}
