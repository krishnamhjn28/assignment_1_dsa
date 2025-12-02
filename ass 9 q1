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
        int u, v;
        cin >> u >> v;
        adj[u][v] = 1;
        adj[v][u] = 1;
    }

    int start;
    cin >> start;

    int visited[100] = {0};
    int q[1000];
    int front = 0, rear = 0;

    q[rear++] = start;
    visited[start] = 1;

    while (front < rear) {
        int u = q[front++];
        cout << u << " ";
        for (int v = 0; v < n; v++) {
            if (adj[u][v] && !visited[v]) {
                visited[v] = 1;
                q[rear++] = v;
            }
        }
    }
}
