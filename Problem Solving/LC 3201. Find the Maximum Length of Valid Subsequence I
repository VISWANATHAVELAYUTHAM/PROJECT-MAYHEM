import java.util.ArrayList;
import java.util.List;

class Solution {
    public int solve(List<Integer> v, int a, int b) {
        int n = v.size();
        int i = 0, f = 0;
        int c = 0;
        while (i < n) {
            if ((f == 0 && v.get(i) == a) || (f == 1 && v.get(i) == b)) {
                c++;
                f = f ^ 1;
            }
            i++;
        }
        return c;
    }

    public int maximumLength(int[] nums) {
        List<Integer> v = new ArrayList<>();
        int ans, c1 = 0, c2 = 0;
        for (int i : nums) {
            int k = i % 2;
            v.add(k);
            if (k == 1)
                c1++;
            else
                c2++;
        }
        ans = Math.max(c1, c2);
        ans = Math.max(ans, solve(v, 0, 1));
        ans = Math.max(ans, solve(v, 1, 0));
        return ans;
    }
}
