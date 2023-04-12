# Momo-Project-
Assignment 
include<iostream>
#include <string>
using namespace std;

int main(){
bool authenticated=false;
string pin="0000";
string password;
float balance=1000;
bool run=true;
int option;
while (run){

cout<<"enter pin or 0 to cancel"<<endl

for(int x=0;x<3;x++) {

cin >> password;

if (password==pin){
authenticated=true;
break;
} else if(password =="0"){
run=false;
break;
} else {
if (x == 2){
run = false;
break;
} else {
cout <<"try again or press 0 to exit:"<<endl;
}
} 
}

if (authenticated){
cout<<"1.reset pin"<<endl;
cout<<"2.check balance"<<endl;
cout<<"3.transfer money"<<endl;
cout<<"4.deposit"<<endl;
cout<<"0.exit"<<endl;
cin >>option;
if (option==0){
run = false;
} else if (option == 1){
cout <<"enter new pin" <<endl;
cin >>password;
pin = password;
cout <<"your new pin is:" << pin <<endl;
}else if (option == 2){
cout<<"your current balance is GHS:"<<balance <<".00"<<endl;
}else if (option == 3){
string number;
float amount;
cout <<"enter recipient number:"<<endl;
cin >>number;
cout <<"enter amount"<<endl;
cin >>amount;
if(amount >balance){
cout <<"not enough funds."<<endl;
}else {
balance-=amount;
cout<<"GHS"<<amount<<".00
has been sent to "<<number<<endl;
cout<<"your current balance is GHS"<<balance <<".00"<<endl;
}
}else if (option = 4){
float amount;
cout<<"enter amount:"<<endl;
cin >>amount;
balance += amount;
cout <<"transaction successful"<<endl;
cout <<"your new balance is GHS"<<balance <<".00"<<endl;
}
}
}
return 0;
}
