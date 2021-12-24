#include<iostream>
#include<string>
using namespace std;
bool ok;
void test(int M[], int n, int sum, int m, string s, int j) {
	for (int i = j; i < n; i++) {
		if (sum == m) {
			ok = true;
			s.pop_back();
			cout << "[" << s << "]";
			return;
		}
		else if (sum > m)return;
		else test(M, n, sum + M[i], m, s + to_string(M[i])+" ", i);
	}
}

int main() {
	int t; cin >> t;
	while (t--) {
		int n, x; cin >> n >> x;
		ok = false;
		int M[20];
		for (int i = 0; i < n; i++)cin >> M[i];
		test(M, n, 0, x, "", 0);
		if (!ok)cout << -1;
		cout << endl;
	}
}
