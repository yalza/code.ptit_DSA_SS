#include<iostream>
#include<vector>
#include<set>
#include<queue>
#include<cstring>
using namespace std;
int n;
typedef pair<int, int> p;
bool check[1001][1001];
vector<p> X;
set<pair<p, p>> Y;
int dx[4] = { -1,1,0,0 };
int dy[4] = { 0,0,1,-1 };
void DFS(p u) {
	check[u.first][u.second] = true;
	for (int i = 0; i < 4; i++) {
		int x = u.first + dx[i];
		int y = u.second + dy[i];
		if (x >= 1 && x <= n && y >= 1 && y <= n && !check[x][y] && Y.count({ u, { x,y } }) == 0)
			DFS({ x,y });
	}
}
int main() {
	int k, m; cin >> n >> k >> m;
	for (int i = 0; i < m; i++) {
		int a, b, c, d;
		cin >> a >> b >> c >> d;
		Y.insert({ {a,b},{c,d} });
		Y.insert({ {c,d},{a,b} });
	}
	for (int i = 0; i < k; i++) {
		int a, b; cin >> a >> b;
		X.push_back({ a,b });
	}
	int res = 0;
	for (p x: X) {
		for (int i = 0; i < 1001; i++)memset(check[i], false, 1001);
		DFS(x);
		for (p y : X) {
			if (!check[y.first][y.second])
				res++;
		}
	}
	cout << res/2 << endl;
}
