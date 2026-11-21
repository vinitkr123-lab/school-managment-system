# school-managment-
#include<iostream>
#inlcude<string>
using namespace std;
struct Student{
	int rollno;
	string name;
	char section;
	int age;
};
struct Teacher{
	int id;
	string name, subject;
	double salary;
};
struct Attendence{
	int roll;
	string data,status;
};
struct Fee{
	int rollno;
	double totalfee, paidfee;
};
struct Marks{
	int rollno;
	float m1,m2,m3,m4,m5;
};
struct Book{
	int rollno;
	string author,name;
	int issued;
};
struct Transport{
	int rollno;
	string busno,route;
};
struct Timeline{
	string studentclass,day, subject, time;	
};
------Array--------
Student students[100];
Teacher teachers[100];
Attendence attendences[100];
Fee fees[100];
Marks marks[100];
Book books[100];
Transport transports[100];
Timeline timelines[100];
string notices[100];
int studentcount=0;
int teachercount=0;
int attendence=0;
int fee=0;
int marks=0;
int book=0;
int transport=0;
int timeline=0;
int noticecount=0;
======login=====
bool login(){
	string username,int password;
	cout<<"Enter user name:";
	cin>>username;
	cout<<"Enter password:";
	cin>>password;
	if(username=="Admin"&& password=="1234"){
		cout<<"login successfully";
		return true;
	}
	cou<<"invalid username & password";
	return false;	
}
void addstudent(){
	if(studentcount>=100){
		cout<<"student limit reached:";
		return ;
	}
	cout<<"-------Add student-------";
	cout<<"Enter rollno:";
	cin>>student[studentcount].roll;
	cin.ignore();
	cout<<"Enter name:";
	getline(cin,student[studentcount].name);
	cout<<"Enter section:";
	cin>>student[studentcount].section;
	cout<<"Enter age:";
	cin>>student[studentcount].age;
	studentcount++;
	count<<"\nstudent add successfully.";	
}
void displaystudent(){
	cout<<"----------student record-----------";
	if(studentcount==0){
		cout<<"\nNo student record:";
		return;
	}
	for(int i=0; i<studentcount; i++){
		cout<<"Rollno:"<<students[i].rollno;
		cout<<"Name:"<<students[i].name;
		cout<<"Section:"<<students[i].section;
		cout<<"age:"<<students[i].age;
	}
}
void searchstudent(){
	int roll;
	cout<<"\nEnter rollno:";
	cin>>roll;
	for(int i=0; i<studentcount; i++){
		if(student[i].roll==roll){
			cout<<"\nStudent found successfully:";
			cout<<"Name:"<<student[i].name<<endl;
			cout<<"section:"<<student[i].section<<endl;
			cout<<"Age:"<<student[i].age<<endl;
			cout<<"\n-------------------\n";
			return;
		}
	}
	cout<<"student not found:";
}
void deletestudent(){
	int roll;
	cout<<"Enter rollno:";
	cin>>roll;
	for(int i=0; i<studentcount; i++){
		if(student[i].roll==roll){
			for(int j=i; j<student-1; j++){
			students[j]=students[j+1];	
			}
			studentcount--;
			cout<<"student delete successfully:";
			return;
		}
	}
	cout<<"Student not found:";
}
void updatestudent(){
	int roll;
	cout<<"\nEnter roll number:";
	cin>>roll;
	for(int i=0; i<studentcount; i++){
		if(student[i].roll==roll){
			cin.ignore();
			cout<<"\nEnter new name:";
			getline(cin,student[i].name);
			cout<<"\nEnter new Age:";
			cin>>student[i].age;
			cout<<"\n Enter new section:";
			cin>>student[i].section;	
		}
		cout<<"Students updated successfully:";
		return;
	}
	cout<<"\nstudent not found!";
}
void studentmenu(){
	int choice;
	do{
		cout<<"\nstudent managment system:\n"
		cout<<"\npress 1 for add student:";
		cout<<"\n press 2 for display student record:";
		cout<<"\n press 3 for search student record:";
		cout<<"\n press 4 for update student details:";
		cout<<"\n press 5 for delete student details:";
		cout<<"\n Enter your choice:";
		cin>>choice;
		switch(choice){
			case 1:
			 addstudent(); break;
			case 2:
				display();break;
			case 3:
				search(); break;
			case 4:
				update();break;
			case 5:
				delete();break;
			case 6:
				exit(0); break;
			default:
				cout<<"\n Invalid choice:";
		}
	}while(choice!=6);
}
// ==================== teacher managment system =================
void addteacher(){
	
}

