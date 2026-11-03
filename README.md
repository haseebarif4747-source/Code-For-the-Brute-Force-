# Code-For-the-Brute-Force-
Here You Will see the Scripted Code that is used in the video for the Lab 6 Broken Brute Force PRotection , IP Block which in Language C++ as Writtened.
-------------------------------------------------------------------------------------------------------------------------------
First make the File passwords.txt where the passwords for the User CARLOS has been written in the Lab Section about 150 then make it and see it as they are executed and Solve the Lab of your Own.

#include <iostream>
#include <fstream>
#include <string>
using namespace std;

int main() {
    cout << "############ The following are the usernames: ############"
         << endl;

    for (int i = 0; i < 150; i++) {
        if (i % 3) {
            cout << "carlos" << endl;
        } else {
            cout << "wiener" << endl;
        }
    }

    cout << "\n############ The following are the passwords: ############"
         << endl;

    ifstream file("passwords.txt");

    if (!file.is_open()) {
        cout << "Error: passwords.txt file nahi mili!" << endl;
        return 1;
    }

    string pwd;
    int i = 0;

    while (getline(file, pwd)) {
        if (i % 3) {
            cout << pwd << endl;
        } else {
            cout << "peter" << endl;
            cout << pwd << endl;
            i = i + 1;
        }

        i = i + 1;
    }

    file.close();

    return 0;
}
