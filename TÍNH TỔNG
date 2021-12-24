#include <iostream>
#include <string>
using namespace std;
int main() {
	string a;
	int k, n, mod,tg=0,z=1;
	cin >> a >> k >> n >> mod;
	for (int i = 0;i < k;i++) {
		tg = (tg * n + a[i] - '0') % mod;
		z = (z * n) % mod;
	}
	int sum = tg;
	for (int i = k;i < a.size();i++) {
		int p = a[i - k] - '0';
		tg = (((tg * n + a[i]-'0') % mod - z * p % mod) % mod + mod) % mod;
		sum += tg;
	}
	cout << sum;
}
