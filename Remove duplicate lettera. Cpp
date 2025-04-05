#include <iostream>
#include <stack>
#include <unordered_map>
#include <unordered_set>
using namespace std;

string removeDuplicateLetters(string s) {
    stack<char> stk;
    unordered_set<char> seen;
    unordered_map<char, int> count;

    for (char c : s) count[c]++;

    for (char c : s) {
        count[c]--;
        if (seen.count(c)) continue;

        while (!stk.empty() && stk.top() > c && count[stk.top()] > 0) {
            seen.erase(stk.top());
            stk.pop();
        }

        stk.push(c);
        seen.insert(c);
    }

    string result;
    while (!stk.empty()) {
        result = stk.top() + result;
        stk.pop();
    }
    return result;
}

int main() {
    string s = "bcabc";
    cout << "Result: " << removeDuplicateLetters(s) << endl;
    return 0;
}
