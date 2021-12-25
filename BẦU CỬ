#include<iostream>
#include<algorithm>
using namespace std;
struct XX {
	int a, b;
};
bool cmp(XX A, XX B) {
	return A.a < B.a;
}
int main() {
	int m, n; cin >> m >> n;
	int M[1000];
	for (int i = 0; i < m; i++)cin >> M[i];
	XX N[10];
	for (int i = 0; i < 10; i++) {
		N[i].a = 0;
		N[i].b = i;
	}
	for (int i = 0; i < m; i++)
		N[M[i]].a++;
	sort(N + 1, N + n + 1,cmp);
	int x = 0;
	int a;
	for (int i = n - 1; i >= 1; i--) {
		if (N[i].a < N[n].a) {
			x = 1; a = N[i].a;
			break;
		}
	}
	
	if (x == 0)cout << "NONE";
	else {
		int b = 0;
		for (int i = n - 1; i >= 1; i--) {
			if (N[i].a == a)b = N[i].b;
		}
		if (a == 0)cout << "NONE";
		else
		cout << b;
	}
}
