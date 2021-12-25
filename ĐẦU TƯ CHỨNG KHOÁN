#include<iostream>
#include<vector>
#include<stack>
using namespace std;

int main() {
	int n; cin >> n;
	while (n--) {
		int t; cin >> t;
		vector<int> M(t),N(t);
		for (int i = 0; i < t; i++) {
			cin >> M[i]; N[i] = 1;
		}
		for (int i = 1; i < t; i++) {
			for (int j = i - 1; j >= 0;) {
				if (M[j] <= M[i]) {
					N[i] += N[j];
					j -= N[j];
				}
				else break;
			}
		}
		for (int i = 0; i < t; i++)cout << N[i] << " ";
		cout << endl;
	}
}
