Case Study: Hotel Reservation System
How to Run the Application
1. Prerequisites:
o Java Development Kit (JDK): Ensure that you have the JDK installed on your machine. 
o Text Editor or Integrated Development Environment (IDE)
2. Running the Application:
o Step 1: Copy the provided source code into a file named HotelReservationSystem.java.
o Step 2: Open your terminal or command prompt and navigate to the directory where the file is located.
o Step 3: Compile the program using the following command:
javac HotelReservationSystem.java
o Step 4: Run the compiled program with the following command:
java HotelReservationSystem
o Step 5: The application will start, and you can interact with it using the console by following the on-screen prompts.
Instructions for Each Feature
1. View Room Availability:
o Select Option 1: When prompted, enter 1 to view the available rooms.
o Output: The system will display a list of rooms that are currently available, including details such as room number, type, and price.
2. Make a Reservation:
o Select Option 2: Enter 2 to make a reservation.
o Enter Room ID: Provide the ID of the room you wish to reserve.
o Enter Guest Name: Input the guest's name.
o Confirmation: The system will display the reservation details, including the room number, check-in, and check-out dates, and the total 
price.
3. Cancel a Reservation:
o Select Option 3: Enter 3 to cancel an existing reservation.
o Enter Reservation ID: Provide the ID of the reservation you wish to cancel.
o Confirmation: The system will confirm the cancellation and update the room’s availability status.
4. Check-in:
o Select Option 4: Enter 4 to check-in.
o Enter Reservation ID: Input the reservation ID for the room you wish to check into.
o Confirmation: The system will confirm the check-in and update the room status accordingly.
5. Check-out:
o Select Option 5: Enter 5 to check-out.
o Enter Reservation ID: Provide the reservation ID for the room you are checking out of.
o Confirmation: The system will confirm the check-out, marking the room as available again.
6. Exit:
o Select Option 6: Enter 6 to exit the application.
Explanation of the Exception Handling Implemented
1. Input Validation:
o The system performs input validation to ensure that the data provided by the user is valid. For example:
 If a user enters an invalid room ID or reservation ID, the system will prompt the user to try again instead of causing a crash.
 During reservation, the system checks if the room is available before proceeding, and will notify the user if the room is already 
booked.
2. Null Checks:
o The system performs null checks when searching for rooms or reservations to avoid NullPointerException. If an object is not found, the 
system informs the user and does not attempt to perform any operations on a null reference.
3. Graceful Error Messages:
o Instead of the program terminating abruptly, custom error messages are provided to guide the user when they make mistakes (e.g., 
trying to cancel a reservation that doesn't exist).
4. Try-Catch Blocks:
o The system uses try-catch blocks to handle potential runtime exceptions such as input mismatches when reading user input. For 
instance, if a user inputs a non-numeric value where a number is expected, the system will catch the exception and prompt the user to 
enter a valid value.

Case Study: Hotel Reservation System
Brief Report on the Application Design and Object-Oriented Principles Applied
Application Design Overview
The Hotel Reservation System is designed using Core Java principles, focusing on simplicity and clarity. The system manages hotel operations such as 
viewing room availability, making reservations, canceling reservations, and handling check-ins and check-outs. The design is modular, with separate 
classes representing different entities (Room, Reservation, HotelManager), each responsible for handling its specific functionality.
Object-Oriented Principles Applied
1. Encapsulation:
o The principle of encapsulation is implemented by keeping the attributes of each class private and providing public getter and setter 
methods. This ensures that the internal state of an object is protected from unauthorized access or modification.
o Example: The Room class encapsulates its attributes (number, type, price, available) and provides public methods to access and modify these 
attributes.
2. Abstraction:
o Abstraction is achieved by hiding complex implementation details and exposing only the necessary parts of the functionality through 
methods.
o Example: The HotelManager class provides methods like makeReservation and checkRoomAvailability, which abstract away the complex logic 
involved in managing reservations and room availability.
3. Inheritance:
o While the provided example does not require inheritance (as it focuses on a small-scale system), inheritance could be applied if the 
system were to be expanded. For instance, different types of rooms (Single, Double, Suite) could be represented as subclasses of a base 
Room class.
4. Polymorphism:
o Polymorphism could be applied in a more advanced version of the system. For example, if different types of reservations (e.g., standard, 
premium) were introduced, methods could be overridden to provide specific behavior for each type.
5. Reusability and Maintainability:
o The design ensures that the code is reusable and maintainable. Methods in the HotelManager class, such as findRoomById and 
findReservationById, are reusable across different functionalities. The clear separation of concerns makes the system easy to maintain and 
extend in the future.
6. Separation of Concerns:
o Each class has a distinct responsibility, making the code modular. The Room class handles room-related information, the Reservation class 
handles reservation-related data, and the HotelManager class manages overall operations.

