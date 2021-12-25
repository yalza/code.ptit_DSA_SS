#include<iostream>
#include<stack>
#include<vector>
#include<string>
using namespace std;
typedef pair<char, int> p;
int main() {
	int t; cin >> t;
	cin.ignore();
	while (t--) {
		string s;
		getline(cin, s);
		stack<p> M;
		vector<int> N;
		int x = 1;
		for (int i = 0; i < s.length(); i++) {
			if(s[i]=='(') {
				M.push({ s[i],x });
				N.push_back(x);
				x++;
				
			}
			if (s[i] == ')') {
				N.push_back(M.top().second);
				M.pop();
			}
		}
		for (int i : N)cout << i << " ";
		cout << endl;
	}
}
