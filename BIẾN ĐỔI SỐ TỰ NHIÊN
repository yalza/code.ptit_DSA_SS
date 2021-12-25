#include<iostream>
#include<math.h>
#include<set>
#include<queue>
using namespace std;
int xxx(int n) {
	set<int> X;
	queue<pair<int,int>> Y;
	X.insert(n);
	Y.push({ n,0 });
	while (Y.size()) {
		pair<int, int> x = Y.front();
		Y.pop();
		if (x.first == 1)return x.second;
		if (x.first == 2)return x.second + 1;
		if (X.count(x.first - 1) == 0)
		{
			Y.push({ x.first - 1,x.second + 1 });
			X.insert(x.first - 1);
		}
		for (int i = 2; i * i <= x.first; i++) {
			if (x.first % i == 0&&X.count(x.first/i)==0) {
				Y.push({ x.first / i,x.second + 1 });
				X.insert(n / i);
			}
		}
	}
}
int main() {
	int t; cin >> t;
	while (t--) {
		int a = 0;
		int n; cin >> n;
		cout << xxx(n) << endl;
	}
}
