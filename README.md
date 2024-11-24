![image](https://github.com/user-attachments/assets/56eed5ed-df7a-4ac9-a566-d3bb7863be28)# ***Employee Data Management System***

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

#### 1] Employee: ➡️ Uses private attributes to ensure data encapsulation

1) **Constructor**: Instantiate an **Employee** object with the parameters(id,name,position,email,salary).

2) **getters/setters**: Each attribute has its getter and setter methods all go by the name get_(**attribute_name**) / set_(**attribute_name**).

**_Note:_** ➡️ The set_email() method doesn't accept email values that don't contain both the following keys: ['@', '.com']
            ➡️ The set_salary(salary_amount) method doesn't accept non-numeric values and will notify the user of that error and return him to the main menu.
      
3) **add_bonus(amount)**: will add a bonus to the current employee's salary by the (amount) given in the parameter.

4) **__str__**: it will print the data of the current Employee.

#### 2] EmployeeManager: 
_**1. Create**_
- **add_employee(employee):**
1) Add a new employee to the system.
2) Validate email format (@ and .com required) and salary type.
3) Appends employee data to the CSV file.
4) Uses the method get_next_id() to automatically assign the id of the new Employee to the next id.
   
**Parameters:**
employee (an Employee object).

**Returns:**
True if the employee was successfully added.
False otherwise.

**_2. Read_**
- **list_employees()**
1) Print all employees in the system.
2) Displays data in a tabular format.

- **search_by_id(id):**
1) Searches for an employee by ID.
   
**Parameters:**
id (integer).

**Returns:**
Tuple (True, Employee) if the employee exists.
(False, None) otherwise.

- **get_all():**

1) Retrieves all employees as Employee objects.
   
**Returns:**
List of Employee objects.

- **get_positions():**
Returns a unique set of all positions held by employees.

- **show_positions():**
Prints all unique employee positions.

**_3. Update_**
- **update(id, choice, new_value):**
Updates an employee's details.

**Parameters:**
id (integer): Employee ID.
choice (integer): Field to update (1: Name, 2: Position, 3: Email, 4: Salary).
new_value: The new value to set.

**Returns:**
True if the update was successful.
False if the ID or choice was invalid.

**add_bonus(amount, ids=[]):**
Adds a bonus to specific employees.

**Parameters:**
amount (float): Bonus amount.
ids (list of integers): Employee IDs to update.

**Returns:**
True if bonuses were added successfully.
False if invalid IDs are found.

**_4. Delete_**
- **_delete(id):_**
Deletes an employee by ID.

**Parameters:**
id (integer).

**Returns:**
True if the employee was successfully deleted.
False if the ID does not exist.

**_5. Class Methods_**
- **Map_2_emp(row):**
Maps a CSV row to an Employee object.

**Parameters:**
row (list of strings): Row data from the CSV.

**Returns:**
Employee object if the data is valid.
None otherwise.

- **get_next_id()**
Computes the next unique ID for a new employee.

**Returns:**
An integer representing the next ID.

### _**Terms_Of_Use**_
