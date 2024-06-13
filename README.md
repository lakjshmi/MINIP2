# Intoxicated Driving Case Booking App

## Technologies Used
1. HTML: Structures the app’s interface, creates forms, and defines the content.
2. CSS: Styles the app, including layout, color, and typography, ensuring a visually appealing and user-friendly interface.
3. JavaScript: Implements the app’s functionality, including form validation, event handling, and interactions with Firebase.
4. Firebase: Provides real-time database services for storing, retrieving, and managing data related to vehicles and their statuses. It includes:
    - Firebase App: Initializes the Firebase app with the provided configuration.
    - Firebase Database: Provides real-time database capabilities.
    - Firebase Analytics: Tracks user interactions and usage patterns within the app.

## Key Features
1. Vehicle Number Validation:
    - Users enter a vehicle number, which is validated against a predefined format using regular expressions.
    - If the vehicle number matches the format, the app checks if the vehicle exists in the Firebase database.

2. New Vehicle Handling:
    - If the vehicle number does not exist in the database, the app redirects the user to a new vehicle form.
    - The new vehicle form collects details such as vehicle number, driver’s license number, driver’s name, vehicle type, and status (Drunk, Sober, Safe).
    - The form data is validated to ensure all fields are filled.
    - Upon form submission, the data is saved to the Firebase database.

3. Recurring Vehicle Handling:
    - If the vehicle number already exists in the database, the app redirects the user to a form for updating the vehicle’s status.
    - The form allows the user to select the current status of the vehicle (Drunk, Sober, Safe).
    - The status update is saved to the Firebase database, including a timestamp for tracking the history of statuses.

4. Navigation:
    - The app includes navigation buttons allowing users to return to the main page from both the new vehicle and recurring vehicle pages.
    - It ensures a seamless user experience by maintaining the state of vehicle numbers across different pages.

5. User Feedback:
    - The app provides alerts and notifications to inform users of successful data submissions and any errors encountered during the process.
    - It ensures that users are aware of the actions being performed and any issues that need to be addressed.

## Description of HTML Files
1. index.html:
    - Contains an input field for entering the vehicle number and a button to check the format.
    - Validates the vehicle number format and determines whether the vehicle is new or recurring based on Firebase data.
  
2. newVehicle.html:
    - Displays a form for entering details of a new vehicle.
    - Includes fields for vehicle number, driver’s license number, name, vehicle type, and status.
    - Provides a button to save the data and a back button to return to the main page.
  
3. reccuringVehicle.html:
    - Displays a form for updating the status of an existing vehicle.
    - Auto-fills the vehicle number from the URL if available.
    - Includes radio buttons for selecting the vehicle’s status and a button to save the status.
    - Provides a back button to return to the main page.

## Description of CSS
- Defines the overall layout and styling for the app.
- Provides styles for input fields, buttons, and forms, ensuring a consistent and user-friendly design.
- Includes custom styles for different statuses (Drunk, Sober, Safe) using colors and highlights to distinguish between them.
