#include<iostream>
#include<vector>
#include<cstring>
#include<string>
using namespace std;
vector<int> A[1001];
bool check[1001];
vector<string> M, N;
void reset() {
	memset(check, false, sizeof(check));
	for (int i = 0; i < 1001; i++)A[i].clear();
	M.clear();
	N.clear();
}
void DFS_one(int u,string s) {
	check[u] = true;
	if (u == 2) {
		M.push_back(s);
	}
	for (int x : A[u]) {
		if (!check[x])
			DFS_one(x, s + to_string(x));
	}
	check[u] = false;
}
void DFS_two(int u, string s) {
	check[u] = true;
	if (u == 1) {
		N.push_back(s);
	}
	for (int x : A[u]) {
		if (!check[x])
			DFS_two(x, s + to_string(x));
	}
	check[u] = false;
}
int min_l(string a, string b) {
	int M[200] = { 0 };
	for (int i = 0; i < a.length(); i++)
		M[a[i]]++;
	for (int i = 0; i < b.length(); i++)
		M[b[i]]++;
	int count = 0;
	for (int i = 0; i < 200; i++)
		if (M[i] >= 1)count++;
	return count;
}
int main() {
	int t; cin >> t;
	while (t--) {
		reset();
		int n, m; cin >> n >> m;
		for (int i = 0; i < m; i++) {
			int a, b; cin >> a >> b;
			A[a].push_back(b);
		}
		DFS_one(1, "1");
		memset(check, false, sizeof(check));
		DFS_two(2, "2");
		int res = 10000;
		for (int i = 0; i < M.size(); i++) {
			for (int j = 0; j < N.size(); j++) {
				res = min(res, min_l(M[i], N[j]));
			}
		}
		cout << res << endl;
	}
}
