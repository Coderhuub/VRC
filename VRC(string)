#include <iostream>
#include <string.h>
#include <math.h>

using namespace std;

int Decimal_Binary(char p){
    int n=int(p);
    int ans=0,bit,i=0;
    while(n!=0){
        bit=n&1;
        ans=(bit*pow(10,i))+ans;
        n=n>>1;
        i++;
    }
    return ans;
}

void VRC(int* arr, int size) {
    for (int i = 0; i < size; i++) {
        string data = to_string(arr[i]);
        int count = 0;
        for (char c : data) {
            if (c == '1') {
                count++;
            }
        }
        if (count % 2 == 0) {
            data.append("0");
        } else {
            data.append("1");
        }
        int n = stoi(data);
        arr[i] = n;
    
}}


void receiver(int *arr,int num_frames) {
    int flag=0;
    for(int i=0;i<num_frames;i++){
        string rec_data=to_string(arr[i]);
        int count =0;
        for(char c: rec_data){
        if(c=='1'){
            count++;
        }  }

        if (count%2!=0) {
            cout<<"Error Detected in frame: "<<i+1<<endl;
            flag++;}
}

if(flag==0){
cout<<"NO Error detected"<<endl;}

}

int main() {

    string data;
    cout << "Enter data to be transmitted: ";
    getline(cin, data);
    int size = data.size();
    int arr[size];
    for (int i = 0; i < size; i++) {
        arr[i] = Decimal_Binary(data[i]);
    }

    cout<<"Final data to be sent: "<<endl;
    VRC(&arr[0], size);
    for (int j = 0; j < size; j++) {
        cout<<"Frame"<<j+1<<": "<<arr[j]<<endl;
    }

    cout<<endl;

    int num_frames;
    cout<<"Enter the number of frames received: ";
    cin>>num_frames;

    int arr2[num_frames]; 
    cout<<"Enter the received data:" << endl;
    for (int k = 0; k < num_frames; k++) {
        cin>>arr2[k];
    }
cout<<endl;
    receiver(&arr2[0],num_frames);

    
    return 0;
}


/*

OUTPUT SCREEN:
Enter data to be transmitted: HELLO
Final data to be sent: 
Frame1: 10010000
Frame2: 10001011
Frame3: 10011001
Frame4: 10011001
Frame5: 10011111

Enter the number of frames received: 5
Enter the received data:
100010000
10001010
10011001
10011000
10011111
Error Detected in frame: 2
Error Detected in frame: 4

*/
