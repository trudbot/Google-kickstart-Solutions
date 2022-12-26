```cpp
#include <bits/stdc++.h>
using namespace std;
using ll = long long;
const double pi = 3.141592653;

int main() {
    int T; cin >> T;
    for(int t = 1; t<=T; t++)
    {
        ll r, a, b; cin >> r >> a >> b;
        ll ans = r * r;
        while(r > 0)
        {
            r *= a;
            ans += r*r;
            r /= b;
            ans += r*r;
        }

        printf("Case #%d: %lf\n", t, pi * ans);
    }

    return 0;
}
```

