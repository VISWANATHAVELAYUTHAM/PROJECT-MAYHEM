class Solution {
    public void rearrange(int[] arr, int x) {
        // code here
        List<Pair> list = new ArrayList<>();
        for(int num : arr){
            list.add(new Pair(num, (int)Math.abs(num - x)));
        }
        list.sort(Comparator.comparingInt(p -> p.diff));
        for(int i=0; i<list.size(); i++){
            arr[i] = list.get(i).getEle();
        }
        
    }
    static class Pair {
        int ele;
        int diff;
        
        Pair(int ele, int diff){
            this.ele = ele;
            this.diff = diff;
        }
        public int getEle(){
            return this.ele;
        }
    }
}
