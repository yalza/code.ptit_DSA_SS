#include<iostream>
#include<vector>
#include<string>
#include<algorithm>
using namespace std;
vector<string> X;
int a = 0;
void Try(string s, int n) {
	if (s.length() == n) {
		X.push_back(s);
		return;
	}
	Try(s + "4", n);
	Try(s + "5", n);
}

int main() {
	int t; cin >> t;
	while (t--) {
		a = 0;
		X.clear();
		int n; cin >> n;
		for (int i = 1; i <= 14; i++)
			Try("", i);
		for (int i = 0; i < n; i++) {
			cout << X[i];
			for (int j = 0; j < X[i].length(); j++)
				cout << X[i][X[i].length() - 1 - j];
			cout << " ";
		}
		cout << endl;
	}
}
