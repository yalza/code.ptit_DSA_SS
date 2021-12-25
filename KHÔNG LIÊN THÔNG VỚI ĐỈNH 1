#include<iostream>
#include<vector>
#include<cstring>
using namespace std;
vector<int> A[1001];
bool check[1001];
void DFS(int u) {
	check[u] = true;
	for (int x : A[u])
		if (!check[x])
			DFS(x);
}
int main() {
	int n, m; cin >> n >> m;
	for (int i = 0; i < m; i++) {
		int a, b; cin >> a >> b;
		A[a].push_back(b);
		A[b].push_back(a);
	}
	DFS(1);
	int a = 0;
	for (int i = 1; i <= n; i++) {
		if (!check[i]) {
			cout << i << endl;
			a++;
		}
	}
	if (a == 0)cout << 0 << endl;
}
