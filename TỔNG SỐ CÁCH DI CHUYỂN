#include<iostream>
using namespace std;
#define mod 1000000007
int main() {
	int t; cin >> t;
	while (t--) {
		int n, k; cin >> n >> k;
		int M[1000000] = { 0 };
		M[0] = 1;
		M[1] = 1;
		for (int i = 2; i <= n; i++) {
			for (int j = 1; j <= min(i, k); j++) {
				M[i] += M[i-j];
				M[i] %= mod;
			}
		}
		cout << M[n] << endl;
	}
}
