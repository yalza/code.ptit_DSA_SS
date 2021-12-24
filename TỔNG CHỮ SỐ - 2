#include<iostream>
#include<string.h>
#include<vector>
using namespace std;
int dp[901][8101];
int Minleng(int a, int b) {
	if (a > b || a < 0 || b < 0||a>900||b>8100)return -1;
	if (a == 0 && b == 0)return 0;
	if (dp[a][b] != -1)return dp[a][b];
	int y = 101;
	for (int i = 9; i >= 1; i--) {
		int x = Minleng(a - i, b - i * i);
		if (x != -1)y = min(y, x + 1);
	}
	return dp[a][b]=y;
}
int main() {
	int t; cin >> t;
	while (t--) {
		int a, b; cin >> a >> b;
		memset(dp, -1, sizeof(dp));
		dp[0][0] = 0;
		int x = Minleng(a, b);
		if (x == -1 || x >100)cout << -1;
		else {
			while (a>0&&b>0) {
				for (int i = 1; i <= 9; i++) {
					if (a >= i && b >= i*i &&1+dp[a - i][b - i * i]== dp[a][b]) {
						cout << i; a -= i; b -= i * i;
						break;
					}
				}
			}
			
		}
		cout << endl;
	}
}
