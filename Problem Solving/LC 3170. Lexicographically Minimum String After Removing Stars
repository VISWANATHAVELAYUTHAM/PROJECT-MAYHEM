
class Solution {
    public String clearStars(String s){
        int n = s.length();
        
        List<List<Integer>> buckets = new ArrayList<>();
        
        for(int i = 0; i < 26; i++){
            buckets.add(new ArrayList<>());
        }
        
        boolean[] removed = new boolean[n];
        
        for (int i = 0 ; i < n ; i++){
            if(s.charAt(i) == '*'){
                removed[i] = true;
                for (int j = 0; j < 26; j++){
                    if (!buckets.get(j).isEmpty()){
                        removed[buckets.get(j).get(buckets.get(j).size() - 1)] = true;
                        buckets.get(j).remove(buckets.get(j).size() - 1);
                        break;
                    }
                }
            } 
            else{
                buckets.get(s.charAt(i) - 'a').add(i);
            }
        }
        
        StringBuilder ans = new StringBuilder();
        for(int i = 0 ; i < n ; i++){
            if(!removed[i]) ans.append(s.charAt(i));
        }
        return ans.toString();
    }
}
