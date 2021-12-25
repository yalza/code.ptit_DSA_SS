#include <bits/stdc++.h>
using namespace std;
void sub_x(string a, int b, string& s) {
    int tg = 0;
    for (int i = 0; i < a.size(); i++) {
        s.push_back(((a[i] - '0') * b + tg) % 10 + '0');
        tg = ((a[i] - '0') * b + tg) / 10;
    }
    if (tg) s.push_back(tg + '0');
}
void sum(string& a, string b, int n) {
    int tg = 0, zz;
    int z = n + b.size() - a.size();
    for (int i = 0; i < z; i++) a.push_back('0');
    for (int i = 0; i < b.size(); i++) {
        zz = a[i + n] - '0';
        a[i + n] = (zz - '0' + b[i] + tg) % 10 + '0';
        tg = (zz - '0' + b[i] + tg) / 10;
    }
    if (tg) a.push_back(tg + '0');
}
void xxx(string& a, string b) {
    int s[10] = {};
    vector<string> z(10);
    for (int i = 0; i < b.size(); i++) s[b[i] - '0'] = 1;
    for (int i = 0; i < 10; i++) if (s[i]) sub_x(a, i, z[i]);
    for (int i = 0; i < a.size(); i++) a[i] = '0';
    for (int i = 0; i < b.size(); i++) if (b[i] != '0') sum(a, z[b[i] - '0'], i);
}
void n_to_string(long long int n, string& s) {
    while (n) {
        s.push_back(n % 10 + '0');
        n /= 10;
    }
}
void divi(long long int& x, map<int, int>& check) {
    for (auto i = check.begin(); i != check.end(); i++) {
        if (i->first > 0) {
            while (x % i->first == 0 && i->second > 0) {
                x /= i->first;
                i->second--;
            }
        }
    }
}
string cata(short n) {
    int dem = 0;
    if (n <= 1) return "1";
    map <int, int> check;
    for (int i = 2; i <= (n + 1) / 2; i++) {
        int tg = i;
        for (int j = 2; j <= i / j; j++) {
            if (i % j == 0) {
                int dem = 0;
                while (tg % j == 0) {
                    tg /= j;
                    dem++;
                }
                check[j] += dem;
            }
        }
        if (tg - 1) check[tg]++;
    }
    vector <int> nn(2 * n + 20, 1);
    for (int i = n + 2; i <= 2 * n; i++) nn[i] = i;
    long long int x = 1;
    vector<string> sub_cata(n);
    int c = n - 1;
    for (int i = n + 2; i <= 2 * n;) {
        for (int j = 0; j < 6; j++) {
            if (nn[i] % 2) x *= nn[i]; else x *= 2;
            i++;
        }
        divi(x, check);
        n_to_string(x, sub_cata[dem++]);
        x = 1;
    }

    string total = sub_cata[0];
    for (int i = 1; i < dem; i++) xxx(total, sub_cata[i]);
    reverse(total.begin(), total.end());
    return total;
}
int main() {
    int t; cin >> t;
    while (t--) {
        short n; cin >> n;
        cout << cata(n)<<endl;
    }
}
