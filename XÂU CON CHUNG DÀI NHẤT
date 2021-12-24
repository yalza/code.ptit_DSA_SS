#include<iostream>
#include <cstring>
using namespace std;
int main() {
	int t; cin >> t;
	while (t--) {
		string a, b; cin >> a >> b;
		int M[1000][1000];
		memset(M, 0, sizeof(M));
		int res = 0;
		for (int i = 1; i <= a.length(); i++) {
			for (int j = 1; j <= b.length(); j++) {
				if (a[i - 1] == b[j - 1])M[i][j] = M[i - 1][j - 1] + 1;
				else
				M[i][j] = max(M[i - 1][j], M[i][j - 1]);
				res = max(res, M[i][j]);
			}
		}
		cout << res << endl;
	}
}
