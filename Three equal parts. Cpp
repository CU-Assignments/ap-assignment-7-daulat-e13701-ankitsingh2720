#include <iostream>
#include <vector>
using namespace std;

vector<int> threeEqualParts(vector<int>& arr) {
    vector<int> ones;
    for (size_t i = 0; i < arr.size(); i++) {
        if (arr[i] == 1) ones.push_back(i);
    }

    int totalOnes = ones.size();
    if (totalOnes % 3 != 0) return {-1, -1};
    if (totalOnes == 0) return {0, (int)arr.size() - 1};

    int partSize = totalOnes / 3;
    int first = ones[0], second = ones[partSize], third = ones[2 * partSize];

    while (third < arr.size() && arr[first] == arr[second] && arr[second] == arr[third]) {
        first++, second++, third++;
    }

    if (third == arr.size()) return {first - 1, second};
    return {-1, -1};
}

int main() {
    vector<int> arr = {1, 0, 1, 0, 1};
    vector<int> result = threeEqualParts(arr);
    cout << "Three Equal Parts Indices: [" << result[0] << ", " << result[1] << "]" << endl;
    return 0;
}
