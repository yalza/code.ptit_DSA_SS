#include<iostream>
using namespace std;

int main() {
	int n; cin >> n;
	int M[100000];
	for (int i = 0; i < n; i++)cin >> M[i];
	int minnn = M[n - 1];
	int res = M[n - 2] - M[n - 1];
	for (int i = n - 1; i >= 0; i--) {
		res = max(res, M[i] - minnn);
		minnn = min(minnn, M[i]);
	}
	cout << res << endl;
}
