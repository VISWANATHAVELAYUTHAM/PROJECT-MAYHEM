class Solution {
    public String[] spellchecker(String[] W, String[] Q) {
        Set<String> orig = new HashSet<>(Arrays.asList(W));
        Map<String, String> lower = new HashMap<>(), mask = new HashMap<>();
        for (int i = W.length - 1; i >= 0; i--) {
            String word = W[i], wlow = word.toLowerCase();
            lower.put(wlow, word);
            mask.put(vmask(wlow), word);
        }
        for (int i = 0; i < Q.length; i++) {
            String query = Q[i], qlow = query.toLowerCase(),
                qmask = vmask(qlow);
            if (orig.contains(query)) continue;
            else if (lower.containsKey(qlow)) Q[i] = lower.get(qlow);
            else if (mask.containsKey(qmask)) Q[i] = mask.get(qmask);
            else Q[i] = "";
        }
        return Q;
    }
    public String vmask(String str) {
        StringBuilder sb = new StringBuilder();
        for (int i = 0; i < str.length(); i++) {
            char c = str.charAt(i);
            if (c == 'a' || c == 'e' || c == 'i' || c == 'o' || c == 'u') c = '*';
            sb.append(c);
        }
        return sb.toString();
    }
}
