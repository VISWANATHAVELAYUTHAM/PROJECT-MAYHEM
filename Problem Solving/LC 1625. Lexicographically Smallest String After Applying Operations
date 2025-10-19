class Solution {
    public String findLexSmallestString(String s, int a, int b) {
        //3456 a=5
        //3951

        //3456 b=2
        //5634

        Queue<String> queue= new LinkedList<>();
        Set<String> seen= new HashSet<>();

        String smallest= s;

        queue.add(s);
        seen.add(s);

        while(!queue.isEmpty()){
            String curr= queue.poll();
            if(curr.compareTo(smallest)<0){
                smallest= curr;
            }

            //a.compareTo(b)
            //if(a>b) it will return >0
            //else if(a<b) return <0
            //if equal return 0

            //operation 1
            char[] arr= curr.toCharArray();
            for(int i=1; i<arr.length; i+=2){
                int val= (arr[i]-'0'+a)%10;
                arr[i]= (char)(val+'0');
            }
            String toAdd= new String(arr);
            if(seen.add(toAdd)){
                //if value is in set : false
                // if not in set and got added : true
                queue.add(toAdd);
            }

            //operation 2
            String rotated= curr.substring(curr.length()-b, curr.length())+curr.substring(0, curr.length()-b);
            if(seen.add(rotated)){
                queue.add(rotated);
            }
        }
        return smallest;
    }
}
