# Android Send SMS App

## Overview

This project is a simple Android application built using Android Studio that allows users to send SMS messages directly from the app. It demonstrates runtime permission handling and use of the `SmsManager` API.

---

## Features

* Send SMS to any mobile number
* Runtime permission request for sending SMS
* Input fields for phone number and message
* Simple and user-friendly interface
* Displays success and error messages using Toast

---

## Tech Stack

* Language: Java
* IDE: Android Studio
* Components Used:

  * `SmsManager`
  * `EditText`
  * `Button`
  * `Toast`
  * Runtime Permissions (`Manifest.permission.SEND_SMS`)

---

## How It Works

1. User enters **phone number** and **message**.
2. App checks if `SEND_SMS` permission is granted.
3. If not granted, it requests permission at runtime.
4. Once permission is granted, SMS is sent using:

   ```
   SmsManager.sendTextMessage()
   ```
5. Displays confirmation message after sending SMS.

---

## Setup Instructions

1. Open project in Android Studio
2. Add permission in `AndroidManifest.xml`:

   ```
   <uses-permission android:name="android.permission.SEND_SMS"/>
   ```
3. Run the app on a **real device** (SMS may not work on emulator)
4. Grant SMS permission when prompted

---

## Code Highlights

* `SmsManager.getDefault()` is used to send SMS
* `ActivityCompat.requestPermissions()` handles runtime permission
* `onRequestPermissionsResult()` processes user response
* Input validation ensures fields are not empty

---

## Learning Outcomes

* Understanding Android runtime permissions
* Working with SMS functionality
* Handling user input and validation
* Using system services like `SmsManager`
