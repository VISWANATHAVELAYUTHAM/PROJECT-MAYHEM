import java.util.*;

public class Solution {
    public int maxTaskAssign(int[] tasks, int[] workers, int pills, int strength) {
        Arrays.sort(tasks);
        Arrays.sort(workers);
        
        int left = 0, right = Math.min(tasks.length, workers.length), answer = 0;
        
        while (left <= right) {
            int mid = (left + right + 1) / 2;
            if (canAssign(tasks, workers, pills, strength, mid)) {
                answer = mid;
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }

        return answer;
    }

    private boolean canAssign(int[] tasks, int[] workers, int pills, int strength, int k) {
        if (k == 0) return true;
        if (k > workers.length) return false;

        TreeMap<Integer, Integer> availableWorkers = new TreeMap<>();
        for (int i = workers.length - k; i < workers.length; i++) {
            availableWorkers.put(workers[i], availableWorkers.getOrDefault(workers[i], 0) + 1);
        }

        int usedPills = 0;
        for (int i = k - 1; i >= 0; i--) {
            int task = tasks[i];

            Integer key = availableWorkers.floorKey(Integer.MAX_VALUE);
            if (key != null && key >= task) {
                decrementCount(availableWorkers, key);
            } else {
                Integer boosted = availableWorkers.ceilingKey(task - strength);
                if (boosted == null || usedPills >= pills) return false;
                decrementCount(availableWorkers, boosted);
                usedPills++;
            }
        }

        return true;
    }

    private void decrementCount(TreeMap<Integer, Integer> map, int key) {
        if (map.get(key) == 1) {
            map.remove(key);
        } else {
            map.put(key, map.get(key) - 1);
        }
    }
}
