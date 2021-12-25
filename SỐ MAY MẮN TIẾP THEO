#include<iostream>
#include<string>
#include<vector>
#include<algorithm>
using namespace std;
vector<long long int> M;
void test(string s) {
	if (s.length()<=9&&s.length()>0) {
			M.push_back(stoi(s));
	}
	else if(s.length()>9) return;
	test(s + "4");
	test(s + "7");
}

int main() {
	int a, b; cin >> a >> b;
	test("");
	sort(M.begin(), M.end());
	long long smm = 0;
	int x = 0,y=0;
	if (a == b) {
		int u = 0;
		for (int i = 0; i < M.size(); i++) {
			if (M[i] >= a && u == 0) {
				cout << M[i]; u++;
			}
			
		}
	}
	else if (a <= 4 && b <= 4)
		cout << (b - a + 1) * 4;
	else {
		for (int i = 0; i < M.size(); i++) {
			if (M[i] >= a && x == 0 && M[i] < b) {
				smm += M[i] * (M[i] - a + 1);
				x++;
			}
			else if (M[i] >= a && x > 0 && M[i] < b) {
				smm += M[i] * (M[i] - M[i - 1]);
			}
			if (M[i] >= b && y == 0) {
				y++;
				smm += M[i] * (b - M[i - 1]);
			}
			else if (M[i] >= b && y > 0)break;
		}

		cout << smm << endl;
	}
}
