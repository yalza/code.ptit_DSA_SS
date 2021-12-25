#include<iostream>
#include<stack>
#include<string>
using namespace std;
int xxx(string s){
	int res = 0;
	int m = 0;
	for (int i = 0; i < s.length(); i++) {
		if (s[i] == '(') {
			m++;
			res = max(res, m);
		}
		else if (s[i] == ')') {
			if (m > 0)m--;
			else return -1;
		}
	}
	if (m != 0)return -1;
	return res;
}
int main() {
	int t; cin >> t;
	cin.ignore();
	while (t--) {
		string s; getline(cin, s);
		cout << xxx(s) << endl;
	}
}
