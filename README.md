# ***Employee Data Management System***

## **Table of contents**

- [Overview](#Overview)
- [Classes/Methods](#Classes/Methods)
- [Terms Of Use](#Terms_Of_Use)

### _**Overview**_

This is a simple **Employee Data Management System**,
which helps persistently store, retrieve,
and manipulate the data using a CSV(comma-separated values) file,
one can use the program with a CLI(Command line interface),
and The program uses the CSV Python library to handle the read and write operations in the file.
The CSV file classifies the Employees into the following categories (labels/columns): Employee ➡️ (ID, Name, Position, Email, Salary). 

_**Note**_: To effectively use the system's functionalities, follow the CLI instructions when running the app.

### _**Classes/Methods**_

**Classes**:
  1] Employee: ➡️ Uses private attributes to ensure data encapsulation
  
      1) **Constructor**: Instantiate an **Employee** object with the parameters(id,name,position,email,salary).
      
      2) **getters/setters**: Each attribute has its getter and setter methods all go by the name get_(**attribute_name**) / set_(**attribute_name**).
        **_Note:_** ➡️ The set_email() method doesn't accept email values that don't contain both the following keys: ['@', '.com']
                    ➡️ The set_salary(salary_amount) method doesn't accept non-numeric values and will notify the user of that error and return him to the main menu.
                    
      3) **add_bonus(amount)**: will add a bonus to the current employee's salary by the (amount) given in the parameter.
      4) **__str__**: it will print the data of the current Employee.
  2] EmployeeManager:
      
