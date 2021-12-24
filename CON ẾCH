#include<iostream>
using namespace std;
int cnt;

int main() {
	int t; cin >> t;
	long long int M[101] = { 0 };
	M[0] = 1; M[1] = 2; M[2] = 4;
	for (int i = 3; i <= 100; i++)
		M[i] = M[i - 1] + M[i - 2] + M[i - 3];
	while (t--) {
		int n; cin >> n;
		cout << M[n - 1] << endl;
	}
}
