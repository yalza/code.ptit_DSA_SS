#include<iostream>
#include<vector>
#include<cstring>
#include<string>
#include<queue>
using namespace std;
bool check[1001];
vector<int> A[1001];
int B[1001];
void BFS(int u,int v) {
	queue<int> X;
	X.push(u);
	while (X.size()) {
		int x = X.front();
		X.pop();
		check[x] = true;
		if (x == v)return;
		for (int f : A[x]) {
			if (!check[f]) {
				X.push(f);
				check[f] = true;
				B[f] = x;
			}
		}
	}
}
void Truy_vet(int u, int v) {
	if (!check[v]) {
		cout << -1;
		return;
	}
	vector<int> X;
	while (u != v) {
		if (u == 0) {
			cout << -1;
			return;
		}
		X.push_back(u);
		u = B[u];
	}
	X.push_back(v);
	for (int i = X.size() - 1; i >= 0; i--) {
		cout << X[i]<<" ";
	}
}
int main() {
	int t; cin >> t;
	while (t--) {
		memset(check, false, sizeof(check));
		memset(B, 0, sizeof(B));
		for (int i = 0; i < 1001; i++)A[i].clear();
		int n, m; cin >> n >> m;
		int a, b; cin >> a >> b;
		for (int i = 0; i < m; i++) {
			int x, y; cin >> x >> y;
			A[x].push_back(y);
		}
		BFS(a, b);
		Truy_vet(b, a);
		cout << endl;

	}
}
