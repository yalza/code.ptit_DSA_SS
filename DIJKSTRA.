#include<bits/stdc++.h>
using namespace std;
typedef pair<int, int> ii;
vector<ii> a[1005];
int n, m,start;
priority_queue<ii, vector<ii>, greater<ii> > pq;
int d[1005];
void dijkstra(int st) { 
    int u,v;
    for (int i = 1; i <= n; i++) d[i] = 1e9;
    d[st] = 0;
   // while(!pq.empty()) pq.pop();
        pq.push(ii(0, st));

    while (!pq.empty()) {
         u = pq.top().second;pq.pop();
        for (int i = 0; i < a[u].size(); i++) {
             v = a[u][i].second;
            int uv = a[u][i].first;
            if (d[v] > d[u] + uv) {
                d[v] = d[u] + uv;
                pq.push(ii(d[v], v));
            }
        }
    }
    for(int i=1;i<=n;i++) cout<<d[i]<<" ";
    cout<<endl;
}
int main() {
	int t;cin>>t;
	while(t--)
	{
	int u,v,k;
    cin>>n>>m>>start;
    for(int i=0;i<=n;i++) a[i].clear(); 
    while (m--) {
        cin>>u>>v>>k;
        a[u].push_back(ii(k, v));
        a[v].push_back(ii(k, u));
    }
    dijkstra(start);
    
	}  
}
