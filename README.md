### EX NO:04
### DATE: 
# <p align="center">Constructor</p> 
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
## Algorithm:
### Step1:
Start.

### Step2:
Create a class and a constructor.

### Step3:
Get name, designation, noofexperience, basic salary and insurance amount from the User.

### Step4:
Call salary method in constructor to calculate salary.

### Step5:
Call display method to display the output.

### Step6:
stop.
 
 
 
 ## Program:
 ```python
using System;
namespace Hello
{
    class Employ
    {
        public string name, designation;
        public int noofexperience, basicsalary, insuranceamount;
        float hra, ta, income;
        public Employ(string name, string designation, int noofexperience, int basicsalary, int insuranceamount)
        {
            this.name = name;
            this.designation = designation;
            this.noofexperience = noofexperience;
            this.basicsalary = basicsalary;
            this.insuranceamount = insuranceamount;
        }
        public void salary()
        {
            hra = (20 * this.basicsalary) /100;
            ta = (10* this.basicsalary) /100;
            income = hra+ this.basicsalary + ta  - this.insuranceamount;
        }
        public void display()
        {
            Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}", this.name, this.noofexperience, this.designation);
            Console.WriteLine("Receives {0} of salary", income);
        }
        public static void Main(String[] args)
        {
            Employ emp1 = new Employ("Hari", "Tester", 10, 30000, 1000);
            Employ emp2 = new Employ("Latha", "Developer", 5, 25000, 1000);
            emp1.salary();
            emp2.salary();
            emp1.display();
            emp2.display();
        }
    }
}
 ```
 ## Output:
 
![4](https://user-images.githubusercontent.com/77089276/190059223-516d77b7-daca-457a-a356-4271697c1b3f.PNG)


 ## Result:
Thus the C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor is executed successfully.
