#include<iostream>
#include<vector>
#include<cstring>
#include<string>
using namespace std;
vector<int> A[1001];
bool check[1001];
bool ok; int n, m;
void reset() {
	for (int i = 0; i < 1001; i++)A[i].clear();
	memset(check, false, sizeof(check));
	ok = false;
}
void DFS(int u,string s) {
	if (s.length() == n)ok = true;
	check[u] = true;
	for (int x : A[u]) {
		if (!check[x]) {
			DFS(x,s+to_string(x));
		}
	}
	check[u] = false;
		
}
bool ktra() {
	for (int i = 1; i <= n; i++) {
		memset(check, false, sizeof(check));
		ok = false;
		DFS(i,to_string(i));
		if (ok)return true;
	}
	return false;
}

int main() {
	int t; cin >> t;
	while (t--) {
		reset();
		cin >> n >> m;
		for (int i = 0; i < m; i++) {
			int a, b; cin >> a >> b;
			A[a].push_back(b);
			A[b].push_back(a);
		}
		if (ktra())cout << 1 << endl;
		else cout << 0 << endl;
	}
}
