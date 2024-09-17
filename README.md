//# Row-and-Column-Sum
#include<iostream>
using namespace std;
void print(int a[][3],int rownumber,int colnumber){
    cout<<"Array : "<<endl;
    for(int i=0;i<rownumber;i++){
        for(int j=0;j<colnumber;j++){
            cout<<a[i][j]<<" ";
        }
        cout<<endl;
    }
}
void row_sum(int a[][3],int rownumber,int colnumber){
    for(int i=0;i<rownumber;i++){
        int sum = 0;
        for(int j=0;j<colnumber;j++){
            sum = sum + a[i][j];
        }
        cout<<"Sum of row "<<i<<" : "<<sum<<endl;
    }
}
void col_sum(int a[][3],int rownumber,int colnumber){
    int i,j;
    for(j=0;j<colnumber;j++){
        int sum = 0;
        for(i=0;i<rownumber;i++){
            sum = sum + a[i][j];
        }
        cout<<"Sum of column "<<i<<" : "<<sum<<endl;
    }
}
int main(){
    int a[3][3];
    int rownumber = 3;
    int colnumber = 3;
    int i,j;
    cout<<"Enter Array Element"<<endl;
    for(i=0;i<rownumber;i++){
        for(j=0;j<colnumber;j++){
            cin>>a[i][j];
        }
    }
    print(a,rownumber,colnumber);
    // row_sum(a,rownumber,colnumber);
    col_sum(a,rownumber,colnumber);
}
