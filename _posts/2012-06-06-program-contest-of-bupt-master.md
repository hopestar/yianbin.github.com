---
layout: post
title: 北邮计算机考研复试上级题目
---

现在是等录取通知书的时候。离研究生入学复试结束已经过去一个半月了，我能有幸以307的低分被录取，觉得关键还是要重视复试，尤其是计算机上机考试。

下面分享2012年北邮计算机学院的上机题目，我做出了其中的A、B、D三题，RankList排名在33。（总人数281，四道题全部做出来的有11人。）

## A 二进制数 ##

参考代码：
    #include <iostream>
    #include <stack>
    using namespace std;
    
    int main()
    {
        unsigned int x;
        stack<int> bin;
        while (cin >> x) {
            while (x != 0) {
               int b = x % 2;
                bin.push(b);
                x = x / 2;
            }
            while (!bin.empty()) {
                cout << bin.top();
                bin.pop();
            }
            cout << endl;
        }
        return 0;
    }

## B 矩阵幂 ##

参考代码：
