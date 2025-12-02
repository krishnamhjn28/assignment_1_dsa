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

    int dist[100];
    int visited[100];

    for (i = 0; i < n; i++) {
        dist[i] = 1000000000;
        visited[i] = 0;
    }

    int src;
    cin >> src;
    dist[src] = 0;

    for (int cnt = 0; cnt < n - 1; cnt++) {
        int u = -1;
        int mind = 1000000000;
        for (i = 0; i < n; i++) {
            if (!visited[i] && dist[i] < mind) {
                mind = dist[i];
                u = i;
            }
        }

        if (u == -1) break;

        visited[u] = 1;

        for (int v = 0; v < n; v++) {
            if (adj[u][v] && !visited[v] && dist[u] + adj[u][v] < dist[v]) {
                dist[v] = dist[u] + adj[u][v];
            }
        }
    }

    for (i = 0; i < n; i++)
        cout << "Distance from " << src << " to " << i << " = " << dist[i] << endl;
}
