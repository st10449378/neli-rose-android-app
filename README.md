# Neli-Rose App

### Android-Based Care Management and Communication Application

![Android](https://img.shields.io/badge/Platform-Android-green)
![Kotlin](https://img.shields.io/badge/Language-Kotlin-purple)
![Firebase](https://img.shields.io/badge/Backend-Firebase-orange)
![Version](https://img.shields.io/badge/Version-1.0-blue)
![Status](https://img.shields.io/badge/Status-In%20Development-yellow)

---

##  Project Overview

**Neli-Rose App** is an Android mobile application developed to provide a convenient digital platform for managing care-related activities, schedules, health information, announcements, and communication.

The application aims to improve accessibility, organisation, and communication by bringing essential features together in one user-friendly mobile platform.

Developed using **Android Studio and Kotlin**, the application incorporates Firebase services, local database storage, and modern Android development technologies.

The project focuses on creating a functional, accessible, and reliable application that supports users in managing important information and staying connected.

---

##  Project Objectives

The main objectives of the Neli-Rose App are to:

- Develop an interactive Android mobile application.
- Provide secure user registration and authentication.
- Allow users to access and manage relevant information.
- Improve communication through announcements.
- Support real-time updates using Firebase.
- Provide access to health and care-related information.
- Organise schedules and daily activities.
- Implement local and cloud-based data management.
- Create a simple and accessible user interface.
- Improve application reliability through testing and continuous integration.

---

##  Application Features

###  User Registration and Login

The application includes authentication functionality designed to provide secure access.

Features include:

- User registration.
- Email and password authentication.
- Google Sign-In integration.
- Firebase Authentication.
- User session management.
- Login validation.
- Authentication error handling.

**Development note:** Authentication functionality is undergoing further testing and improvement, particularly Google Sign-In and verification behaviour.

###  Home Dashboard

The home dashboard serves as the main navigation point.

It provides access to the application's primary sections, including:

- Home
- Health
- Activities
- Schedule
- Contact
- Announcements
- Settings

The dashboard is designed to make navigation simple and convenient.

###  Health Management

The Health section provides access to health-related functionality.

The project includes components for:

- Health information.
- Care-related data.
- Recording health measurements.
- Processing recorded vital information.

These features aim to support better organisation and accessibility of health-related records.

###  Schedule Management

The Schedule section is designed to help users organise important activities and planned events.

Its purpose is to support:

- Daily planning.
- Schedule organisation.
- Access to planned activities.
- Improved time management.

###  Activities

The Activities section provides a dedicated area for activity-related information.

It is intended to help users access and manage relevant activities within the application.

###  Announcements

The application includes an announcements feature integrated with Firebase Firestore.

The feature is designed to allow authenticated users to:

- Access announcements.
- Add new announcements.
- View announcements created by other users.
- Receive updated announcement information through Firestore's real-time data listeners.

Announcements are stored in a shared Firestore collection.

This allows information to be made available across authenticated users, subject to the configured database security rules.

### Notifications

The project includes Firebase Cloud Messaging integration.

This provides a foundation for push notification functionality.

The notification system is intended to improve communication by supporting timely delivery of important updates.

Notification delivery and permissions require testing on supported Android devices.

###  Settings

The application includes a Settings section for managing supported application preferences.

The settings functionality is intended to improve the overall user experience and provide greater control over application behaviour.

---

##  Technologies Used

The following technologies and development tools are used in the project.

| Technology | Purpose |
|---|---|
| Kotlin | Android application development |
| Android Studio | Development environment |
| Android SDK | Android platform functionality |
| Firebase Authentication | User authentication |
| Firebase Firestore | Cloud database and real-time updates |
| Firebase Cloud Messaging | Push notification infrastructure |
| Room Database | Local data persistence |
| Retrofit | API communication |
| OkHttp | HTTP networking |
| Gson | JSON conversion |
| Google Sign-In | Google account authentication |
| WorkManager | Background task management |
| XML | Android user interface layouts |
| Gradle | Dependency management and builds |
| GitHub | Source code version control |
| GitHub Actions | Continuous integration |
| JUnit | Unit testing |
| Espresso | Android UI testing |

---

## Project Architecture

The application follows a modular Android project structure.

The main components include:

**User Interface**

Responsible for displaying information and allowing users to interact with the application.

**Authentication**

Handles user registration, login, and authentication-related operations.

**Local Database**

Uses Room Database for local data storage and retrieval.

**Cloud Database**

Uses Firebase Firestore to support cloud-based data management.

**API Communication**

Uses Retrofit and OkHttp to communicate with external services.

**Notifications**

Uses Firebase Cloud Messaging components to support notification functionality.

**Background Processing**

Uses WorkManager to support background operations.

---

##  Project Structure

```text
NeliRoseApp/
│
├── .github/
│   └── workflows/
│       └── main.yml
│
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/
│   │   │   │   └── com/example/neli_roseapp/
│   │   │   │       ├── MainActivity.kt
│   │   │   │       ├── LoginActivity.kt
│   │   │   │       ├── SignUpActivity.kt
│   │   │   │       ├── HomeFragment.kt
│   │   │   │       ├── HealthFragment.kt
│   │   │   │       ├── ActivitiesFragment.kt
│   │   │   │       ├── ScheduleFragment.kt
│   │   │   │       ├── ContactFragment.kt
│   │   │   │       ├── AnnouncementsActivity.kt
│   │   │   │       ├── SettingsActivity.kt
│   │   │   │       ├── FcmHelper.kt
│   │   │   │       ├── VitalsRecorder.kt
│   │   │   │       ├── VitalsParser.kt
│   │   │   │       │
│   │   │   │       ├── api/
│   │   │   │       │   ├── ApiClient.kt
│   │   │   │       │   ├── ApiModels.kt
│   │   │   │       │   └── NeliApiService.kt
│   │   │   │       │
│   │   │   │       └── db/
│   │   │   │           ├── Daos.kt
│   │   │   │           ├── Entities.kt
│   │   │   │           └── NeliDatabase.kt
│   │   │   │
│   │   │   ├── res/
│   │   │   │   ├── drawable/
│   │   │   │   └── layout/
│   │   │   │
│   │   │   └── AndroidManifest.xml
│   │   │
│   │   ├── test/
│   │   └── androidTest/
│   │
│   ├── build.gradle.kts
│   └── google-services.json
│
├── gradle/
├── gradlew
├── gradlew.bat
└── README.md
```

---

##  Installation and Setup

### Prerequisites

Before running the application, ensure that you have:

- Android Studio installed.
- Android SDK configured.
- Java Development Kit (JDK) 17 for the build environment.
- An Android emulator or physical Android device.
- An internet connection for Firebase functionality.
- Access to the appropriate Firebase project configuration.

The project currently specifies:

- Minimum Android SDK: 26
- Target Android SDK: 37
- Compile Android SDK: 37

### Step 1: Clone the Repository

Open a terminal and execute:

```bash
git clone https://github.com/st10449378/neli-rose-android-app.git
```

### Step 2: Open the Project

1. Launch Android Studio.
2. Select **Open**.
3. Navigate to the cloned repository.
4. Select the Android project folder containing the Gradle settings.
5. Allow Android Studio to synchronise the project.

### Step 3: Configure Firebase

The application uses Firebase services.

To configure Firebase:

1. Open the Firebase Console.
2. Create or select the appropriate Firebase project.
3. Register the Android application.
4. Use the package name:

```text
com.example.neli_roseapp
```

5. Download the Firebase configuration file.
6. Place the file in:

```text
app/google-services.json
```

7. Enable the required Firebase Authentication providers.
8. Configure Cloud Firestore.
9. Configure Firebase Cloud Messaging as required.
10. Apply appropriate Firestore security rules.

For Google Sign-In, ensure the required application signing certificate fingerprints and OAuth configuration are correctly registered.

### Step 4: Build the Application

In Android Studio:

1. Select **Build**.
2. Click **Make Project**.
3. Wait for Gradle to complete.
4. Resolve any configuration or dependency errors.

Alternatively, use:

```bash
./gradlew build
```

On Windows:

```bash
gradlew.bat build
```

### Step 5: Run the Application

1. Connect an Android device or start an emulator.
2. Enable USB debugging when using a physical device.
3. Select the device in Android Studio.
4. Click **Run**.
5. Wait for the application to install and launch.

---

## Firebase Integration

Firebase is used to support authentication, cloud data storage, and notification functionality.

### Firebase Authentication

Provides the infrastructure for:

- Email and password authentication.
- Google authentication.
- User identification.
- Authentication session management.

### Cloud Firestore

Provides cloud-based data storage.

The announcements feature uses the following collection:

```text
announcements
```

Firestore snapshot listeners support real-time updates when announcement documents change.

### Firebase Cloud Messaging

Provides the infrastructure required for push notifications.

Additional configuration and device testing may be required to verify end-to-end notification delivery.

---

## Testing

Testing is an important part of the development process.

The project includes Android testing dependencies for JUnit and Espresso.

### Unit Testing

JUnit is included to support testing application logic.

Unit tests can be executed using:

```bash
./gradlew test
```

### Instrumented Testing

Android instrumented tests can be executed on a connected device or emulator using:

```bash
./gradlew connectedAndroidTest
```

### Functional Testing

The following functionality should be verified:

| Feature | Testing Focus |
|---|---|
| Registration | Account creation and validation |
| Login | Successful authentication |
| Google Sign-In | Google authentication flow |
| Announcements | Creating and retrieving announcements |
| Real-time Updates | Synchronisation between users |
| Notifications | Permission handling and delivery |
| Navigation | Movement between application screens |
| Room Database | Local storage and retrieval |
| API Connection | Successful communication and error handling |
| Settings | Saving and applying supported preferences |

**Note:** The presence of testing tools does not indicate that every test has passed. Authentication, notifications, and server connectivity remain important areas for further verification.

---

##  GitHub Actions and Continuous Integration

The repository includes a GitHub Actions workflow.

Workflow location:

```text
.github/workflows/main.yml
```

The workflow is configured to run when code is pushed to the `main` or `master` branch and when pull requests target those branches.

### Current Workflow

The workflow performs the following operations:

1. Checks out the repository.
2. Configures JDK 17.
3. Enables Gradle caching.
4. Grants execution permission to the Gradle wrapper.
5. Runs the Gradle build command.

The main build command is:

```bash
./gradlew build
```

### Continuous Integration Objectives

GitHub Actions helps developers:

- Detect build failures.
- Identify compilation problems.
- Validate project changes.
- Improve code reliability.
- Maintain consistent builds.

### APK Generation

A debug APK can be generated locally using:

```bash
./gradlew assembleDebug
```

The generated APK is normally located at:

```text
app/build/outputs/apk/debug/app-debug.apk
```

**Important:** The current GitHub Actions workflow performs a Gradle build but does not explicitly publish the APK as a downloadable GitHub Actions artifact.

Uploading APK artifacts can be added as a future workflow improvement.

---

## Security Considerations

Security is an important requirement for applications handling user information.

The project uses Firebase Authentication and supports cloud-based data storage.

Recommended security practices include:

- Requiring authentication for protected features.
- Applying Firebase Firestore security rules.
- Restricting access to sensitive information.
- Validating user input.
- Avoiding hardcoded passwords and private credentials.
- Using secure network communication.
- Testing authentication and session handling.
- Keeping dependencies updated.
- Applying appropriate access controls to shared data.

Sensitive health-related information should be protected through suitable authentication, authorisation, and data-handling measures.

---

## User Interface Design

The application uses Android XML layouts to create its interface.

The design aims to provide:

- Simple navigation.
- Readable information.
- Clearly labelled controls.
- Organised screens.
- Consistent interface components.
- An accessible user experience.

The application separates functionality into dedicated screens and fragments to improve organisation and usability.

---

##  Future Improvements

The following improvements are planned or recommended for future development:

### Authentication Improvements

- Resolve Google Sign-In issues.
- Improve email and password login reliability.
- Review verification handling.
- Improve authentication error messages.

### Notification Improvements

- Complete end-to-end notification testing.
- Improve notification delivery reliability.
- Support announcements with timely notifications.

### Database Improvements

- Strengthen Firebase security rules.
- Improve data validation.
- Review user-specific data access.
- Improve synchronisation and error handling.

### Testing Improvements

- Expand automated unit tests.
- Add additional instrumented tests.
- Test authentication failure scenarios.
- Verify server connectivity.
- Improve error reporting.

### Continuous Integration Improvements

- Add automatic APK artifact uploads.
- Improve automated build validation.
- Expand testing within GitHub Actions.
- Support future release builds.

### User Experience Improvements

- Improve loading indicators.
- Provide clearer feedback messages.
- Improve offline handling.
- Enhance navigation consistency.
- Continue accessibility improvements.

---

##  Development Status

**Current Version:** 1.0

**Project Status:** Active Development

The application contains implementations for authentication, navigation, care-related functionality, announcements, local database storage, API communication, and Firebase integration.

Some features require additional configuration, debugging, or testing before they can be considered production-ready.

The current development priorities include improving authentication reliability, validating server connectivity, and completing notification testing.

---

## Development Tools and Resources

The project uses the following development resources:

- Android Studio
- Kotlin
- Android SDK
- Firebase
- Git
- GitHub
- GitHub Actions
- Gradle
- JUnit
- Espresso

These technologies support application development, data management, testing, and version control.

---

## Project Repository

**Project Name:** Neli-Rose App

**Platform:** Android

**Programming Language:** Kotlin

**Version:** 1.0

**Repository:**

https://github.com/st10449378/neli-rose-android-app

---

##   Conclusion

The Neli-Rose App demonstrates the development of an Android application that integrates multiple technologies to provide a centralised platform for care-related information, communication, and daily organisation.

By combining Kotlin, Firebase, Room Database, and Android development components, the project establishes a foundation for a scalable and maintainable mobile application.

Continued development will focus on improving reliability, strengthening security, expanding automated testing, and refining the user experience.

---

**Neli-Rose App | Android Application | Version 1.0**

*Developed using Kotlin, Android Studio, and Firebase.*

Video link:https://drive.google.com/file/d/1AOb5Aq7qgv9LlbMBq9Nn594rfRvYRTw5/view?usp=drivesdk
