class Solution {

    String compareFrac(String str) {
        String s1="", s2="", s3="", s4="";
        int a=0, b=0, c=0, d=0;
        int i=0;
    
    // Extract a
        while(str.charAt(i) != '/') s1 += str.charAt(i++);
        a = Integer.parseInt(s1);
        i++;        // ignore '/' symbol
    
    // Extract b  
        while(str.charAt(i) != ',') s2 += str.charAt(i++);
        b = Integer.parseInt(s2);
        
        i += 2;     // ignore ',' and ' ' symbol
       
    // Extract c 
        while(str.charAt(i) != '/') s3 += str.charAt(i++);
        i++;        // ignore '/' symbol
        c = Integer.parseInt(s3);

    // Extract d
        while(i < str.length()) s4 += str.charAt(i++);
        d= Integer.parseInt(s4);
        
    // Comparing two fractions
        float f1 = (float)a/(float)b;
        float f2 = (float)c/(float)d;
        
        if(f1 == f2) return "equal";        
    
        return f1 > f2 ? s1+"/"+s2 : s3+"/"+s4;
    }
}
