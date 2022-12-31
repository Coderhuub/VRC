#include <iostream>
#include <string.h>
using namespace std;

string VRC(string data) {
    int count = 0;
    for (char c: data) {
        if (c == '1') {
            count++;
        }
    }

    if (count % 2 == 0) {
        data.append("0");
    } else {
        data.append("1");
    }

    return data;
}

int receiver(string data) {
    int count = 0;
    for (char c: data) {
        if (c == '1') {
            count++;
        }
    }
    if (count % 2 == 0) {
        return 1;
    } else {
        return 0;
    }
}

int main() {
    string data;
    cout <<"Enter data to be transmitted: ";
    getline(cin, data);
    string Final_data = VRC(data);
    cout <<"Final data to be sent: "<< Final_data << endl;
    string rec_data;
    cout <<"Enter the received data: "<< endl;
    getline(cin, rec_data);
    int result = receiver(rec_data);
    if (result == 1) {
        cout <<"NO Error detected"<< endl;
    } else {
        cout <<"Error detected"<< endl;
    }

    return 0;
}


/*
OUTPUT SCREEN : 
Enter data to be transmitted: 100101
Final data to be sent: 1001011
Enter the received data:      
1001010
Error detected
*/
