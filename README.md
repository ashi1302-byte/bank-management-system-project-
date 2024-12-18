# bank-management-system-project-
//
#include<iostream>
using namespace std;
class booking{
public:
int id;
string from;
string to;
int guest_no;
void setbooking(int id,string from,string to,int guest_no){
this->id=id;
this->from=from;
this->to=to;
this->guest_no=guest_no;
}
void getbooking(){
cout<<"booking ID = "<<id<<endl;
cout<<"date from = "<<from<<" to "<<endl;
cout<<"guest number="<<guest_no<<endl;
}
};
class room:public booking{
public:
int id;
string room_type;
void setroom(int id,string room_type){
this->id=id;
this->room_type=room_type;
}
void getroom(){
cout<<"room id="<<id<<endl;
cout<<"room type="<<room_type;
}
};
class guest:public booking{
public:
string name;
string surname;
int age;
void setguest(string name,string surname,int age){
this->name=name;
this->surname=surname;
this->age=age;
}
void getguest(){
cout<<"Guest name : "<<name<<endl;
cout<<"surname : "<<surname<<endl;
cout<<"age of guest : "<<age<<endl;
}
};
class payment:public booking{
public:
int amount;
string cardNumber;
void setpayment(int amount,string cardNumber){
this->amount=amount;
this->cardNumber=cardNumber;
}
void getpayment(){
cout<<"Amount="<<amount<<endl;
cout<<"card number="<<cardNumber<<endl;
}
};
int main(){
guest guest;
room room;
room.setbooking(1001,"27-july-2022","28-july-2022",2);
room.setroom(201,"AC room");
room.getbooking();
room.getroom();
guest.setbooking(1002,"27-july-2021","31-july-2022",4);
guest.setguest("NIL","patil",23);
guest.getbooking();
guest.getguest();
payment payment;
payment.setbooking(1003,"27-july 2022","29-july 2022",7);
payment.setpayment(3500,"N00001234");
payment.getbooking();
payment.getpayment();
return 0;
}
