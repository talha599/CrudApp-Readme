# CRUD Application for Contact Management

This repository contains a simple CRUD (Create, Read, Update, Delete) application in C# for managing contacts. The application allows you to perform basic operations on a contact list stored in a SQL Server database.



## Table Structure
The application operates on a table named `Contacts` with the following structure:

![Screenshot 2024-09-19 123224](https://github.com/user-attachments/assets/6a879ff9-b32e-4bcb-b836-6a63b9490cfd)

## Prerequisites

- .NET Framework (version 4.7.2 or higher)
- SQL Server (version 2012 or higher)
- SQL Server Management Studio (SSMS)
- Visual Studio (Community Edition or higher)



## How to Run

Step 1: Setup the Database

1. Create a New Database:

- Open SQL Server Management Studio (SSMS).
- Right-click on `Databases` and select `New Database`.
- Name the database  `ContactDB`.

2. Generate the Table Script:

- Copy the following SQL script and execute it in SSMS to create the `Contacts` table:

```bash
  CREATE TABLE Contacts (
    ID INT PRIMARY KEY IDENTITY(1,1),
    FirstName NVARCHAR(50),
    LasttName NVARCHAR(50),
    Phone NVARCHAR(20),
    Age INT
);
```
3. Backup the Database (Optional):

- Right-click on `ContactDB` in SSMS.
- Select `Tasks` -> `Back Up`.
- Choose the destination and backup the database for future use.

Step 2: Configure the Application
1. Clone the Repository:

- Clone this repository to your local machine using:

```bash
  git clone <repository-url>
```
2. Open the Solution:

- Open the solution file `(.sln)` in Visual Studio.
3. Modify the Connection String:

- Open the `app.config` file.
- Update the connection string to point to your local SQL Server instance and the ContactDB database:

```bash
  <connectionStrings>
    <add name="ContactDB" connectionString="Data Source=TALHA;Initial Catalog=MyCURD;Integrated Security=True;TrustServerCertificate=True" />
</connectionStrings>

```

Step 3: Run the Application
1. Build the Solution:

- Build the solution in Visual Studio to restore all necessary packages.
2. Run the Application:

- Press `F5` or click `Start` in Visual Studio to run the application.
3. Perform CRUD Operations:

 You can now perform the following operations:
- Create: Add new contacts.
- Read: View the list of contacts.
- Update: Modify contact details.
- Delete: Remove a contact.
## Database Backup

To backup the `ContactDB` database:

1. Open SSMS and right-click on the `ContactDB`.
2. Navigate to `Tasks` -> `Back Up`.
3. Select the destination and click `OK` to create a backup file.
## Support

For support, Email: talhasedubd@gmail.com or Watch: https://youtu.be/mzeUKQjJK5c?si=n-TIVOsHtAzTHyHH.


## License

[MIT](https://choosealicense.com/licenses/mit/)

