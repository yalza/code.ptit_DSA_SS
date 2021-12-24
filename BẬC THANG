#include<iostream>
#include<vector>
using namespace std;
int main() {
	int t; cin >> t;
	while (t--) {
		int n, k; cin >> n >> k;
		vector<long long> M(n + 1);
		M[0] = M[1] = 1;
		for (int i = 2; i <= n; i++) {
			for (int j = 1; j <= min(k, i); j++) {
				M[i] += M[i - j];
				M[i] %= 1000000007;
			}
		}
		cout <<M[n]<< endl;
	}
}
