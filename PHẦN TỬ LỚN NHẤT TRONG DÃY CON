#include<iostream>
#include<set>
#include<vector>
using namespace std;
typedef long long ll;
int main() {
	int t; cin >> t;
	while (t--) {
		int n, k; cin >> n >> k;
		vector<ll> M(n);
		multiset<ll> d;
		for (int i = 0; i < n; i++)cin >> M[i];
		for (int i = 0; i < k; i++)d.insert(M[i]);
		cout << *d.rbegin() << " ";
		for (int i = k; i < n; i++) {
			d.erase(d.find(M[i-k]));
			d.insert(M[i]);
			cout << *d.rbegin() << " ";
		}
		cout << endl;
	}
}
