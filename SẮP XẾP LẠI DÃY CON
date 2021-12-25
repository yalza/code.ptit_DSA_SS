#include<iostream>
using namespace std;
int main() {
	int t; cin >> t;
	while (t--) {
		int n; cin >> n;
		int M[1000];
		for (int i = 0; i < n; i++)cin >> M[i];
		int i = 0,j=n-1;
		while (M[i + 1] >= M[i])i++;
		while (M[j - 1] <= M[j])j--;
		int minn = 100000, maxx = 0;
		for (int l = i; l <= j; l++) {
			minn = min(minn, M[l]);
			maxx = max(maxx, M[l]);
		}
		int a = i, b = j;
		for (int l = i; l >= 0; l--) {
			if (M[l] > minn)a = l;
		}
		for (int l = j; l < n; l++) {
			if (M[l] < maxx)b = l;
		}
		cout << a + 1 << " " << b + 1 << endl;
	}
}
