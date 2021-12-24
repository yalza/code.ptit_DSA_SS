#include<iostream>
#include<stack>
using namespace std;
int xx(int a, int b, char x) {
	if (x == '+')return a + b;
	if (x == '-')return a - b;
	if (x == '/')return a / b;
	if (x == '*')return a * b;
}
int main() {
	int t; cin >> t;
	while (t--) {
		string s; cin >> s;
		stack<int> X;
		for (int i = s.length()-1; i >= 0; i--) {
			if (s[i] >= '0' && s[i] <= '9')X.push(s[i] - 48);
			else {
				int x = X.top(); X.pop();
				int y = X.top(); X.pop();
				X.push(xx(x, y, s[i]));
			}
		}
		cout << X.top() << endl;
	}
}
