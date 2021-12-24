#include<iostream>
#include<string>
#include<set>
#include<vector>
#include<algorithm>
using namespace std;

int main() {
	int t; cin >> t;
	while (t--) {
		int k; cin >> k;
		string s; cin >> s;
		vector<int> M(1000,0);
		vector<int> N;
		for (int i = 0; i < s.length(); i++)
			M[s[i]]++;
		for (int i = 0; i <= 100; i++) {
			if (M[i] > 0)N.push_back(M[i]);
		}
		int n = N.size();
		sort(N.begin(), N.end());
		while (k--) {
			N[n - 1]--;
			sort(N.begin(), N.end());
		}
		long long sum = 0;
		for (int i = 0; i < n; i++)sum += (long long )N[i] * N[i];
		cout << sum << endl;
	}
}
