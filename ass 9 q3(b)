//B
//Prim’s Algorithm
#include <iostream>
using namespace std;

int main() {
    int n, m;
    cin >> n >> m;

    int adj[100][100];
    int i, j;

    for (i = 0; i < n; i++)
        for (j = 0; j < n; j++)
            adj[i][j] = 0;

    for (i = 0; i < m; i++) {
        int u, v, w;
        cin >> u >> v >> w;
        adj[u][v] = w;
        adj[v][u] = w;
    }

    int key[100];
    int parent[100];
    int inMST[100];

    for (i = 0; i < n; i++) {
        key[i] = 1000000000;
        inMST[i] = 0;
        parent[i] = -1;
    }

    key[0] = 0;

    for (int cnt = 0; cnt < n - 1; cnt++) {
        int u = -1;
        int minKey = 1000000000;
        for (i = 0; i < n; i++) {
            if (!inMST[i] && key[i] < minKey) {
                minKey = key[i];
                u = i;
            }
        }

        inMST[u] = 1;

        for (int v = 0; v < n; v++) {
            if (adj[u][v] && !inMST[v] && adj[u][v] < key[v]) {
                key[v] = adj[u][v];
                parent[v] = u;
            }
        }
    }

    int mstWeight = 0;
    for (i = 1; i < n; i++) {
        cout << parent[i] << " - " << i << " (" << adj[parent[i]][i] << ")\n";
        mstWeight += adj[parent[i]][i];
    }
    cout << "MST Weight = " << mstWeight;
}
