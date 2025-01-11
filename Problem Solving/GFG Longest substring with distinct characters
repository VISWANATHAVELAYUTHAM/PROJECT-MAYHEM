class Solution {
    public int longestUniqueSubstr(String s) {
        HashSet<Character> set = new HashSet<>();
        int left = 0, maxLength = 0;

        // Iterate through the string with the right pointer
        for (int right = 0; right < s.length(); right++) {
            // If the character is already in the set, move the left pointer
            // to remove the duplicate character
            while (set.contains(s.charAt(right))) {
                set.remove(s.charAt(left));
                left++;
            }

            // Add the current character to the set
            set.add(s.charAt(right));

            // Update the maximum length of the substring
            maxLength = Math.max(maxLength, right - left + 1);
        }

        return maxLength;
    }
}
