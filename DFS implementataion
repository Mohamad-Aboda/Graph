#include <iostream>
#include <stdio.h>
#include <memory.h>
#include <algorithm>
#include <vector>
#include <stack>
using namespace std;
int n, m;
vector<vector<int> >v;
bool vis[10001];
void dfs(int u) {
    vis[u] = 1;
    for (int i = 0; i < v[u].size(); ++i) {
        if (!vis[v[u][i]])
            dfs(v[u][i]);
    }
}
int main() {
    v.clear();
    v.resize(n);
    for (int i = 0; i < m; ++i) {
        int a, b; cin >> a >> b;
        v[a].push_back(b);
        // for directed 
        v[b].push_back(a);
    }
    memset(vis, 0, sizeof(vis));
    dfs(0);
    return 0;
}
