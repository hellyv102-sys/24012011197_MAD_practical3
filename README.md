📱 Practical-3: Implicit & Explicit Intent in Android
Aim

Create an Android application which demonstrates Implicit Intent and Explicit Intent using Kotlin in Android Studio.

Application Demo
🎥 Demo

This application demonstrates different Android Intent actions through simple buttons.

Functions Included:

🌐 Open Specific URL

📞 Make Call to Specific Number

📋 Open Call Log

🖼️ Open Gallery

📷 Open Camera

⏰ Set Alarm

🔐 Open Login Activity (Explicit Intent)

Add your screen recording here after uploading it to GitHub.

https://github.com/hellyv102-sys/Practical-3/blob/main/ScreenRecording.mp4
📝 Steps

Web Browser – Opens a website using an implicit intent.

Phone Call – Opens the dialer with a predefined phone number.

Call Log – Opens the device call history.

Gallery – Opens the phone gallery to select an image.

Camera – Launches the device camera application.

Set Alarm – Opens the alarm app and creates an alarm.

Login Navigation – Opens LoginActivity using an explicit intent.

Application Logic
1. Implicit Intent

Implicit Intent requests another application on the device to perform an action.

🌐 Open Website
val intent = Intent(Intent.ACTION_VIEW)
intent.data = Uri.parse("https://www.google.com")
startActivity(intent)

Explanation

ACTION_VIEW opens the URL in the default browser.

Uri.parse() converts the website link into a URI.

📞 Make Phone Call
val intent = Intent(Intent.ACTION_DIAL)
intent.data = Uri.parse("tel:9876543210")
startActivity(intent)

Explanation

ACTION_DIAL opens the phone dialer.

tel: is used to pass the phone number.

📋 Open Call Log
val intent = Intent(Intent.ACTION_VIEW)
intent.type = CallLog.Calls.CONTENT_TYPE
startActivity(intent)

Explanation

Opens the device call log using CallLog.Calls.CONTENT_TYPE.

🖼️ Open Gallery
val intent = Intent(Intent.ACTION_PICK)
intent.type = "image/*"
startActivity(intent)

Explanation

ACTION_PICK opens the gallery.

"image/*" allows selecting image files.

📷 Open Camera
val intent = Intent(MediaStore.ACTION_IMAGE_CAPTURE)
startActivity(intent)

Explanation

Opens the camera application to capture a photo.

⏰ Set Alarm
val intent = Intent(AlarmClock.ACTION_SET_ALARM)
intent.putExtra(AlarmClock.EXTRA_HOUR, 7)
intent.putExtra(AlarmClock.EXTRA_MINUTES, 30)
intent.putExtra(AlarmClock.EXTRA_MESSAGE, "Wake Up")
startActivity(intent)

Explanation

Creates an alarm at 7:30 AM.

EXTRA_MESSAGE sets the alarm label.

2. Explicit Intent

Explicit Intent opens a specific activity inside the same application.

🔐 Open Login Activity
val intent = Intent(this, LoginActivity::class.java)
startActivity(intent)

Explanation

Opens LoginActivity.

Used for navigation between activities in the app.

UI Details
Main Activity (activity_main.xml)

The home screen is created using ConstraintLayout.

Components Used

EditText for URL input.

EditText for Phone Number input.

Buttons for:

Open Website

Make Call

Open Call Log

Open Gallery

Open Camera

Set Alarm

Login Activity

Layout Features

ConstraintLayout for responsive UI.

Proper spacing and alignment for all buttons.

Easy-to-use interface.

Login Activity (activity_login.xml)

The login screen is opened using an Explicit Intent.

Components Used

ImageView for University Logo.

MaterialCardView for login form.

EditText for Email.

EditText for Password.

Button for Login.

TextView for Forgot Password.

Layout Features

Clean login interface.

Rounded CardView design.

Centered logo and login form.

Android Permissions Used

Add these permissions in AndroidManifest.xml.

<uses-permission android:name="android.permission.CALL_PHONE"/>
<uses-permission android:name="android.permission.CAMERA"/>

These permissions allow the application to access phone calling and camera features. 
