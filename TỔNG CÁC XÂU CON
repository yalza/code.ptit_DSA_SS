#include<iostream>
#include<string>
using namespace std;
long long sum(string s) {
	long long a = 0;
	for (int i = 0; i < s.length(); i++) {
		long long b = 0;
		for (int j = i; j < s.length(); j++) {
			b = b * 10 + s[j] - '0';
			a += b;
		}
	}
	return a;
}
int main() {
	int t; cin >> t;
	while (t--) {
		string s; cin >> s;
		cout << sum(s) << endl;
	}
}
