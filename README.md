Download Link: https://assignmentchef.com/product/solved-payroll-processing-for-different-kinds-of-employees
<br>
5/5 - (2 votes)

Your task is to implement payroll processing for different kinds of employees.

• Hourly employees get paid an hourly rate, but if they work more than 40 hours per week, the excess is paid at “time and a half”.

• Salaried employees get paid their salary, no matter how many hours they work.

• Managers are salaried employees who get paid a salary and a bonus.

Your program should compute the pay for a collection of employees. For each employee, ask for the number of hours worked in a given week, then display the weekly pay earned.

This problem description lists three classes: HourlyEmployee, SalariedEmployee, and Manager. We need a class that expresses the commonality among them: Employee. Organize the classes into an inheritance hierarchy. Here is the inheritance diagram for these classes. Details about this diagram are provided next:

Class Employee.java

instance variables: name –&gt; String

properties: setName(), getName() –&gt; same datatype that the instance variable “name”

methods: weeklyPay() –&gt; Double

Class HourlyEmployee.java

instance variables: hourlyWage –&gt; Double

methods: weeklyPay() –&gt; even though this method was declared in the superclass, you must override it in this class.

Class SalariedEmployee.java

instance variables: annualSalary –&gt; Double

methods: weeklyPay() –&gt; even though this method was declared in the superclass, you must override it in this class.

Class Manager.java

instance variables: weeklyBonus –&gt; Double

methods: weeklyPay() –&gt; even though this method was declared in the superclass, you must override it in this class.

You should implement the constructors and methods for all classes. Keep in mind that for some cases calling properties from the superclass, or sending parameters to constructors of the superclass will be required.

The weekly pay should be computed as specified in the problem description for each case. For instance:

For hourly employees: In general, you can calculate this as pay = hoursWorked * hourlyWage . However, consider that if an employee works more than 40 hours, the excess should be paid at “time and a half”.

For salaried employees: you can calculate the pay by dividing the annualSalary between the number of weeks worked per year. For this calculation, it does not really matter how many hours the employee has worked during the week. Consider a year has 52 weeks.

For managers: you just need to add the bonus to the salaried employee calculation.

Finally, add a Main.java class, which will be the interface of your program. It will not be part of the inheritance diagram but should contain the main method. This is the code you should use to test your program:

Employee[] staff = new Employee[4];

staff[0] = new HourlyEmployee(“Morgan, Harry”, 30); //30 is Harry’s wage per hour.

staff[1] = new SalariedEmployee(“Lin, Sally”, 52000); // 52000 is Lin’s annual salary.

staff[2] = new Manager(“Smith, Mary”, 52000, 50); //52000 is Mary’s annual salary and 50 is her bonus per week.

staff[3] = new HourlyEmployee(“Meza, Adriana”, 1); // 1 is Adriana’s wage per hour.

Scanner in = new Scanner(System.in);

for (Employee e: staff) {

System.out.print(“Hours worked by ” + e.getName() +”:”);

int hours = in.nextInt();

System.out.println(“Salary: ” + e.weeklyPay(hours));

}

You can assume that all salaries will be more than zero and that the hours worked will be more than zero as well. An example of the program running is here. The input provided by the user is the number of hours that the employee worked for a week.

<img decoding="async" style="margin: 0px; padding: 0px; border: 0px; font: inherit; vertical-align: baseline; max-width: 100%; height: auto;" alt="Console X <terminated> Main (5) [Java Application] /Library/Java/JavaVirtual Hours worked by Morgan, Harry:40 Salary: 1200.0" aria-describedby="fpl" data-recalc-dims="1" data-src="https://i0.wp.com/media.cheggcdn.com/study/8ab/8abc29fe-d598-46e8-a6b3-875e3635a715/image.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

<noscript>

 <img decoding="async" style="margin: 0px; padding: 0px; border: 0px; font: inherit; vertical-align: baseline; max-width: 100%; height: auto;" src="https://i0.wp.com/media.cheggcdn.com/study/8ab/8abc29fe-d598-46e8-a6b3-875e3635a715/image.png?w=980&amp;ssl=1" alt="Console X <terminated> Main (5) [Java Application] /Library/Java/JavaVirtual Hours worked by Morgan, Harry:40 Salary: 1200.0" aria-describedby="fpl" data-recalc-dims="1">

</noscript>

<img decoding="async" alt="Instance variable Employee name setName() getName(). weeklyPay(). Methods HourlyEmployee SalariedEmployee annualSalary hourly" aria-describedby="fpm" data-recalc-dims="1" data-src="https://i0.wp.com/media.cheggcdn.com/study/9c9/9c91f204-9b13-47a0-900e-55a2bd3a48f6/image.png?w=980&amp;ssl=1" class="lazyload" src="data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==">

<noscript>

 <img decoding="async" src="https://i0.wp.com/media.cheggcdn.com/study/9c9/9c91f204-9b13-47a0-900e-55a2bd3a48f6/image.png?w=980&amp;ssl=1" alt="Instance variable Employee name setName() getName(). weeklyPay(). Methods HourlyEmployee SalariedEmployee annualSalary hourly" aria-describedby="fpm" data-recalc-dims="1">