#include<iostream>
#include<string.h>
using namespace std;
char M[100][100];
int m, n;
bool dp[100][100];
void slove(int i, int j) {
	dp[i][j] = true;
	if (M[i][j] == '#' && M[i - 1][j] == '#' && i > 0&&!dp[i-1][j]) {
		dp[i - 1][j] = true;
		slove(i - 1, j);
	}
	else if (M[i][j] == '#' && M[i][j - 1] == '#' && j > 0&&!dp[i][j-1]) {
		dp[i][j - 1] = true;
		slove(i, j - 1);
	}
	else if (M[i][j] == '#' && M[i + 1][j] == '#' && i < m-1&&!dp[i+1][j]) {
		dp[i + 1][j] = true;
		slove(i + 1, j);
	}
	else if (M[i][j] == '#' && M[i][j + 1] == '#' && j < n-1&&!dp[i][j+1]) {
		dp[i][j + 1] = true;
		slove(i, j + 1);
	}
}

int main() {
	 cin >> m >> n;
	 memset(dp, false, sizeof(dp));
	for (int i = 0; i < m; i++) {
		for (int j = 0; j < n; j++) {
			cin >> M[i][j];
		}
	}
	int count = 0;
	for (int i = 0; i < m; i++) {
		for (int j = 0; j < n; j++) {
			if (!dp[i][j]&&M[i][j]=='#') {
				count++;
				slove(i, j);
			}
		}
	}
	cout << count << endl;
}
