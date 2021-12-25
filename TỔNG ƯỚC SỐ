#include<iostream>
#include<math.h>
using namespace std;
int main() {
	int a, b; cin >> a >> b;
	int M[1000001] = { 0 };
	for (int i = 1; i <= b; i++) {
		for (int j = 2*i; j <= b; j+=i)
			M[j] += i;
	}
	int count = 0;
	
	for (int i = a; i <= b; i++)
		if (M[i] > i)count++;
	cout << count;
}
