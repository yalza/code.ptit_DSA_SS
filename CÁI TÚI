#include<iostream>
#include<vector>
using namespace std;


int main() {
	int t; cin >> t;
	while (t--) {
		int n, k; cin >> n >> k;
		pair<int, int> M[1000000];
		for (int i = 0; i < n; i++) 
			cin >> M[i].first;
		for (int i = 0; i < n; i++)
			cin>> M[i].second;
		int dp[n+1][k+1];
		for (int i = 0; i <= n; i++) {
			for (int j = 0; j <= k; j++) {
				if (i == 0 || j == 0)dp[i][j] = 0;
				else if (j < M[i].first) {
					dp[i][j] = dp[i - 1][j];
				}
				else {
					dp[i][j] = max(dp[i - 1][j], M[i].second+dp[i - 1][j - M[i].first]);
				}
			}
		}
		cout << dp[n][k] << endl;
	}
}
