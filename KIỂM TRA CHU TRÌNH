#include <iostream>
#include <cstring>
#include <vector>
#include<stack>
using namespace std;
vector<int> k[1005];
bool chuaxet[1005];
int truoc[1005];
void dfs(int d, int& kt) {
	chuaxet[d] = false;
	for (int i = 0; i < k[d].size(); i++) {
		int y = k[d][i];
		if (chuaxet[y] == true) {
			truoc[y] = d;
			dfs(y, kt);
		}
		else if (truoc[d] != y)kt = 1;
	}
}
int ktra(int v) {
	int kt = 0;
	for (int i = 1; i <= v; i++) {
		memset(chuaxet, true, sizeof(chuaxet));
		memset(truoc, 0, sizeof(truoc));
		dfs(i, kt);
		if (kt == 1) return 1;
	}
	return 0;
}
int main() {
	int t; cin >> t;
	while (t--) {
		int v, e; cin >> v >> e;
		for (int i = 0; i < 1005; i++)k[i].clear();
		memset(chuaxet, true, sizeof(chuaxet));
		memset(truoc, 0, sizeof(truoc));
		for (int i = 1; i <= e; i++) {
			int a, b; cin >> a >> b;
			k[a].push_back(b);
			k[b].push_back(a);
		}
		if (ktra(v) == 1)cout << "YES" << endl;
		else cout << "NO" << endl;
	}
}
