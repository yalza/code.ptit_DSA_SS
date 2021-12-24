#include<iostream>
#include<vector>
#include<cstring>
using namespace std;
vector<int> A[1001];
bool check[1001];
int n, m;
int maxx;
void DFS(int u, int v) {
	check[u] = true;
	if (check[v])return;
	for (int i : A[u]) {
		if (!check[i])
			DFS(i, v);
	}
}
int main() {
	int t; cin >> t;
	while (t--) {
		for (int i = 0; i < 1001; i++)A[i].clear();
		 cin >> n >> m;
		for (int i = 0; i < m; i++) {
			int a, b; cin >> a >> b;
			maxx = max(maxx, max(a, b));
			A[a].push_back(b);
			A[b].push_back(a);
		}
		int q; cin >> q;
		while (q--) {
			int u, v; cin >> u >> v;
			memset(check, false, sizeof(check));
			DFS(u, v);
			if (check[v])cout << "YES\n";
			else cout << "NO\n";
		}
	}
}
