#include<iostream>
#include<vector>
#include<cstring>
#include<queue>
using namespace std;
vector<int> A[1001];
bool check[1001];
int M[1001];
int n, m, v;
void reset() {
	for (int i = 0; i < 1001; i++)A[i].clear();
	memset(check, false, sizeof(check));
}

bool BFS() {
	int maxx = 1;
	memset(check, false, sizeof(check));
	for (int i = 1; i <= n; i++)M[i] = 1;
	for (int i = 1; i <= n; i++) {
		if (!check[i]) {
			check[i] = true;
			queue<int> X;
			X.push(i);
			while (X.size()) {
				int z = X.front(); X.pop();
				for (int x : A[z]) {
					if (M[x] == M[z])M[x]++;
					maxx = max(maxx, max(M[x], M[z]));
					if (maxx > v)return false;
					if (!check[x]) {
						check[x] = true;
						X.push(x);
					}
				}
			}
		}
	}
	return true;
}

int main() {
	int t; cin >> t;
	while (t--) {
		reset();
		cin >> n >> m >> v;
		for (int i = 0; i < m; i++) {
			int a, b;
			cin >> a >> b;
			A[a-1].push_back(b-1);
			A[b-1].push_back(a-1);
		}
		if (BFS())cout << "YES\n";
		else cout << "NO\n";
	}
}
