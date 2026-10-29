# App3 — Login & Registration App

**SOFTWARE** | **MOBILE APPLICATION** | **KOTLIN ‧ ANDROID STUDIO**

App3 is a simple Android application that demonstrates a basic user authentication flow, including registration, login validation, and a welcome screen. Developed using Kotlin and XML layouts, the application focuses on input validation, activity navigation, and passing user data between screens.

## 01. Project Overview

**App3** is a beginner-friendly Android application developed to demonstrate fundamental Android development concepts using Kotlin and XML.

### Objectives
- Implement a basic registration and login flow.
- Validate user input, including email format and password length.
- Navigate between activities using Android Intents.
- Transfer user information between activities using Parcelable.
- Display a personalized welcome message after successful login.

### Problem Statement

Understanding how to validate user input, navigate between screens, and transfer data between activities is an important foundation in Android application development.

### Solution

App3 provides a simple registration and login workflow with validation messages for empty fields, invalid email formats, and passwords shorter than eight characters. After successful login, the application displays a welcome message containing the registered user's name.

### Key Features
- **Registration:** Accepts the user's name, email address, and password.
- **Input Validation:** Checks required fields, email format, and minimum password length.
- **Login:** Compares the entered credentials with user data passed from registration.
- **Landing Page:** Displays a personalized welcome message.
- **Logout:** Returns the user to the login screen.
- **Activity Navigation:** Uses Android Intents to move between activities.
- **Parcelable Data Transfer:** Passes user information between activities.

### Project Scope and Limitations

This project demonstrates a basic authentication flow for learning purposes. User data is transferred between activities in memory and is not stored in a persistent database. Registration data is therefore not retained after the application restarts. The implementation is not intended for production authentication.

## 02. Tech Stack

| Category | Technology |
|---|---|
| Programming Language | Kotlin |
| UI Layout | XML |
| Development Environment | Android Studio |
| UI Components | Android Views, ConstraintLayout |
| Navigation | Android Intents |
| Data Transfer | Parcelable |
| Input Validation | Android Patterns API |
| Build System | Gradle |

## 03. Screenshots / Results

### Application Workflow

1. **Login Screen** — Provides email and password fields, a Login button, and navigation to registration.
2. **Registration Screen** — Collects the user's name, email address, and password.
3. **Input Validation** — Displays feedback when required fields are empty, the email format is invalid, or the password is shorter than eight characters.
4. **Login Validation** — Checks the submitted credentials against the user data received from registration.
5. **Landing Screen** — Displays a welcome message containing the registered user's name.
6. **Logout** — Returns the user to the login screen.

### Screenshots

**Home Screen**
![image](https://github.com/user-attachments/assets/5cf402f8-643c-4a8b-80ee-3dfe8fa01379)

**Login page display if password and email are empty**

![image](https://github.com/user-attachments/assets/f6740b58-3009-4a71-be30-178bc6ca4f57)


**Login page view if the email is invalid**

![image](https://github.com/user-attachments/assets/d24820d1-a911-4c08-a631-7e950679078a)

**Login page view if not registered yet**

![image](https://github.com/user-attachments/assets/167af7c1-7272-429d-9bb9-f287fc80abb5)

**Registration page view and if empty**

![image](https://github.com/user-attachments/assets/979cbf71-02fd-46cf-8d7f-583e17cabce1)

**The registration page display if the email format is wrong**

![image](https://github.com/user-attachments/assets/1bc1f6b2-8c32-416f-acc6-f93c51648ef2)

**Registration page view if the password is less than 8 characters long**

![image](https://github.com/user-attachments/assets/4381e014-0bd3-429d-9ad3-b1969f440b12)

**Login Page Display after registering, if the password is less than 8 characters**

![image](https://github.com/user-attachments/assets/d9553be7-64c5-4404-9eb9-4538b4d34cf0)


**Landing Page View if Login is Successful**

![image](https://github.com/user-attachments/assets/416671f5-3e95-4add-a022-0c0175ed8a84)

### Insight

App3 demonstrates the relationship between Kotlin activity classes and XML layout resources, as well as how user input can be validated and information transferred between activities.

### Usefulness

- Helps beginners understand Android activity navigation.
- Demonstrates form validation and user feedback.
- Introduces object transfer using Parcelable.
- Provides a foundation for applications with registration and login interfaces.

### Practical Application

App3 can be used as an Android Studio learning project, a programming practice exercise, or a starting point for a more complete authentication application.

## 04. Installation & Usage

### Prerequisites
- Android Studio.
- Android SDK compatible with the project configuration.
- Kotlin and Gradle support.
- Android Emulator or a physical Android device.

### Project Structure

```text
App3/
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── java/
│   │       │   └── com/
│   │       │       └── example/
│   │       │           └── app3/
│   │       │               ├── User.kt
│   │       │               ├── login.kt
│   │       │               ├── register.kt
│   │       │               └── landing.kt
│   │       ├── res/
│   │       │   └── layout/
│   │       │       ├── activity_login.xml
│   │       │       ├── activity_register.xml
│   │       │       └── activity_landing.xml
│   │       └── AndroidManifest.xml
│   └── build.gradle.kts
├── gradle/
├── build.gradle.kts
├── settings.gradle.kts
├── gradlew
├── gradlew.bat
└── README.md
```

### Installation

**1. Create the Android Studio project**

- Open Android Studio and select **New Project**.
- Choose **Empty Views Activity**.
- Set the project name to `App3`.
- Set the package name or namespace to `com.example.app3`.
- Select Kotlin as the programming language.
- Finish creating the project and wait for Gradle synchronization.
   ![image](https://github.com/user-attachments/assets/59d65576-2f1a-415c-9032-1f9fd5884e0e)

**2. Add Kotlin source files**

Place the following files in:

`app/src/main/java/com/example/app3/`

- `User.kt`
- `login.kt`
- `register.kt`
- `landing.kt`

Keep the package declaration consistent:

```kotlin
package com.example.app3
```

**3. Add XML layouts**

Place the following files in:

`app/src/main/res/layout/`

- `activity_login.xml`
- `activity_register.xml`
- `activity_landing.xml`

**4. Configure AndroidManifest.xml**

Register the `login`, `register`, and `landing` activities inside the existing `<application>` element. Configure `login` as the launcher activity using the `MAIN` action and `LAUNCHER` category. Like this:
Open App > manifests > AndroidManifest.xml > and then add this:
      
    ```  kotlin
   <activity
               android:name=".landing"
               android:exported="false" />
           <activity
               android:name=".register"
               android:exported="false" />
           <activity
               android:name=".login"
               android:exported="true"> <!-- Set TRUE & tambahkan intent-filter -->
               <intent-filter>
                   <action android:name="android.intent.action.MAIN" />
                   <category android:name="android.intent.category.LAUNCHER" />
               </intent-filter>
           </activity>

**5. Check Gradle configuration**

Ensure the app module includes compatible AppCompat and ConstraintLayout dependencies. The current `User.kt` implements Parcelable manually, so the `kotlin-parcelize` plugin is not required.

**6. Run the application**

- Wait for Gradle synchronization to finish.
- Select an emulator or connected Android device.
- Click **Run** in Android Studio.

### Usage Guide

1. Launch App3 and open the Login screen.
2. Select Register to open the registration screen.
3. Enter a name, valid email address, and password of at least eight characters.
4. Submit the registration form.
5. Log in using the registered credentials.
6. View the personalized welcome message.
7. Select Logout to return to Login.

### Notes

- Registration data is passed through an Intent and is not permanently stored.
- A fresh application launch starts without a previously registered account.
- This project is intended for learning purposes and does not implement a production authentication backend.
- The original Android Studio project configuration must be recreated if the Gradle files and project structure are missing.

