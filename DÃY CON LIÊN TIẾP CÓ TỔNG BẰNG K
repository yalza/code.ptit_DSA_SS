#include<iostream>
#include<set>
using namespace std;
typedef long long ll;
string test(ll* M, ll n,ll k) {
	if (k == 0)return "NO\n";
	set<ll> d;
	for (int i = 0; i < n; i++)d.insert(M[i]);
	int z = d.size();
	d.insert(k);
	if (d.size() == z)return "YES\n";
	else d.erase(k);
	for (int i = 0; i < n; i++) {
		ll x = M[i] + k;
		d.insert(x);
		if (d.size() == z)return "YES\n";
		else d.erase(x);
	}
	return "NO\n";
	 }
int main() {
	int t; cin >> t;
	while (t--) {
		ll n, k; cin >> n >> k;
		ll M[100000];
		for (int i = 0; i < n; i++)cin >> M[i];
		for (int i = 1; i < n; i++)M[i] += M[i - 1];
		cout << test(M, n, k);
	}
}
