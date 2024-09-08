class Solution {
    static int minJumps(int[] arr) {
        if (arr[0] == 0) {
            return -1;
        }
        
        int jump = 1;
        int pos = 0;
        while (pos + arr[pos] < arr.length - 1) {
            int max = 0;
            int tpos = pos;
            for (int i = pos + 1; i <= pos + arr[pos]; i++) {
                if (i > arr.length) {
                    break;
                }
                if (max < i + arr[i]) {
                    max = i + arr[i];
                    tpos = i;
                }
            }
            if (pos == tpos) {
                return -1;
            } else {
                pos = tpos;
                jump += 1;
            }
        }
        return jump;
    }
}
