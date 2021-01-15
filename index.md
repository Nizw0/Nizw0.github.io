---
layout: post
title: main page
---

# test

*hello ~*
  void solve() {
    int t, n, k;
    cin >> t;
    while (t-- and cin >> n >> k) {
      int ans = 0;
      if (!n) ans = 1, n = 1;
      cout << ans + f(n, k) << '\n';
    }
  }
  int f(int n, int k) {
    if (n >= k)
      return n - k;
    if (k & 1)
      return min(f(n, k + 1), f(n, k - 1)) + 1;
    else
      return min(k - n, f(n, k / 2) + 1);
  }
