Bank System with Login – C++ 🔐💻


Overview:

This project is a robust Bank Management System built entirely in C++, showcasing advanced file handling, user authentication, and role-based permissions. Developing such functionality in C++ comes with unique challenges, but this project demonstrates a seamless integration of these features into a console-based application.

Features:

1. Login System 🔑
   
	•	User credentials are stored securely in an external file (users.txt) with encrypted passwords.
	•	Fields in the file include Name, Email, UserID, Encrypted Password, and Permission Key.
	•	Each record is delimited using #//# to ensure structured parsing.
	•	Password encryption:
		A simple yet effective technique subtracts 2 from each digit of the password before storing it.
		Example: Password 1234 is stored as 3456.

2. Clients Management 👥
   
	•	A separate file named clients.txt is used to store all the bank’s client data.
	•	This file contains client information, enabling functionality such as listing, adding, updating, or deleting clients based on user permissions.
	•	Operations on this file ensure a structured and organized system for client management.

3. Role-Based Permissions 🛡️
   
	•	The system uses an enum to define permissions for user roles:

		enum enPermissions {  
		    eAll = -1,  
		    pListClients = 1,  
		    pAddNewClient = 2,  
		    pDeleteClient = 4,  
		    pUpdateClients = 8,  
		    pFindClient = 16,  
		    pTransactions = 32,  
		    pManageUsers = 64,  
		    pShowLogInRegister = 128  
		};  


	•	Permission keys grant access to specific functionalities for example:
	•	-1: Special user with access to all functionalities.
	•	 7: Access to listing, adding, and deleting clients.
	•	 0: Denied access, with a message “Access Denied”.


4. Functionalities 🛠️

	After successful login, users can choose from 10 options, depending on their permissions:
	•	Client management: List, add, delete, update, or search for clients using clients.txt.
	•	Transactions: Handle banking transactions and currency exchange.
	•	System management: View transaction logs, login history, and manage system users and permissions.
	•	Logging out: Safely end the session.

	 ![GUI Bank](https://github.com/user-attachments/assets/4c3cf150-bde8-45d5-a68b-1863a6a3cda1)


5. File Handling 📂
   
	•	users.txt: Stores user credentials, encrypted passwords, and permission keys.
	•	clients.txt: Stores all client-related data for the bank, allowing flexible and secure management of client information.
	•	Files are parsed dynamically to retrieve, update, or modify data as needed.

Challenges Overcome 🚀

	•	Implementing an encrypted login system with role-based permissions in C++, without the luxury of built-in libraries, highlights the complexity and creativity required for file handling, enum-based permissions, and data encryption.
	•	Managing user and client data securely while maintaining flexibility in permissions access is non-trivial, but this system demonstrates it efficiently.

How to Run 🏃‍♂️

	✅	Clone the repository to your local system.
	✅	Ensure the following files are included in the project directory:
 
	•	users.txt: Contains user credentials in the following format:
               Name#//#Email#//#UserID#//#EncryptedPassword#//#PermissionKey  
               Example: John Doe#//#john.doe@email.com#//#JD123#//#3456#//#7  


	•	clients.txt: Contains the bank’s client data.

	✅	Compile and run the code using a C++ compiler.
	✅	Follow the on-screen instructions to log in and interact with the system.

