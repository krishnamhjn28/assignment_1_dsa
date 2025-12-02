#include <iostream>
using namespace std;

int adj[100][100];
int visited[100];
int n;

void dfs(int u) {
    visited[u] = 1;
    cout << u << " ";
    for (int v = 0; v < n; v++) {
        if (adj[u][v] && !visited[v]) dfs(v);
    }
}

int main() {
    int m;
    cin >> n >> m;

    int i, j;
    for (i = 0; i < n; i++)
        for (j = 0; j < n; j++)
            adj[i][j] = 0;

    for (i = 0; i < m; i++) {
        int u, v;
        cin >> u >> v;
        adj[u][v] = 1;
        adj[v][u] = 1;
    }

    for (i = 0; i < n; i++) visited[i] = 0;

    int start;
    cin >> start;
    dfs(start);
}
