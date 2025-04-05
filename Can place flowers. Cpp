#include <iostream>
#include <vector>
using namespace std;

bool canPlaceFlowers(vector<int>& flowerbed, int n) {
    int count = 0;
    for (size_t i = 0; i < flowerbed.size(); i++) {
        if (flowerbed[i] == 0 &&
            (i == 0 || flowerbed[i - 1] == 0) &&
            (i == flowerbed.size() - 1 || flowerbed[i + 1] == 0)) {
            flowerbed[i] = 1;
            count++;
        }
        if (count >= n) return true;
    }
    return false;
}

int main() {
    vector<int> flowerbed = {1, 0, 0, 0, 1};
    int n = 1;
    cout << "Can place flowers: " << (canPlaceFlowers(flowerbed, n) ? "True" : "False") << endl;
    return 0;
}
