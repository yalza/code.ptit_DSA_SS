#include<iostream>
#include<vector>
#include<string>
#include<algorithm>
using namespace std;
vector<long long> X;
int a = 0;
void Try(string s, int n) {
	if (s.length() == n) {
		a++;
		long long x = 0;
		for (int i = 0; i < s.length(); i++)x = x * 10 + s[i] - 48;
		X.push_back(x);
		return;
	}
	Try(s + "6", n);
	Try(s + "8", n);
}

int main() {
	int t; cin >> t;
	while (t--) {
		a = 0;
		X.clear();
		int n; cin >> n;
		for (int i = 1; i <=n; i++)
			Try("", i);
		sort(X.begin(), X.end());
		cout << a << endl;
		for (int i = a-1; i>=0; i--)cout << X[i] << " ";
		cout << endl;
	}
}
