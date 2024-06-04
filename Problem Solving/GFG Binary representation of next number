class Solution {
    String binaryNextNumber(String s) {
        // Remove leading zeros for correct processing
        s = s.replaceFirst("^0+(?!$)", "");
        
        int n = s.length();
        StringBuilder result = new StringBuilder(s);
        
        // Traverse from the end to the beginning
        for (int i = n - 1; i >= 0; i--) {
            if (s.charAt(i) == '0') {
                result.setCharAt(i, '1');
                return result.toString();
            } else {
                result.setCharAt(i, '0');
            }
        }
        
        // If we finished the loop, all were '1's, we need an extra '1' at the beginning
        return "1" + result.toString();
    }
}
