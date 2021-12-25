#include<iostream>
#include<algorithm>
#include<vector>
#include<math.h>
#include<map>
using namespace std;

int main() {
	int  n, m; cin >> n>> m;
	int y1, y2; cin >> y1 >> y2;
	int N[500000], M[500000];
	for (int i = 0; i < n; i++)cin >> N[i];
	for (int i = 0; i < m; i++)cin >> M[i];
	sort(N, N+n);
	sort(M, M+m);
	int y = abs(y1 - y2);
	vector<int> A,B;
	for (int i = 0; i < n; i++) {
		int z = lower_bound(M, M+m, N[i]) - M;
		if(z>=0)
		A.push_back(abs(M[z] - N[i]));
	}
	for (int i = 0; i < m; i++) {
		int z = upper_bound(N, N + n, M[i]) - N;
		if (z >= 0)
			B.push_back(abs(N[z] - M[i]));
	}
	sort(A.begin(), A.end());
	sort(B.begin(), B.end());
	int v = min(A[0], B[0]);
	int count = 0;
	for (int i = 0; i < A.size(); i++) {
		if (v == A[i])count++;
		else break;
	}
	for (int i = 0; i < B.size(); i++) {
		if (v == B[i])count++;
		else break;
	}
	cout << v+y << " " << count;
}
