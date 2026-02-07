#include <bits/stdc++.h>
using namespace std;

void display_queue(queue<int> q) {
    while (!q.empty()) {
        cout << q.front() << " ";
        q.pop();
    }
    cout << endl;
}

int main() {
    queue<int> que;
    que.push(1);
    que.push(2);
    que.push(3);
    que.push(4);
    que.push(5);
    que.push(6);
    que.push(7);
    que.push(8);

    int n = que.size();

    for (int i = 0; i < n; i++) {
        int x = que.front();
        que.pop();

        if (i % 2 != 0) {
            que.push(x);
        }
    }

    display_queue(que);
    return 0;
}
