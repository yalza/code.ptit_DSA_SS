#include<iostream>
#include<vector>
#include<stdbool.h>
using namespace std;
bool ok;
void sinh(int* M, int n, int k) {
	int a = 0;
	for (int i = k; i > 0; i--) {
		if (M[i] != n - k + i) {
			a = 1;
			M[i]++;
			for (int j = i + 1; j <= k; j++)M[j] = M[j - 1] + 1; \
				break;
		}
	}
	if (a == 0)ok = true;
}
int main() {
	int t; cin >> t;
	while (t--) {
		int n, m; cin >> n >> m;
		int k = 3;
		vector<int> M(n+1);
		ok = false;
		for (int i = 1; i <= n; i++) {
			cin >> M[i];
		}
		int N[100]; 
		for (int i = 1; i <= k; i++)N[i] = i;
		long long int res = 0;
		while (!ok) {
			int sum = 0;
			for (int i = 1; i <= k; i++)sum += M[N[i]];
			if (sum<=m && m - res>=m - sum)res = sum;
			sinh(N, n, k);
		}
		cout << res << endl;
	}
}
