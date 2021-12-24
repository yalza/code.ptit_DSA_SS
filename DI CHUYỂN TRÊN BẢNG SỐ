#include <iostream>
#include<set>
using namespace std;
#define Z 1000000000;
int n, m;
int M[501][501];
int dx[] = { -1, 0, 1, 0 };
int dy[] = { 0, 1, 0, -1 };
struct XX {
	int x, y, data;
	XX(int x, int y, int data) : x(x), y(y), data(data) {

	}
};
bool operator<(const XX&A,const XX&B) {
	if (A.data == B.data) {
		if (A.x == B.x)
			return A.y < B.y;
		else return A.x < B.x;
	}
	return A.data < B.data;
}
int BFS() {
	int N[501][501];
	for (int i = 0; i < m; i++)
		for (int j = 0; j < n; j++)
			N[i][j] = Z;
	set<XX> X;
	X.insert(XX(0,0,0));
	N[0][0] = M[0][0];
	while (X.size()) {
		XX x = *X.begin();
		X.erase(X.begin());
		for (int i = 0; i < 4; i++) {
			int a = x.x + dx[i];
			int b = x.y + dy[i];
			if (a >= 0 && a < m && b >= 0 && b < n) {
				if (N[a][b] > N[x.x][x.y] + M[a][b]) {
					if (N[a][b] != 1000000000) {
						X.erase(X.find(XX(a, b, N[a][b])));
					}
					N[a][b] = N[x.x][x.y] + M[a][b];
					X.insert(XX(a, b, N[a][b]));
				}
			}
		}
	}
	return N[m - 1][n - 1];
}
int main() {
	int t; cin >> t;
	while (t--) {
		cin >> m >> n;
		for (int i = 0; i < m; i++)
			for (int j = 0; j < n; j++)
				cin >> M[i][j];
		cout << BFS() << endl;
	}
}
