#include<iostream>
#include<string>
#include<algorithm>
#include<vector>
using namespace std;
int M[257][50000];
int a, b, c, d;
bool Ktra() {
	for (int i = 1; i < 257; i++) {
		
		if (M[i][b] - M[i][a - 1] != M[i][d] - M[i][c - 1])
			return false;
	}
	return true;
}

int main() {
	string s; cin >> s;
	for (int i = 0; i < 257; i++) {
		for (int j = 0; j < s.length(); j++)
			M[i][j] = 0;
	}
	for (int i = 0; i < s.length(); i++) {
		M[s[i]][i] = 1;
	}
	for (int i = 1; i < 257; i++) {
		for (int j = 1; j <= s.length(); j++) {
			M[i][j] += M[i][j-1];
		}
	}
	int t; cin >> t;
	while (t--) {
		cin >> a >> b >> c >> d;
		a--; b--; c--; d--;
		if (Ktra())cout << "YES\n";
		else cout << "NO\n";
	}
}
