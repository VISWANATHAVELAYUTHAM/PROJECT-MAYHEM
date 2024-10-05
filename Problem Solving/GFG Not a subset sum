class Solution {
    public long findSmallest(int[] arr) {
        // Your code goes here
        long i = 1;
        long sum = 0;
        //int j = 0;
        if(arr[0] != 1)
        {
            return (long)1;
        }
        
        for(int j = 0; j < arr.length; j++)
        {
            sum += arr[j];
            if(arr[j] != j+1 && j+1 > sum)
            {
                return (long)sum+1;
            }
            else
            {
                while(j < arr.length-1 && arr[j+1] <= sum)
                {
                    sum += arr[j+1];
                    j++;
                }
                if(j < arr.length-1 && arr[j+1] > sum+1)
                {
                    return sum+1;
                }
            }
            
        }
        
        return sum+1;
    }
}
