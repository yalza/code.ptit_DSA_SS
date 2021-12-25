#include<iostream>
#include<string>
#include<stack>
using namespace std;
string test(string a)
{
    string u = "";
    for (int i = 0; i < a.length(); i++) {
        if (a[i] == '(' || a[i] == ')' || a[i] == ']' || a[i] == '[')
            u += a[i];
    }
    a = u;
    int b = 0;
    while (1) {
        int x = a.find("()");
        int y = a.find("[]");
        if (x == -1 && y == -1)
            break;
        if (x != -1) {
            a.erase(x, 2);
            b += 2;
        }
        else if (y != -1) {
            a.erase(y, 2);
            b += 2;
        }
    }
    if (b != u.length()) {
        return "NO\n";
    }
    return "YES\n";
}
int main() {
    int t; cin >> t;
    cin.ignore();
    while (t--) {
        string s; getline(cin, s);
        cout << test(s);
    }
}
