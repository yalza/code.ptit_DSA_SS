#include<iostream>
using namespace std;

int main() {
	int t; cin >> t;
	while (t--) {
		int n; cin >> n;
		int M[100000];
		for (int i = 0; i < n; i++)cin >> M[i];
		int dp[100000];
		dp[0] = M[0];
		dp[1] = max(M[1], M[0]);
		for (int i = 2; i < n; i++)
			dp[i] = max(dp[i - 2] + M[i],dp[i - 1]);
		cout << dp[n - 1] << endl;
	}
}
