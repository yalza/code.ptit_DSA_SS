#include<iostream>
#include<algorithm>
#include<vector>

using namespace std;
int main() {
	int n, k; cin >> n >> k;
	vector<int> M(n);
	for (int i = 0; i < n; i++)cin >> M[i];
	sort(M.begin(), M.end());
	int count = 0;
	for (int i = 0; i < n - 1; i++)
		if (M[i + 1] - M[i] > k)count++;
	cout << count +1<< endl;
}
