#include<iostream>
#include <string>
#include <cmath>
#define ll long long int 
using namespace std;
int main() {
    int z;cin >> z;
    while(z--){
        int n;cin >> n;
        n-=2;
        if(n<0) {
            cout<<"9\n";
            continue;
        }
        int a = 10;
        int tg = 1;
        while (n>0) {
            if (tg == 10) tg = 1;
            int c=to_string(a+1).size()-1;
            if(to_string(a).size()==c) {
                a++;
                n--;
            }
            int b = pow(10,c)-a%10;
            b -= b % tg;
            if (b + a%10== pow(10, c) || b + a%10+1== pow(10,c)) {
                if(tg==1) b-=2;
                else b-=tg;
                
            }
            if(n<=b/tg) {
                a+=n*tg;
                break;
            }
            a+=b+tg+1;
            if(to_string(a).size()==c+2) a-=a%10+1;
            n-=b/tg+1;
            tg++;
        }
        cout<<a<<"\n";
    }
}
