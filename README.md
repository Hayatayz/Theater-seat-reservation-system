# Theater-seat-reservation-system
Theater Seat Reservation System  This C++ program simplifies the process of reserving theater seats. It allows users to view available and reserved seats, book or cancel reservations, and handles pricing based on seat location. The system also uses file handling to save and load reservation data, ensuring persistence. 
This Theater Seat Reservation System, a simple program that lets users reserve seats, check seat availability, and search for existing reservations. It explains the development of the system following the Software Development Life Cycle (SDLC). Each stage, from planning and design to implementation and testing, is covered to show how the system was created and organized. This project focuses on the main features of seat reservation while highlighting the importance of structured coding and modular design for creating a smooth, user-friendly program.
The SDLC are the following
Planning
The Theater Seat Reservation System is designed to manage seat reservations for VIP and Standard sections while ensuring input validation and error handling. The system allows users to reserve seats, check availability, and search for reservations by name. The focus is on creating a user-friendly program that handles invalid inputs and avoids crashes. The code uses arrays to track seat reservations and stores user data like names, ages, and preferred genres to ensure smooth operation.
Requirements
The system will allow users to reserve seats, view seat statuses, and search for reservations by name. Input validation is key: names should only contain alphabetic characters, ages must be numeric, and the system should check for available seats before making a reservation. If a section is full, it should offer users the option to reserve a seat in the other section. 
The design of the system revolves around simplicity and modularity. The program utilizes arrays to track seat availability for VIP and Standard sections, while functions like getValidString ensure that the user inputs are validated. The user is guided through the system using a menu-driven interface, and each task is handled by a dedicated function to keep the code organized and modular. The main program flow includes reserving seats, checking availability, and searching for reservations.
Algorithm are

Step 1: Initialize Constants and Variables
1. Define constants for the number of VIP and Standard seats:
VIP_SEATS = 30
STANDARD_SEATS = 70
2. Initialize two boolean arrays to track the reserved status of seats:
vipSeats (size 30): All elements initialized to false.
standardSeats (size 70): All elements initialized to false.
3. Initialize arrays to store user details:
names[100]: To store user names.
genres[100]: To store user-preferred genres.
sections[100]: To store the section ("VIP" or "Standard").
ages[100]: To store user ages.
seatNumbers[100]: To store reserved seat numbers.
4. Set userCount = 0 to track the number of reservations.
Step 2: Define Utility Functions
1. getValidString(prompt, alphabeticOnly): Repeatedly prompt the user for input until a valid string is entered.
If alphabeticOnly = true, ensure the string contains only alphabetic characters or spaces.
If alphabeticOnly = false, ensure the string contains only numeric characters.
Step 3: Display Main Menu
1. Display options for the user:
     1. Reserve a VIP Seat.
     2. Reserve a Standard Seat.
    3. View Seat Status.
    4. Search for a Reservation.
    5. Exit.
Step 4: Handle User Choice
1. If the choice is 5: Exit the program.
2. If the choice is 1 or 2: Reserve a Seat
Determine the section (VIP for 1, Standard for 2) and corresponding seat array and size.
Prompt for user details:
Name: Use getValidString() to validate.
Genre: Use getValidString() to validate.
Age: Use a loop to ensure the input is a valid positive integer.
Find the first available seat in the selected section:
If a seat is available, mark it as reserved and save the reservation details:
Update names, genres, ages, sections, and seatNumbers arrays.
Increment userCount.
Display a reservation confirmation.
If the section is full:
Check availability in the alternate section.
If available, prompt the user to reserve in the alternate section.
If no seats are available in either section, display a message indicating full capacity.
3. If the choice is 3: View Seat Status
Display the reservation status (Reserved or Available) for all VIP and Standard seats.
4. If the choice is 4: Search for a Reservation
Prompt for the user’s name using getValidString().
Search for the name in the names array:
If found, display the corresponding reservation details.
If not found, display a "No reservation found" message.
5. If the choice is invalid: Display an error message.
Step 5: Repeat
1. Return to the main menu and allow the user to make another choice until they choose to exit.
Step 6: Exit the Program
1. Terminate the program when the user chooses 5.
   	

























