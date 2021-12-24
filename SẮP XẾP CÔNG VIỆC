#include<iostream>
#include<vector>
using namespace std;
int main() {
	int t; cin >> t;
	while (t--) {
		vector<pair<int, int>> M(10000);
		int n; cin >> n;int dp[10000];
		for (int i = 0; i < n; i++) {
			cin >> M[i].first; dp[i] = 1;
		}
		for (int i = 0; i < n; i++)cin >> M[i].second;
		for (int i = 0; i < n - 1; i++) {
			for (int j = i+1; j < n; j++) {
				if (M[i].second > M[j].second)
					swap(M[i], M[j]);
			}
		}
		int maxx = 1;
		for (int i = n - 2; i >= 0; i--) {
			int max = 0;
			for (int j = i + 1; j < n; j++) {
				if (M[j].first >= M[i].second && dp[j] > max)max = dp[j];
			}
			dp[i] += max;
			if (dp[i] > maxx)maxx = dp[i];
		}
		cout << maxx << endl;
	}
}
