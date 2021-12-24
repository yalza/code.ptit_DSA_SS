#include<iostream>
#include<vector>
#include<stack>
using namespace std;
bool chuaxet[1005];
int truoc[1005];
void init(int v) {
	for (int i = 1; i <= v; i++)chuaxet[i] = true;
}
void dfs(int dau, vector<vector<int>>ke) {
	stack<int>st;
	st.push(dau);
	chuaxet[dau] = false;
	truoc[dau] = dau;
	while (!st.empty()) {
		int s = st.top(); st.pop();
		for (int i = 0; i < ke[s].size(); i++) {
			if (chuaxet[ke[s][i]] == true) {
				st.push(s);
				st.push(ke[s][i]);
				chuaxet[ke[s][i]] = false;
				truoc[ke[s][i]] = s;
				break;
			}
		}
	}
}
void duongdi(int dau, int cuoi) {
	if (chuaxet[cuoi] == true)cout << "-1" << endl;
	else {
		stack<int>a;
		a.push(cuoi);
		int u = truoc[cuoi];
		while (u != dau) {
			a.push(u);
			u = truoc[u];
		}
		a.push(dau);
		while (!a.empty()) {
			cout << a.top() << " ";
			a.pop();
		}
		cout << endl;
	}
}
int main() {
	ios_base::sync_with_stdio(0); cin.tie(0);
	int t; cin >> t;
	while (t--) {
		int v, e, dau, cuoi; cin >> v >> e >> dau >> cuoi;
		vector<vector<int>>ke(v + 5);
		for (int i = 1; i <= e; i++) {
			int a, b; cin >> a >> b;
			ke[a].push_back(b);
		}
		init(v);
		dfs(dau, ke);
		duongdi(dau, cuoi);
	}
}
