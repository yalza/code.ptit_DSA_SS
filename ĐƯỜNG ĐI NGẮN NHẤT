#include<iostream>
#include<vector>
#include<cstring>
using namespace std;
int ok[500][500];

int main() {
	int n, m; cin >> n >> m;
	for (int i = 1; i <= n; i++) {
		for (int j = 1; j <= n; j++) {
			ok[i][j] = 1000000000;
		}
	}
	for (int i = 1; i <= n; i++)ok[i][i] = 0;
	for (int i = 0; i < m; i++) {
		int a, b, k; cin >> a >> b >> k;
		ok[a][b] = ok[b][a] = k;
	}
	for(int k=1;k<=n;k++)
	for (int i = 1; i <= n; i++) {
		for (int j = 1; j <= n; j++) {
			ok[i][j] = min(ok[i][j], ok[i][k] + ok[k][j]);
		}
	}
	int t; cin >> t;
	while (t--) {
		int u, v; cin >> u >> v;
		cout << ok[u][v] << endl;
	}
}
