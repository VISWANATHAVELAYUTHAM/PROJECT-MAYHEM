class Solution {
    int lps(String str) {
        // code here
        int n=str.length();
        
        int p=0,s=1,pos=1,count=0;
        
        while(p<n && s<n){
            if(str.charAt(p)==str.charAt(s)){
                p++;
                s++;
                count++;
            }
            else{
                p=0; //reset prefix pointer to start
                pos++; //incement suffix start position
                s=pos; //update suffix to new start position
                count=0;
            }
        }
        return count;
    }
}
