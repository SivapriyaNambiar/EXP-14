# EXP-14

### Aim 
To study and implement Inheritance. 

### Software 
Visual Studio Code. 

### Theory 
Inheritance -> The capability of a class to derive properties and characteristics from another class is called Inheritance. Inheritance is one of the most important features of Object Oriented Programming in C++. <br> 
Modes of Inheritance in C++ <br> 
Mode of inheritance controls the access level of the inherited members of the base class in the derived class. In C++, there are 3 modes of inheritance: <br> 

(1) Public Mode <br> 
(2) Protected Mode  <br> 
(3) Private Mode  <br> 

Types Of Inheritance in C++  <br> 
The inheritance can be classified on the basis of the relationship between the derived class and the base class. In C++, we have maily 4 types of inheritances:  <br> 

(1) Single inheritance <br> 
In single inheritance, a class is allowed to inherit from only one class. i.e. one base class is inherited by one derived class only.<br> 

Syntax <br> 

class subclass_name : access_mode base_class <br> 
{ <br> 
  //  body of subclass <br> 
};                  <br> 

(2) Multilevel inheritance <br> 
Multiple Inheritance is a feature of C++ where a class can inherit from more than one class. i.e one subclass is inherited from more than one base class. <br> 

Syntax <br> 

class subclass_name : access_mode base_class1, access_mode base_class2, .... <br> 
{ <br> 
  // body of subclass <br> 
}; <br> 

(3) Multiple inheritance <br> 
In this type of inheritance, a derived class is created from another derived class and that derived class can be derived from a base class or any other derived class. There can be any number of levels. <br> 

(4) Hierarchical inheritance <br> 
In this type of inheritance, more than one subclass is inherited from a single base class. i.e. more than one derived class is created from a single base class.  <br> 

### Code 
(A) <br> 
```
// NAME - SIVAPRIYA NAMBIAR
// PRN - 23070123125 
// EXPERIMENT - 14(A)  

// Program to show single inheritance.

# include <iostream>
# include <string>
using namespace std;

class Uni
{
    public:
    string uni= "Symbiosis";
    void discipline()
    {
        cout << "Engineering" <<endl;
    }
};
class Dep : public Uni
{
    public:
    string dept= " Electronics & Telecommunication";
};
int main()
{
    Dep u1;
    u1.discipline();
    cout<<u1.uni + " "+u1.dept ;
} 

```

(B) <br> 
```
// NAME - SIVAPRIYA NAMBIAR
// PRN - 23070123125 
// EXPERIMENT - 14(B) 

// Program toshow multiple inheritance.

#include<iostream> 
#include<string> 
using namespace std; 

// Parent CLass1 
class Vehicle {
    public:
    string company=" Ford";
    void type(){
        cout << "Mustang"<< endl;
    }
};
// Parent Class 2
class Specs{
    public:
    string mileage="8 kmpl";
    void colour(){
        cout<<"Grey"<<endl;
    }
};
// Child Class-1 (derived from parent- 1&2)
class Car: public Vehicle,public Specs{
    public:
    string seater = " 4 seater";
};
int main(){
    //multiple inheritance
    Car f2;
    f2.colour();
    cout<<f2.company<<" ";
    f2.type();
    cout<<"("<<f2.seater<<")"<<endl<<"MILEAGE:"<<f2.mileage<<endl;
} 

```

(C) <br> 
```
// NAME - SIVAPRIYA NAMBIAR
// PRN - 23070123125 
// EXPERIMENT - 14(C) 

// Program to showmultilevel inheritance.

#include<iostream> 
#include<string>
using namespace std; 

// single base class
class Student {
public:
    string stud;
    void get_Student_data()
    {
        cout << "Enter the name of the student: ";
        cin >>  stud;
    }
};
 
// derived class from base class
class PRN : public Student {
public:
    int prn;
    void get_PRN_data()
    {
        cout << "Enter the PRN: ";
        cin >> prn;
    }
};
 
// derived from class derive1
class Branch : public PRN {
private:
   string branch;
 
public:
    void get_Branch_data()
    {
        cout << "Enter the branch: ";
        cin >> branch;
    }
 
    // function to print sum
    void details()
    {
        cout << "Name: "<<stud<<"  PRN: "<< prn<<"  Branch: "<<branch << endl;
    }
};
int main()
{
    // object of sub class
    Branch obj;
 
    obj.get_Student_data();
    obj.get_PRN_data();
    obj.get_Branch_data();
    obj.details();
    return 0;
}                                     
```

(D) <br> 
```
// NAME - SIVAPRIYA NAMBIAR
// PRN - 23070123125 
// EXPERIMENT - 14(D) 

// Program to show Hiererchical Inheritance.                    

#include <iostream>
using namespace std;

// base class
class Flower {
public:
    Flower() { cout << "This is a Flower. \n"; }
};

// first sub class
class Lotus : public Flower {
public:
    Lotus() { cout << "This flower is a lotus. \n"; }
};

// second sub class
class Marigold : public Flower {
public:
    Marigold() { cout << "Thisflower is a marigold. \n"; }
};

// main function
int main()
{
    // Creating object of sub class will invoke the constructor of base class.
    Lotus obj1;
    Marigold obj2;
    return 0;
}                                                                                             
```

### Output 
(A) <br>  
![](https://github.com/Shloka-Patel/Experiment---14/blob/main/Output_14A.png) 

(B) <br> 
![](https://github.com/Shloka-Patel/Experiment---14/blob/main/Output_14B.png) 

(C) <br> 
![image](https://github.com/user-attachments/assets/29e636ba-a831-489a-a1f3-b9d411069dbf)


(D) <br> 
![](https://github.com/Shloka-Patel/Experiment---14/blob/main/Output_14D.png) 

### Conclusion 
I learnt about inheritance in C++, its keywords, modes, types and performed programs based on that. 
