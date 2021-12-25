#include <bits/stdc++.h>
using namespace std;
int n,k;
int a[2][100]={};
int dem=0;
long long int sum=0;
void load(int z) {
    for(int i=1;i>=0;i--) {
        dem+=i;
        sum+=a[i][z];
        if(sum==k) {
            cout<<dem;
            exit(0);
        }
        if(sum<k && z<n-1) load(z+1);
        sum-=a[i][z];
        dem-=i;
    }
}
int main() {
    cin>>n>>k;
    for(int i=0;i<n;i++) cin>>a[1][i];
    sort(a[1],a[1]+n,greater<int>());
    load(0);
    cout<<-1;
}
