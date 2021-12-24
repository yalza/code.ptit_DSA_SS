#include<iostream>
using namespace std;

int main() {
	int t; cin >> t;
	while (t--) {
		int m, n; cin >> m >> n;
		int M[10000];
		int x = 0;
		for (int i = 1; i <= n; i++)cin >> M[i];
		for (int i = n; i > 0; i--) {
			if (M[i] != m - n + i) {
				x = 1;
				M[i]++;
				for (int j = i + 1; j <= n; j++) {
					M[j] = M[j - 1] + 1;
				}
				break;
			}
			
		}
		if (x == 0)
			for (int i = 1; i <= n; i++)cout << i << " ";
		else
			for (int i = 1; i <= n; i++)cout << M[i] << " ";
		cout << endl;
	}
}
