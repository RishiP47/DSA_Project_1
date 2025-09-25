#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    int num[] = { 0,1,2,3,4,5,6,7,8,9 };
    int n = sizeof(num) / sizeof(num[0]);
    srand(time(0));

    bool condition = true;
    while (condition) {
        cout << "\n\n====================================\n";
        cout << "               OTP Generator\n";
        cout << "====================================\n";
        cout << "1. 4-pin\n";
        cout << "2. 6-pin\n";
        cout << "3. Exit\n";
        cout << "====================================\n";
        cout << "Enter your choice(1,2,3): ";

        int choice;
        cin >> choice;

        switch (choice) {
        case 1: {
            cout << "4-pin OTP: ";
            for (int i = 0; i < 4; i++) {
                int randomIndex = rand() % n;
                cout << num[randomIndex];
            }
            cout << endl;
            break;
        }

        case 2: {
            cout << "6-pin OTP: ";
            for (int i = 0; i < 6; i++) {
                int randomIndex = rand() % n;
                cout << num[randomIndex];
            }
            cout << endl;
            break;
        }

        case 3:
            cout << "*** Exiting the program... ***\n";
            condition = false;
            break;

        default:
            cout << "*** Invalid choice! Please try again.***\n";
            break;
        }
    }

    return 0;
}
