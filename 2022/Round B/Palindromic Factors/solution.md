```cpp
#include <bits/stdc++.h>
using namespace std;
using ll = long long;

bool isPalindrome(ll n) {
    string s = to_string(n);
    int i = 0, j = s.size() - 1;
    while (i < j) {
        if (s[i ++] != s[j --]) return false;
    }
    return true;
}

int main () {
    int T; cin >> T; 
    for (int t = 1; t <= T; t ++) {
        ll n; cin >> n;
        int res = 0;
        for (ll i = 1; i <= n / i; i ++) {
            if (n % i == 0) {
                if (isPalindrome(i)) res ++;
                if (n / i != i && isPalindrome(n / i)) res ++;
            }
        }
        printf("Case #%d: %d\n", t, res);
    }
    return 0;
}
```

