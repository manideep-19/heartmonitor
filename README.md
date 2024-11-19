Health Monitoring Application

This application monitors the user's heart rate using a smartphone's camera and flashlight. It also includes login and main activity functionalities.

Features

Heart Rate Measurement:

Uses the camera to measure the user's heart rate by detecting changes in the green channel intensity of the video frames.

Activates the flashlight during measurement for better accuracy.

User Authentication:

Login screen as the first activity.

Navigates to the main activity after successful login.

Includes a logout feature.

Prerequisites

Android Studio installed on your computer.

An Android device with a camera and flashlight.

Minimum SDK: 24 (Android 7.0)

Target SDK: 34 (Android 14)

Setup Instructions

1. Clone the Repository

Download or clone the project repository to your local machine.

git clone <repository-url>

2. Open the Project in Android Studio

Launch Android Studio.

Open the cloned project.

Sync the Gradle files when prompted.

3. Grant Necessary Permissions

Ensure the following permissions are included in your AndroidManifest.xml:

<uses-permission android:name="android.permission.CAMERA" />
<uses-permission android:name="android.permission.FLASHLIGHT" />

4. Configure the Application

The namespace and package name should match the provided build.gradle and AndroidManifest.xml settings:

android {
    namespace = "com.example.health"
    compileSdk = 34

    defaultConfig {
        applicationId = "com.example.health"
        minSdk = 24
        targetSdk = 34
        versionCode = 1
        versionName = "1.0"
    }
}

5. Build and Run the Application

Connect your Android device or use an emulator.

Build and run the application from Android Studio.

Grant camera permissions when prompted.

Application Workflow

1. Login Activity

The application starts with a login screen.

New users can navigate to a sign-up page to create an account.

Valid login credentials redirect the user to the main activity.

2. Main Activity

Displays the main features of the application.

Includes an option to measure the heart rate.

Logout functionality to return to the login screen.

3. Heart Monitor Activity

Accessed from the main activity.

Requires the user to place their finger on the camera and flashlight.

Displays the estimated heart rate in beats per minute (BPM).

Key Files

Java Files

LoginActivity.java: Handles user login.

SignUpActivity.java: Manages user sign-up functionality.

MainActivity.java: The main screen after login.

HealthMonitorActivity.java: Measures and displays heart rate.

XML Layout Files

activity_login.xml: Layout for login activity.

activity_main.xml: Layout for the main activity.

activity_health_monitor.xml: Layout for heart rate monitoring.

Troubleshooting

Common Issues

Black Screen During Heart Rate Measurement:

Ensure the camera permission is granted.

Check if the flashlight is functioning properly.

Heart Rate Not Detected:

Place your finger gently over the camera and flashlight.

Ensure there is minimal movement during measurement.

Build Errors:

Verify that the compileSdk and targetSdk versions match.

Ensure all dependencies are resolved by syncing the Gradle files.
