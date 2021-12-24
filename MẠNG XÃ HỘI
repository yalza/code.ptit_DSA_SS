#include<iostream>
#include<vector>
#include<cstring>
#include<set>
using namespace std;
vector<int> A[100001];
bool check[100001];
int truoc[100001];
set<pair<int,int>> X;
void reset() {
	memset(check, false, sizeof(check));
	for (int i = 0; i < 100001; i++)A[i].clear();
	memset(truoc, false, sizeof(truoc));
	X.clear();
}
bool DFS(int u) {
	for (int x : A[u]) {
		for (int y : A[x]) {
			if (X.count({ u,y })==0&&y!=u) {
				return false;
			}
		}
	}
	return true;
}
bool ktra(int n) {
	for (int i = 1; i <= n; i++) {
		memset(check, false, sizeof(check));
		if (!DFS(i))return false;
	}
	return true;
}
int main() {
	int t; cin >> t;
	while (t--) {
		reset();
		int n, m; cin >> n >> m;
		for (int i = 0; i < m; i++) {
			int a, b; cin >> a >> b;
			X.insert({ a,b });
			X.insert({ b,a });
			A[a].push_back(b);
			A[b].push_back(a);
		}
		if (ktra(n))cout << "YES\n";
		else cout << "NO\n";
	}
}
