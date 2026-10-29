# mp25--Assign3
## Aplikasi Login-Register Sederhana
File ini adalah file kt dan xml untuk project bernama App3 di android studio untuk menjalankan code ini:
1. Buka android studio pilih _new project_ lalu pilih _new activity_ beri nama app3 dan next.
2. Ubah tampilan dari PROJECT ke  ANDROID
   
   ![image](https://github.com/user-attachments/assets/59d65576-2f1a-415c-9032-1f9fd5884e0e)

4. lalu di bagian App > kotlin+java > com.example.app3 , masukan file "User.kt", "login.kt", "register.kt", "landing.kt".
   
   ![image](https://github.com/user-attachments/assets/9eb8c1f8-b54c-4abb-a327-ca6d0aeab0e2)

6. selanjutnya bagian App > res > Layout, masukan file "activity_login.xml", "activity_register.xml", "activity_landing.xml".

   ![image](https://github.com/user-attachments/assets/cebc8db2-a8ce-4254-9b0b-50f489fc0d54)

8. Buka lagi App > manifests > AndroidManifest.xml > tambahkan codingan berikut:
      
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


![image](https://github.com/user-attachments/assets/9f4b4947-31b1-4389-a37a-dd16d5cae82a)

10. selanjutnya di Gradle Script > pilih dan buka build.gradle.kts (Modul : app) dan tambahkan kodingan [ `id("kotlin-parcelize")` ]
    
   ![image](https://github.com/user-attachments/assets/854a8a47-6875-471d-879a-1bdf5b4bf1e1)
   
   ![image](https://github.com/user-attachments/assets/4ba0f4e4-e8d0-44d3-883c-fc5f09d37f0a)

12. Selanjutnya jalankan Aplikasi di android studio dengan memilih  Device Manager > pilih perangkat > Run
13. Selamat mencoba!

# Tampilan APP3

## Tampilan Awal
![image](https://github.com/user-attachments/assets/5cf402f8-643c-4a8b-80ee-3dfe8fa01379)

## Tampilan halaman login jik pw dan email kosong
![image](https://github.com/user-attachments/assets/f6740b58-3009-4a71-be30-178bc6ca4f57)

## Tampilan halaman login jika email tidak valid
![image](https://github.com/user-attachments/assets/d24820d1-a911-4c08-a631-7e950679078a)

## Tampilan halaman login jika belum registrasi
![image](https://github.com/user-attachments/assets/167af7c1-7272-429d-9bb9-f287fc80abb5)

## Tampilan halaman Registrasi dan jika kosong
![image](https://github.com/user-attachments/assets/979cbf71-02fd-46cf-8d7f-583e17cabce1)

## Tampilan halaman registrasi jika format email salah
![image](https://github.com/user-attachments/assets/1bc1f6b2-8c32-416f-acc6-f93c51648ef2)

## Tampilan halaman registrasi jika panjang password < 8 karakter
![image](https://github.com/user-attachments/assets/4381e014-0bd3-429d-9ad3-b1969f440b12)

## Tampilan Halaman Login setelah register, Jika panjang password < 8 Karakter
![image](https://github.com/user-attachments/assets/d9553be7-64c5-4404-9eb9-4538b4d34cf0)

## Tampilan Halamann Landingjika berhasil Login
![image](https://github.com/user-attachments/assets/416671f5-3e95-4add-a022-0c0175ed8a84)


# AppSign — Login & Registration App

**Mobile Application** | **Android Development** | **Kotlin, XML, Android Studio**

AppSign is a simple Android application that demonstrates a basic user authentication flow, including registration, login validation, and a welcome screen. Developed using Kotlin and XML layouts, the application focuses on input validation, activity navigation, and passing user data between screens.

## 01. Project Overview

**AppSign** is a beginner-friendly Android application developed to demonstrate the fundamental concepts of Android application development using Kotlin and XML.

### Objectives
- Implement a basic registration and login flow.
- Validate user input, including email format and password length.
- Navigate between activities using Android Intents.
- Transfer user information between activities using Parcelable.
- Display a personalized welcome message after successful login.

### Problem Statement

Applications commonly require users to enter account information and navigate between authentication screens. Understanding how to validate user input and transfer information between activities is an important foundation in Android development.

### Solution

AppSign provides a simple registration and login workflow with validation messages for empty fields, invalid email formats, and passwords shorter than eight characters. After successful login, the application displays a welcome message using the registered user's name.

### Key Features
- **Registration:** Accepts a name, email address, and password.
- **Input Validation:** Checks required fields, email format, and minimum password length.
- **Login:** Compares the entered email and password with the user data received from the registration flow.
- **Landing Page:** Displays a personalized welcome message.
- **Logout:** Returns the user to the login screen.
- **Activity Navigation:** Uses Android Intents to move between application screens.
- **Parcelable Data Transfer:** Transfers user information between activities.

### Project Scope and Limitations

This project demonstrates a basic authentication flow for learning purposes. User data is passed between activities in memory and is not stored in a persistent database. Consequently, registration is not retained after the application is restarted, and the implementation is not intended for production authentication.

## 02. Tech Stack

| Category | Technology |
|---|---|
| Programming Language | Kotlin |
| UI Layout | XML |
| Development Environment | Android Studio |
| Android UI Components | Android Views, ConstraintLayout |
| Navigation | Android Intents |
| Data Transfer | Parcelable |
| Input Validation | Android Patterns API |
| Build System | Gradle |

## 03. Screenshots / Results

### Application Workflow

1. **Login Screen** — Provides email and password fields, a Login button, and navigation to registration.
2. **Registration Screen** — Collects the user's name, email address, and password.
3. **Input Validation** — Displays feedback when fields are empty, the email format is invalid, or the password contains fewer than eight characters.
4. **Login Validation** — Checks the submitted credentials against the user data passed from registration.
5. **Landing Screen** — Displays a welcome message containing the registered user's name.
6. **Logout** — Returns the user to the login screen and clears the current activity stack.

### Screenshots

Place your actual application screenshots inside a `screenshots/` folder in the repository.

**Login Screen**

![AppSign Login Screen](screenshots/login.png)

**Registration Screen**

![AppSign Registration Screen](screenshots/register.png)

**Input Validation**

![AppSign Input Validation](screenshots/validation.png)

**Landing Page**

![AppSign Landing Page](screenshots/landing.png)

Replace the image paths above with the filenames of your actual screenshots.

### Insight

The project demonstrates how an Android application can validate user input, transfer data between activities, and manage navigation through a straightforward authentication workflow.

It also illustrates the relationship between Kotlin activity classes and XML layout resources.

### Usefulness

- Helps beginners understand Android activity lifecycles and navigation.
- Demonstrates basic form validation and user feedback.
- Provides an example of passing objects between activities with Parcelable.
- Serves as a foundation for applications that require registration and login interfaces.

### Practical Application

AppSign can be used as a learning project, an Android Studio practice exercise, or a starting point for developing a more complete authentication interface with persistent storage and secure authentication.

## 04. Installation & Usage

### Prerequisites

- Android Studio.
- Android SDK compatible with the project configuration.
- Kotlin and Gradle support configured through Android Studio.
- Android Emulator or a physical Android device.

### Project Structure

The following is the expected Android Studio project structure after recreating the project:

```text
AppSign/
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

The exact project structure may vary depending on the Android Studio version and project template.

### Recreating the Android Studio Project

Because the original Android Studio project configuration is no longer available, create a new project and restore the source files.

**1. Create a new project**

- Open Android Studio.
- Select **New Project**.
- Choose **Empty Views Activity** or a template that uses XML layouts.
- Set the project name to `AppSign`.
- Set the package name or namespace to `com.example.app3`.
- Choose Kotlin as the programming language.
- Finish creating the project and wait for Gradle synchronization.

**2. Add the Kotlin files**

Navigate to:

`app/src/main/java/com/example/app3/`

Place these four files in that directory:

- `User.kt`
- `login.kt`
- `register.kt`
- `landing.kt`

Ensure that each file retains the package declaration:

```kotlin
package com.example.app3
```

**3. Add the XML layout files**

Navigate to:

`app/src/main/res/layout/`

Place these three files in that directory:

- `activity_login.xml`
- `activity_register.xml`
- `activity_landing.xml`

The filenames must match the resources referenced by `setContentView()` in the Kotlin activities.

**4. Configure AndroidManifest.xml**

Open:

`app/src/main/AndroidManifest.xml`

Register the activities and configure the login screen as the launcher activity:

```xml
<application
    ... >

    <activity
        android:name=".landing"
        android:exported="false" />

    <activity
        android:name=".register"
        android:exported="false" />

    <activity
        android:name=".login"
        android:exported="true">

        <intent-filter>
            <action android:name="android.intent.action.MAIN" />
            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>

    </activity>

</application>
```

Keep the existing attributes generated by Android Studio, such as the application theme and label. Insert the activity declarations inside the existing `<application>` element rather than replacing the entire manifest.

**5. Check Gradle dependencies**

Ensure the app module includes AppCompat and ConstraintLayout dependencies compatible with your Android Studio project.

The Kotlin source shown here implements Parcelable manually, so the `kotlin-parcelize` plugin is not required for this particular implementation.

**6. Run the application**

- Wait for Gradle synchronization to finish.
- Open **Device Manager** and create or select an Android Emulator, or connect a physical device.
- Select the device in the toolbar.
- Click **Run** to build and launch AppSign.

### Usage Guide

1. Open the application on the Login screen.
2. Select Register to open the registration screen.
3. Enter a name, valid email address, and password of at least eight characters.
4. Submit the registration form.
5. Log in using the registered credentials.
6. View the personalized welcome message on the Landing screen.
7. Select Logout to return to Login.

### Important Notes

- The current implementation passes registration data through an Intent; it does not save account data permanently.
- A fresh application launch starts without a previously registered account.
- The project is a learning prototype and does not implement secure password storage or a production authentication backend.
- The Android Studio project configuration, including Gradle files and the manifest, must be recreated because the original project folder is missing.

