class Solution {
    public static ArrayList<Integer> constructList(int q, int[][] queries) {
        // code here
         ArrayList<Integer> arrLst = new ArrayList<>();
        int xor=0;
        for(int i=queries.length-1;i>=0;i--){
            if(queries[i][0]==1) xor^=queries[i][1];
            else arrLst.add(queries[i][1]^xor);
        }
        arrLst.add(0^xor);
        arrLst.sort((a,b)->a-b);
        return arrLst;
    }
  }
