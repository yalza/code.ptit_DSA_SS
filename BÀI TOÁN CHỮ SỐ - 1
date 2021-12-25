#include <bits/stdc++.h>
using namespace std;
#define ll long long int
ll tg[11]={};
void load(int n, int a[]) {
    if(n==0) return;
    string s=to_string(n);
    int x=s.size();
    for(int i=0;i<10;i++) a[i]+=tg[x-1];
    for(int i=0;i<x-1;i++) a[0]-=pow(10,i);
    for(int i=0;i<x;i++) {
        int j=0,p=0,sum;
        if(i==0) {
            p=1;
            j=1;
            a[0]+=tg[x-1-i]*(s[i]-'0'-p);
        }
        sum=tg[x-1-i]*(s[i]-'0'-p);
        for(;j<s[i]-'0';j++) {
            a[j]+=pow(10,x-i-1)+sum;
        }
        a[j]+=n%((int)pow(10,x-i-1))+sum+1;
        for(++j;j<10;j++) a[j]+=sum;
    }
}
int main() {
    int z;cin>>z;
    for(int i=0;i<10;i++) tg[i]=i*pow(10,i-1);
    while(z--) {
        int a,b,aa[20]={},bb[20]={};
        cin>>a>>b;
        load(a-1,aa);
        load(b,bb);
        for(int i=0;i<10;i++) cout<<bb[i]-aa[i]<<" ";
        cout<<"\n";
    }
}
