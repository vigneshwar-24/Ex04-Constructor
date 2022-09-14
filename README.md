# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
 ### Step1:
 
 
 
 ## Program:
 ```
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
            hra = (20 / 100) * this.basicsalary;
            ta = (10 / 100) * this.basicsalary;
            income = hra + ta + this.basicsalary - this.insuranceamount;
        }
        public void display()
        {
            Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}", this.name, this.noofexperience, this.designation);
            Console.WriteLine("Receives {0} of salary", income);
        }
        public static void Main(String[] args)
        {
            Employ emp1 = new Employ("viki", "gdm", 10, 80000, 1000);
            Employ emp2 = new Employ("loki", "Developer", 5, 25000, 1000);
            emp1.salary();
            emp2.salary();
            emp1.display();
            emp2.display();
        }
    }
}
 ```
 
 ## Output:
 
 ![exp4](https://user-images.githubusercontent.com/77089276/190057914-14017912-b609-44aa-8de4-7124825762c0.PNG)

 
 ## Result:
