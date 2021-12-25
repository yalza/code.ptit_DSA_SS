#include<iostream>
#include<vector>
#include<stack>
#include<algorithm>
using namespace std;
struct XXX {
	string cha, con;
	int tuoi;
};
int n;
vector<pair<string, int>> X;
void Try(string s, int x, vector<XXX> M) {
	X.push_back({ s, x });
	int a = 0;
	for (int i = 0; i < n; i++) {
		if (s == M[i].cha) {
			Try(M[i].con, x - M[i].tuoi,M);
			a++;
		}
	}
	if (a == 0)return;
}
bool cmp(pair<string, int> A, pair<string, int> B) {
	if (A.second == B.second)return A.first < B.first;
	return A.second > B.second;
}
int main() {
	int t; cin >> t;
	for(int j=1;j<=t;j++){
		cin >> n;
		X.clear();
		vector<XXX> M(n);
		for (int i = 0; i < n; i++) {
			cin >> M[i].cha >> M[i].con >> M[i].tuoi;
		}
		Try("Ted", 100,M);
		sort(X.begin(), X.end(), cmp);
		cout << "DATASET " << j << endl;
		for (int i = 1; i < X.size(); i++) {
			cout << X[i].first << " " << X[i].second << endl;
		}
	}
}
