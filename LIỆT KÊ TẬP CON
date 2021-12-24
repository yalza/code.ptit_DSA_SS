#include<iostream>
#include<string>
#include<stdbool.h>
#include<algorithm>
using namespace std;
bool f=false;
void sinh(int* M, int n) {
	int a = 0;
	for (int i = n - 1; i >= 0; i--) {
		if (M[i] == 0) {
			M[i] = 1;
			for (int j = i + 1; j < n; j++)M[j] = 0;
			a = 1;
			break;
		}
	}
	if (a == 0)f = true;
}
int main() {
	int t; cin >> t;
	while (t--) {
		int n; cin >> n;
		string s; cin >> s;
		string x[100000];
		int M[1000] = { 0 };
		M[n - 1] = 1;
		int a = 0;
		f = false;
		while (!f) {
			for (int i = 0; i < n; i++)
				if (M[i] == 1)
					x[a].push_back(s[i]);
			a++;
			sinh(M, n);
		}
		sort(x, x + a);
		for (int i = 0; i < a; i++)cout << x[i] << " ";
		cout << endl;
	}
}
