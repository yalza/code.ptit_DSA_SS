#include<iostream>
#include<string>
#include <algorithm>
using namespace std;
int load(string s[], int m, int n) {
    int resuilt = 1e8, a[n];
    for (int i = 1; i <= n; i++) a[i - 1] = i;
    while (1) {
        sort(s, s + m);
        int t = stoi(s[m - 1]) - stoi(s[0]);
        //cout<<t<<"\n";
        resuilt = min(resuilt, t);
        int k = n - 2;
        while (k >= 0 && a[k + 1] < a[k]) k--;
        if (k < 0) return resuilt;
        for (int i = n - 1; i > k; i--) {
            if (a[i] > a[k]) {
                swap(a[i], a[k]);
                reverse(a + k + 1, a + n);
                for (int j = 0; j < m; j++) swap(s[j][i], s[j][k]);
                for (int j = 0; j < m; j++) reverse(s[j].begin() + k + 1, s[j].end());
                break;
            }
        }
    }
}
int main() {
    int n, k; cin >> n >> k;
    string a[10];
    for (int i = 0; i < n; i++) cin >> a[i];
    cout <<endl<< load(a, n, k);

}
