

Step 1: Install XAMPP

Install XAMPP on your system.
Step 2: Move PHP File

Move the PHP.RAR file You can find it in the project code above to the following path: C:\xampp\htdocs.
Step 3: Start MySQL Server

Run the MySQL server.
Step 4: Create Database

Create a database named "android" with a table named "users."
Step 5: Test API Connection with Postman

Ensure API connectivity using Postman by sending a POST request to:
Key = username, Value = ahmed
Key = email, Value = ahmed@example.com
Key = password, Value = 123456
Post to http://localhost/android/registerUser.php
If you receive the following response:
{"error":false,"message":"user registered successfully"}
it indicates that the API is functioning properly.
Step 6: Download the Project to Android Studio

Download the project to Android Studio and ensure that the Volley library is installed in the build.gradle:
gradle
Copy code
dependencies {
    implementation("com.android.volley:volley:1.2.0")
}
Step 7: Adjust the URL for Emulator

If you're working with an emulator and facing connection issues, modify the url_register value in the Constants class:
Open Command Prompt by pressing Windows Key + R.
Type ipconfig in the Command Prompt and press Enter.
Look for "IPv4 Address" and use it in the server URL. For instance:
http://192.168.1.2/android/registerUser.php
