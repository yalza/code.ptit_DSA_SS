#include <iostream>
#include <vector>
#include <algorithm> 
#include<cstring>
using namespace std;
vector<int> A[1001];
bool check[1001];
struct XX {
	int u, v, w;
};
vector<XX> X;
void reset() {
	for (int i = 0; i < 1001; i++) {
		A[i].clear();
	}
	X.clear();
	memset(check, false, sizeof(check));
}
bool cmp(XX a, XX b) {
	return a.w < b.w;
}

void DFS(int u) {
	check[u] = true;
	for (int x : A[u]) {
		if (!check[x])
			DFS(x);
	}
}

int main() {
	int t; cin >> t;
	while (t--) {
		reset();
		int n, m; cin >> n >> m;
		for (int i = 0; i < m; i++) {
			XX a; cin >> a.u >> a.v >> a.w;
			X.push_back(a);
		}
		sort(X.begin(), X.end(), cmp);
		int res = 0;
		for (XX x : X) {
			memset(check, false, sizeof(check));
			DFS(x.u);
			if (!check[x.v]) {
				res += x.w;
				A[x.u].push_back(x.v);
				A[x.v].push_back(x.u);
			}
		}
		cout << res << endl;
	}
}
