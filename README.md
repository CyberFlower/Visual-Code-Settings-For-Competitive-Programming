### Visual Code Settings For Competitive Programming
---

I will share my visual code settings, which design for Competitive Programming(Codeforces, Baekjoon OJ, Kattis, etc...)

You can get output by following simple steps.

1. Copy-paste input data to input.txt
2. Run Task(Generally, CTRL+Shift+B)
3. Output and debug logs will be print on output.txt

You can save your time during CP, because you don't need to copy paste input data many times.

This settings allow C, C++, and Python3.

![Screenshot](./Screenshot.png)

Make sure that .cpp(or .py) files and input.txt, output.txt files needs to be same location.

---

### Windows OS

You need to install some packages.

1. Git Bash

    * I try a lot of terminals(WSL, etc...), but only Git Bash working well without any path error.

2. MinGW(gcc,g++)
You need to edit Windows system path after install gcc, g++. 

    * [Visual Studio Code Docs](https://code.visualstudio.com/docs/cpp/config-mingw)
    * [Git Bash install gcc](https://yichaoou.github.io/tutorials/software/2016/06/28/git-bash-install-gcc)

Following sites will be helpful to you.

3. Python3

    * [Download Python3](https://www.python.org/downloads/)

4. bits/stdc++.h

    * You can add bits/stdc++.h if you want. (C++ header)
    * [How to include bits/stdc++.h](https://codeforces.com/blog/entry/73240)
    * [Someone's Github, not origin](https://github.com/tekfyl/bits-stdc-.h-for-mac/blob/master/stdc%2B%2B.h)

---

### MAC OS

---

Setting Visual Code in MAC OS, or Ubuntu is much easier than Windows OS. Just copy-paste "tasks.json" and install packages in Visual Code Extensions.

---

### Template

---

Template also helps to save time during contest. I will also share my C++ template that my faculty senior [@SoulTch](http://codeforces.com/profile/SoulTch) gives to me.

Template Code

```cpp
#include <bits/stdc++.h>

using namespace std;

#ifndef __OnlineJudge
#define debug(...) 0
#else
#define debug(...) cout << " [-] ", _dbg(#__VA_ARGS__, __VA_ARGS__)
template<class TH> void _dbg(const char *sdbg, TH h){ cout << sdbg << '=' << h << endl; }
template<class TH, class... TA> void _dbg(const char *sdbg, TH h, TA... a) {
    while(*sdbg != ',') cout << *sdbg++;
    cout << '=' << (h) << ',';
    _dbg(sdbg+1, a...);
}
#endif

#define TYPEMAX(type)   numeric_limits<type>::max()
#define TYPEMIN(type)   numeric_limits<type>::min()
typedef long long ll;
typedef pair<int,int> pii;
typedef pair<ll,ll> pll;
typedef vector<int> vi;
typedef vector<ll> vl;

int main(void){
    ios_base::sync_with_stdio(false); cin.tie(NULL);

    return 0;
}
```

Example usage.

```cpp
int main(void){
    int x=3;
    // print x=3
    // print x just in local. (Not OJ system.)    
    debug(x);

    // print 3
    // print x both local and OJ system.
    cout>>x;
    return 0;
}
```