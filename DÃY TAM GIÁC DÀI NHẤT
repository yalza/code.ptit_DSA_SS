#include<iostream>
#include<vector>
using namespace std;

int main() {
	int t; cin >> t;
	while (t--) {
		int n; cin >> n;
		int M[100000];
		vector<pair<int, int>> N;
		for (int i = 0; i < n; i++)cin >> M[i];
		int dem = 1;
		M[n] = 0;
		for (int i = 1; i <= n; i++) {
			if (M[i] > M[i - 1]) {
				dem++;
			}
			else {
				N.push_back({ i, dem });
				dem = 1;
			}
		}
		int res = 0;
		for (int i = 0; i < N.size(); i++) {
			dem = 0;
			for (int j = N[i].first; j < n && j>0; j++) {
				if (M[j] < M[j - 1]) {
					dem++;
				}
				else break;
			}
			res = max(res, N[i].second + dem);
		}
		cout << res << endl;
	}
}
