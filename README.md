#include <iostream>
#include <string>
#include <vector>
#include <utility>
#include <cmath>
#include <cstdlib>
#include <algorithm>
using namespace std;

class Character {
private:
    string name;
    double health;
    int level;

public:
    Character(string n, double h, int l) {
        name = n;
        health = h;
        level = l;
    }

    double TakeD(double amount) { // Fixed method definition
        cout << "The damage is: " << amount << endl;
        health -= amount; // Update health
        return health;
    }

    int levelUp() {
        level++; // Increment level
        cout << "Level up! New level: " << level << endl;
        return level;
    }

    void GetStatus() {
        cout << "\tName: " << name << endl;
        cout << "\tHealth: " << health << endl;
        cout << "\tLevel: " << level << endl;
    }
};

int main() {
    Character player1("Ali", 100.0, 20);
    player1.GetStatus();
    player1.TakeD(29.99);
    player1.levelUp();
    player1.GetStatus();
}
