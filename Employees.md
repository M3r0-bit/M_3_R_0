 #include <iostream>
using namespace std;
#include <string>
const int l=1;
struct name{
    string Fname,Mname,Lname;
};
struct Address{
    int bNo;
    string stName, cityName;
};
struct Employees{
    int id;
    name n;
    Address ad;
    float salary;
};
int main() {
    Employees e[l];
    int ch;
    do{
        cout<<"press 1 to fill data"<<endl;
        cout<<"press 2 to display all data"<<endl;
        cout<<"press 3 to display data whose salaries are greater than a certain number"<<endl;
        cout<<"press 4 to search by first name"<<endl;
        cout<<"press 5 to search by city name"<<endl;
        cout<<"press 6 to exit"<<endl;
        cin>>ch;
        switch(ch){
            case 1:{
                for (int i=0;i<l;i++){
                    cout<<"enter id"<<endl;
                    cin>>e[i].id;
                    cout<<"enter first name"<<endl;
                    cin>>e[i].n.Fname;
                    cout<<"enter middle name"<<endl;
                    cin>>e[i].n.Mname;
                    cout<<"enter last name"<<endl;
                    cin>>e[i].n.Lname;
                    cout<<"enter building number"<<endl;
                    cin>>e[i].ad.bNo;
                    cout<<"enter street name"<<endl;
                    cin>>e[i].ad.stName;
                    cout<<"enter city name"<<endl;
                    cin>>e[i].ad.cityName;
                    cout<<"enter salary"<<endl;
                    cin>>e[i].salary;
                }
            } break;
            case 2:{
                for (int i=0;i<l;i++){
                    cout<<"The id: "<<e[i].id<<endl;
                    cout<<"The first name: "<<e[i].n.Fname<<endl;
                    cout<<"The second name: "<<e[i].n.Mname<<endl;
                    cout<<"The third name: "<<e[i].n.Lname<<endl;
                    cout<<"The buliding number: "<<e[i].ad.bNo<<endl;
                    cout<<"The street name: "<<e[i].ad.stName<<endl;
                    cout<<"The city name: "<<e[i].ad.cityName<<endl;
                    cout<<"The salary: "<<e[i].salary<<endl;
                }
            } break;
            case 3:{
                float s;
                cout<<"Enter salary: ";
                cin>>s;
                for (int i=0;i<l;i++){
                    if(e[i].salary>s){
                    cout<<"The id: "<<e[i].id<<endl;
                    cout<<"The first name: "<<e[i].n.Fname<<endl;
                    cout<<"The second name: "<<e[i].n.Mname<<endl;
                    cout<<"The third name: "<<e[i].n.Lname<<endl;
                    cout<<"The buliding number: "<<e[i].ad.bNo<<endl;
                    cout<<"The street name: "<<e[i].ad.stName<<endl;
                    cout<<"The city name: "<<e[i].ad.cityName<<endl;
                    cout<<"The salary: "<<e[i].salary<<endl;
                    }
                }
            } break;
            case 4:{
                string n1;
                cout<<"Enter first name: ";
                cin>>n1;
                for (int i=0;i<l;i++){
                    if(n1==e[i].n.Fname){
                    cout<<"The id: "<<e[i].id<<endl;
                    cout<<"The first name: "<<e[i].n.Fname<<endl;
                    cout<<"The second name: "<<e[i].n.Mname<<endl;
                    cout<<"The third name: "<<e[i].n.Lname<<endl;
                    cout<<"The buliding number: "<<e[i].ad.bNo<<endl;
                    cout<<"The street name: "<<e[i].ad.stName<<endl;
                    cout<<"The city name: "<<e[i].ad.cityName<<endl;
                    cout<<"The salary: "<<e[i].salary<<endl;
                    }
                }
            } break;
            case 5:{
                string cname;
                cout<<"Enter city name: ";
                cin>>cname;
                for (int i=0;i<l;i++){
                    if(cname==e[i].ad.cityName){
                    cout<<"The id: "<<e[i].id<<endl;
                    cout<<"The first name: "<<e[i].n.Fname<<endl;
                    cout<<"The second name: "<<e[i].n.Mname<<endl;
                    cout<<"The third name: "<<e[i].n.Lname<<endl;
                    cout<<"The buliding number: "<<e[i].ad.bNo<<endl;
                    cout<<"The street name: "<<e[i].ad.stName<<endl;
                    cout<<"The city name: "<<e[i].ad.cityName<<endl;
                    cout<<"The salary: "<<e[i].salary<<endl;
                    }
                }
            } break;
            case 6:{
                exit(0);
            }
            default:{
                cout<<"wrong choice.. try again"<<endl;
            }
        }
    }while(ch!=6);
    return 0;
}
