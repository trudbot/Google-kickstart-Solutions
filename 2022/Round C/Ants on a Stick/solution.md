```cpp
#include <bits/stdc++.h>
using namespace std;
using pii = pair<int, int>;

int main () {
    int T; cin >> T;
    for (int t = 1; t <= T; t ++) {
        int N, L; cin >> N >> L;
        vector<pii> P;
        vector<pii> D;
        for (int i = 1; i <= N; i ++) {
            int x, y, z; cin >> x >> y;
            z = (y == 0 ? x : L - x);
            P.push_back({x, i}), D.push_back({z, y});
        }
        sort(P.begin(), P.end());
        sort(D.begin(), D.end());
        vector<pii> res;
        int l = 0, r = N - 1;
        for (auto &[dist, dire] : D) {
            if (dire == 0) res.push_back({dist, P[l ++].second});
            else res.push_back({dist, P[r --].second});
        } 
        sort(res.begin(), res.end());
        cout << "Case #" << t << ": ";
        for (auto &[dist, id] : res) {
            cout << id << " ";
        }
        cout << endl;
    }
    return 0;
}
```

