#include<iostream>
#include<string.h>
using namespace std;
int Stn(string s, int n) {
	int res = 0;
	for (int i = 1; i < n; i++) {
		int l = i - 1, r = i + 1;
		int x = 1;
		while (l >= 0 && r < n) {
			if (s[l] == s[r]) {
				x += 2;
				l--; r++;
			}
			else break;
		}
		res = max(res, x);
	}
	for (int i = 0; i < n; i++) {
		int l = i, r = i + 1;
		int x = 0;
		while (l >= 0 && r < n) {
			if (s[l] == s[r]) {
				x += 2;
				l--; r++;
			}
			else break;
		}
		res = max(res, x);
	}
	return res;
}
int main() {
	int t; cin >> t;
	while (t--) {
		string s; cin >> s;
		cout << Stn(s, s.length()) << endl;
	}
}
