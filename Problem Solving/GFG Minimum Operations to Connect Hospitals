class Solution {
    public int minConnect(int V, int[][] edges) {
        DSU dsu = new DSU(V);
        int redundant = 0;

        for (int[] e : edges) {
            if (!dsu.union(e[0], e[1])) {
                redundant++;  // edge forms a cycle → reusable
            }
        }

        int components = dsu.countComponents();

        int required = components - 1;

        if (redundant >= required) 
            return required;

        return -1;
    }
}

class DSU {
    int[] parent, rank;
    int components;

    DSU(int n) {
        parent = new int[n];
        rank = new int[n];
        components = n;
        for (int i = 0; i < n; i++) parent[i] = i;
    }

    int find(int x) {
        if (parent[x] != x)
            parent[x] = find(parent[x]);
        return parent[x];
    }

    boolean union(int a, int b) {
        int pa = find(a), pb = find(b);
        if (pa == pb) return false;

        if (rank[pa] < rank[pb]) parent[pa] = pb;
        else if (rank[pb] < rank[pa]) parent[pb] = pa;
        else {
            parent[pb] = pa;
            rank[pa]++;
        }
        components--;
        return true;
    }

    int countComponents() {
        return components;
    }
}
