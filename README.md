# Bus-Revervation-System-in-C
This C program implements a Bus Reservation System, which allows users to log in, book tickets, cancel tickets, and check the status of buses. The system involves two main components: user authentication and bus reservation management.

Key Features of the Project:
User Login:

A login system is implemented where users can enter their username and password to authenticate.
The system allows multiple users (5 in this case, with predefined usernames and passwords) to log in and perform actions in the user menu.
Bus Information:

Bus details such as bus number, source, destination, total seats, available seats, and fare are stored in a Bus structure.
Three buses are predefined in the system, each with its own details like bus number, route, available seats, and fare.
Main Menu:

After starting the program, the user is prompted with a main menu offering two options: Login or Exit.
If the user chooses to log in, they will be asked for their username and password. If successful, the system proceeds to the user menu.
If the user opts to exit, the program terminates.
User Menu:

Once logged in, the user has access to the user menu with the following options:
Book a Ticket: Allows the user to book a specific number of seats on a bus. The system checks if there are enough available seats.
Cancel a Ticket: Users can cancel previously booked tickets, provided the number of seats they wish to cancel doesn’t exceed the number of booked seats.
Check Bus Status: Users can check the details of any bus, including its source, destination, total seats, available seats, and fare.
Logout: Logs the user out and returns to the main menu.
Ticket Booking and Cancellation:

The user can book or cancel tickets by specifying a bus number and the number of seats they wish to book or cancel.
The system performs checks to ensure that the number of seats being booked or canceled is valid (i.e., there are enough available seats for booking or enough booked seats for cancellation).
Data Structures:

The system uses structures to store both user login information (User structure) and bus details (Bus structure).
An array of User structures is used to store multiple users' login credentials, and an array of Bus structures is used to store information about different buses.
How the System Works:
Login Phase: The user is asked to provide a username and password, which is checked against the predefined list of users.
Post-Login Operations: Once logged in, the user can choose to book or cancel tickets, check bus statuses, or log out.
Ticket Booking Logic: When a user chooses to book tickets, the system checks if the requested number of seats is available. If available, the seats are booked, and the system updates the bus's available seat count.
Ticket Cancellation Logic: Similarly, when a user wants to cancel tickets, the system ensures that they cannot cancel more tickets than they initially booked.
Possible Improvements:
Data Persistence: The current system does not store data permanently. Adding file handling could allow user and bus data to persist across program executions.
Enhanced User Management: The user management could be improved by allowing for user registration, password recovery, etc.
Multiple Bus Routes: The program could be expanded to support more dynamic bus routes, instead of having a fixed number of buses.
Conclusion:
This project serves as a simple demonstration of using C to implement a bus reservation system with basic functionalities like user authentication, ticket booking, cancellation, and checking bus status. It provides a clear and structured approach to handling user inputs and manipulating bus data.


Sample Output:
=== Main Menu ===
1. Login
2. Exit
Enter your choice: 1
Enter Username: user1
Enter Password: pass1
Login successful. Welcome, user1!

=== User Menu ===
1. Book a Ticket
2. Cancel a Ticket
3. Check Bus Status
4. Logout
Enter your choice: 3

Enter Bus Number: 101

Bus Number: 101
Source: City A
Destination: City B
Total Seats: 50
Available Seats: 50
Fare: 500.00

=== User Menu ===
1. Book a Ticket
2. Cancel a Ticket
3. Check Bus Status
4. Logout
Enter your choice: 1

Enter Bus Number: 101
Enter Number of Seats: 2
Booking successful! 2 seats booked on Bus Number 101.

=== User Menu ===
1. Book a Ticket
2. Cancel a Ticket
3. Check Bus Status
4. Logout
Enter your choice: 3

Enter Bus Number: 101

Bus Number: 101
Source: City A
Destination: City B
Total Seats: 50
Available Seats: 48
Fare: 500.00

=== User Menu ===
1. Book a Ticket
2. Cancel a Ticket
3. Check Bus Status
4. Logout
Enter your choice: 2

Enter Bus Number: 101
Enter Number of Seats to Cancel: 1
Cancellation successful! 1 seats canceled on Bus Number 101.

=== User Menu ===
1. Book a Ticket
2. Cancel a Ticket
3. Check Bus Status
4. Logout
Enter your choice: 3

Enter Bus Number: 101

Bus Number: 101
Source: City A
Destination: City B
Total Seats: 50
Available Seats: 49
Fare: 500.00
