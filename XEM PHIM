#include<iostream>
using namespace std;

int main() {
	int m, n; cin >> m >> n;
	int M[100] = { 0 };
	for (int i = 1; i <= n; i++)cin >> M[i];
	int N[n+1][m+1] = { 0 };
	for (int i = 1; i <= n; i++) {
		for (int j = 1; j <= m; j++) {
			if (j < M[i])N[i][j] = N[i - 1][j];
			else
				N[i][j] = max(N[i - 1][j], N[i - 1][j - M[i]] + M[i]);
		}
	}
	cout << N[n][m];
}
