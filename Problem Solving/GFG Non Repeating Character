class Solution {
    // Function to find the first non-repeating character in a string.
    static char nonRepeatingChar(String s) {
     for(int i=0;i<s.length();i++)
     {
         boolean flag=true;
         for(int j=0;j<s.length();j++)
         {
             if(i!=j && s.charAt(i)==s.charAt(j))
             {
                 flag=false;
                 break;
             }
         }
         if(flag)
         {
             return s.charAt(i);
         }
     }
    return '$';
    }
}
