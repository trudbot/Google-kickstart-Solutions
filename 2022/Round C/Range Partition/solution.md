```cpp
#include <bits/stdc++.h>
#define ll long long
#define vll vector<ll>
using namespace std;

vll ans;
void partition(ll N, ll A)
{
    if(A == 0) return;
    else if(N > A) partition(N-1, A);
    else ans.push_back(N), partition(N-1, A-N);
}


int main() {

    ll n, T, x, y;
    scanf("%ld", &T);
    for(ll t = 1; t <= T; t++)
    {
        printf("Case #%d: ", t);
        scanf("%ld%ld%ld", &n, &x, &y);
        ll s = n*(n+1) / 2;
        if(s % (x+y) != 0) printf("IMPOSSIBLE\n");
        else
        {
            ll A = s * x / (x+y);
            puts("POSSIBLE");
            partition(n, A);
            printf("%d\n", ans.size());
            for(ll i : ans) printf("%d ", i);
            puts("");
        }
        ans.clear();
    }

    return 0;
}
```

```cpp
#include <bits/stdc++.h>
#define ll long long
#define vll vector<ll>
using namespace std;

int main() {

    ll n, T, x, y;
    scanf("%ld", &T);
    for(ll t = 1; t <= T; t++)
    {
        printf("Case #%d: ", t);
        scanf("%ld%ld%ld", &n, &x, &y);
        ll s = n*(n+1) / 2;
        if(s % (x+y) != 0) printf("IMPOSSIBLE\n");
        else
        {
            ll A = s * x / (x+y);
            vll res;
            for(int i=n; i; i--)
                if(A >= i) A -= i, res.push_back(i);
            puts("POSSIBLE");
            printf("%d\n", res.size());
            for(ll i : res) printf("%d ", i);
            puts("");
        }
    }

    return 0;
}
```



