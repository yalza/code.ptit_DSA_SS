#include<iostream>
using namespace std;
int n; string s;
char DH='B';
int a = 0;
void Robot(int i, int x,int y) {
	if (i == n) {
		if(a==0)
		cout << x << " " << y << endl;
		a++;
		return;
	}
	if (DH == 'B') {
		if (s[i] == 'G') {
			DH = 'B';
			Robot(i + 1, x, y + 1);
		}
		if (s[i] == 'B'){
			DH = 'N';
			Robot(i + 1, x, y - 1);
		}
		if (s[i] == 'L') {
			DH = 'T';
			Robot(i + 1, x - 1, y);
		}
		if (s[i] == 'R') {
			DH = 'D';
			Robot(i + 1, x + 1, y);
		}
	}
	if (DH == 'N') {
		if (s[i] == 'G') {
			DH = 'N';
			Robot(i + 1, x, y - 1);
		}
		if (s[i] == 'B') {
			DH = 'B';
			Robot(i + 1, x, y + 1);
		}
		if (s[i] == 'L') {
			DH = 'D';
			Robot(i + 1, x + 1, y);
		}
		if (s[i] == 'R') {
			DH = 'T';
			Robot(i + 1, x - 1, y);
		}
	}
	if (DH == 'T') {
		if (s[i] == 'G') {
			DH = 'T';
			Robot(i + 1, x-1, y);
		}
		if (s[i] == 'B') {
			DH = 'D';
			Robot(i + 1, x+1, y);
		}
		if (s[i] == 'L') {
			DH = 'N';
			Robot(i + 1, x , y-1);
		}
		if (s[i] == 'R') {
			DH = 'B';
			Robot(i + 1, x, y+1);
		}
	}
	if (DH == 'D') {
		if (s[i] == 'G') {
			DH = 'D';
			Robot(i + 1, x+1, y);
		}
		if (s[i] == 'B') {
			DH = 'T';
			Robot(i + 1, x-1, y);
		}
		if (s[i] == 'L') {
			DH = 'B';
			Robot(i + 1, x, y+1);
		}
		if (s[i] == 'R') {
			DH = 'N';
			Robot(i + 1, x , y-1);
		}
	}
}
int main()
{
	cin >> n >> s;
	Robot(0, 0, 0);
}
