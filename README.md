Todo App
A simple task management app built with Flutter that allows users to create, manage, and categorize tasks. The app supports three categories: Personal, College, and Office tasks. It uses Firebase Firestore for data storage and Flutter for the frontend.

Features
Task Categories: Create and manage tasks in three categories - Personal, College, and Office.
Task Creation: Add new tasks with a description.
Task Completion: Mark tasks as complete with a checkbox.
Real-Time Updates: Tasks are synced in real-time from Firestore.
Simple UI: A clean and easy-to-use interface with a floating action button for adding tasks.
Prerequisites
Before running this project, make sure you have the following installed:

Flutter (version >= 3.0)
Firebase Project with Firestore setup
An Android/iOS simulator or a physical device to run the app
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/todo-app.git
cd todo-app
Install dependencies: Make sure you have Flutter installed and run:

bash
Copy code
flutter pub get
Configure Firebase:

Create a Firebase project at Firebase Console.
Set up Firestore in your Firebase project.
Download the google-services.json file for Android or GoogleService-Info.plist for iOS.
Place the google-services.json file in the android/app directory for Android or GoogleService-Info.plist in the ios/Runner directory for iOS.
Run the app: Once everything is set up, you can run the app using:

bash
Copy code
flutter run
App Usage:

On the home screen, you can switch between Personal, College, and Office task categories.
Use the floating action button to add new tasks.
Each task can be checked off when completed.
Tasks are stored in Firebase Firestore and synced across devices in real-time.
Project Structure
lib/main.dart: Entry point of the app, handles UI layout and task management.
lib/db_service/database.dart: Contains methods for interacting with Firebase Firestore, including adding tasks and marking them as complete.
How it Works
Task Categories: The app has three categories (Personal, College, Office), and users can toggle between them by clicking the category names at the top of the screen.

Task Management: When the user presses the floating action button, an input box appears where they can enter the task description. Once the task is created, it will appear in the current selected category.

Task Completion: Users can mark tasks as complete by checking the checkbox next to each task. The app will remove the task from the list after a 2-second delay.

Firestore Integration: The app uses Firebase Firestore to store tasks and update the UI in real time. When a task is added or updated, it reflects on all devices that have the app open.

Firebase Setup
To configure Firebase:

Firebase Firestore: Set up Firestore in your Firebase project and enable Cloud Firestore for reading/writing data.
Authentication (Optional): If you want to implement user authentication, you can use Firebase Auth to allow users to log in before accessing tasks.
Contributing
Contributions are welcome! If you would like to improve this app or fix bugs, please feel free to submit a pull request.

Steps to contribute:
Fork this repository.
Create a new branch (git checkout -b feature/your-feature-name).
Make your changes.
Commit your changes (git commit -m 'Add your feature').
Push to your branch (git push origin feature/your-feature-name).
Open a pull request.
