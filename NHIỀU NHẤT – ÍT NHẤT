#include<iostream>
using namespace std;
typedef long long ll;
int K_tra(int*M,int n,int m,int k) {
	int x = 1;
	ll sum = 0;
	for (int i = 0; i < n; i++) {
		if (M[i] > k)return 0;
		if (sum + M[i] <= k)sum += M[i];
		else {
			x++;
			if (x > m)return false;
			sum = M[i];
		}
	}
	return 1;
}
ll Min_max(int* M, int n, int m, ll sum) {
	ll l = 0, r = sum;
	ll res = sum;
	while (l <= r) {
		ll mid = (l + r)/2;
		if (K_tra(M, n, m, mid)) {
			res = mid;
			r = mid - 1;
		}
		else l = mid + 1;
	}
	return res;
}
int main() {
	int t; cin >> t;
	while (t--) {
		int n, m; cin >> n >> m;
		int M[1000000];
		ll sum=0;
		for (int i = 0; i < n; i++) {
			cin >> M[i];
			sum += M[i];
		}
		cout << Min_max(M, n, m, sum) << endl;
	}
}
