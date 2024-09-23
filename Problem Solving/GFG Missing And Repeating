class Solve {
    int[] findTwoElement(int arr[]) {
        int res[]=new int[2];
        int n=arr.length;
       int tmp[]=new int[arr.length+1];
       for(int i=0;i<n;i++)
       tmp[arr[i]]++;
       int x=0,y=0;
       for(int i=1;i<tmp.length;i++)
       {
           if(tmp[i]==0)
           x=i;
           else if(tmp[i]>1)
           y=i;
       }
       res[0]=y;
      res[1]=x;
        return res;
    }
}
