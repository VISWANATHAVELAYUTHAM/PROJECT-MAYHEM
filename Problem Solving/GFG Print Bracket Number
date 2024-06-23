class Solution {
    ArrayList<Integer> bracketNumbers(String str) {
        // code here
        ArrayList<Integer> ans = new ArrayList<>();
        Stack<Integer> st= new Stack<>();
        int count = 1;
        for(int i = 0; i < str.length() ; i++){
            char ch = str.charAt(i);
            if(ch == '('){
                st.push(count);
                ans.add(st.peek());
                count++;
            }else if(ch == ')'){
                ans.add(st.pop());
            }
        }
        return ans;
    }
};
