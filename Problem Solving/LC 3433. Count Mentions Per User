class Solution {
    public int[] countMentions(int numberOfUsers, List<List<String>> events) {
        int[] mentions=new int[numberOfUsers];
        int[] offTime=new int[numberOfUsers];

        Collections.sort(events, (a,b)->Integer.parseInt(a.get(1))==Integer.parseInt(b.get(1))? b.get(0).compareTo(a.get(0)): Integer.parseInt(a.get(1))-Integer.parseInt(b.get(1))
                        );
        
        for(int i=0; i<events.size(); i++){
            if(events.get(i).get(0).equals("MESSAGE")){
                messageFunc(events.get(i), mentions, offTime);
            }
            else if(events.get(i).get(0).equals("OFFLINE")){
                offlineFunc(events.get(i), mentions, offTime);
            }
        }

        return mentions;
    }

    void messageFunc(List<String> event, int[] mentions, int[] offTime){
        int time=Integer.parseInt(event.get(1));
        String[] str=event.get(2).split(" ");

        for(String s:str){
            if(s.equals("ALL")){
                for(int i=0; i<mentions.length; i++){
                    mentions[i]+=1;
                }
            }
            else if(s.equals("HERE")){
                for(int i=0; i<mentions.length; i++){
                    if(offTime[i]==0){ //Only online
                        mentions[i]+=1;
                    }
                    else if(offTime[i]+60<=time){
                        mentions[i]+=1;
                        offTime[i]=0;
                    }
                }
            }
            else{
                int idx=Integer.parseInt( s.substring("id".length()) );
                mentions[idx]+=1;
            }
        }
    }

    void offlineFunc(List<String> event, int[] mentions, int[] offTime){
        int time=Integer.parseInt(event.get(1));
        String[] str=event.get(2).split(" ");
        
        for(String s:str){
            int idx=Integer.parseInt(s);
            offTime[idx]=time;
        }
    }
}
