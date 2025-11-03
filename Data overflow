# Data overflow
关于数据溢出，再斐波那契数列运算时，当计算第114514个数据时，数据已经溢出，所以要及时对其取模，每计算一次就做取模处理。
      #include<iostream>
      #include<vector>
      using namespace std;

      const long long MOD = 998244353;

int main() {
    long long n;
    cin >> n;
    
    if (n == 1 || n == 2) {
        cout << 1 << endl;
        return 0;
    }
    
    // 动态分配大小，避免固定大小限制
    vector<long long> dp(n);
    dp[0] = 1;  // 第1个月
    dp[1] = 1;  // 第2个月
    
    for (long long i = 2; i < n; i++) {
        dp[i] = (dp[i - 1] + dp[i - 2]) % MOD;  // 及时取模
    }
    
    cout << dp[n - 1] << endl;
    return 0;
}

