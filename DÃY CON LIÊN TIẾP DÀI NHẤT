#include<iostream>
#include<algorithm>
#include<vector>
using namespace std;
typedef long long ll;
int main() {
	int n, q; cin >> n >> q;
	ll M[1000001];
	for (int i = 1; i <= n; i++) {
		cin >> M[i]; M[i] -= q;
	}
	bool ok[1000001] = { false };
	ok[0] = true;
	ll min = 0;
	M[0] = 0;
	for (int i = 1; i <= n; i++) {
		M[i] += M[i-1];
		if (M[i] < min) {
			min = M[i];
			ok[i] = true;
		}
	}
	int res = -1;
	int p = n;
	for (int i = n; i >=0; i--) {
		if (ok[i]) {
			while (i < p) {
				if (M[p] - M[i] >= 0) {
					res = max(res, p - i);
					break;
				}
				p--;
			}
		}
	}
	cout << res ;
}
