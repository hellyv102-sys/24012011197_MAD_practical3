# 📱 Practical-3: Implicit & Explicit Intent in Android




## 🎯 Aim

Create an Android application that demonstrates **Implicit Intent** and **Explicit Intent** using Kotlin in Android Studio.

---

# 📲 Application Demo

### Features Demonstrated

| Intent Feature | Description |
|----------------|-------------|
| 🌐 Open Website | Opens a specific URL in the browser. |
| 📞 Make Call | Opens the phone dialer with a phone number. |
| 📋 Call Log | Opens the device call history. |
| 🖼️ Gallery | Opens the image gallery. |
| 📷 Camera | Launches the device camera. |
| ⏰ Set Alarm | Creates a new alarm with time and message. |
| 🔐 Login Activity | Navigates to Login Activity using Explicit Intent. |

### 🎥 Screen Recording

> Add your screen recording after uploading it to GitHub.

```text
https://github.com/hellyv102-sys/Practical-3/blob/main/ScreenRecording.mp4
```

---

# 📝 Implementation Steps

| Step | Operation |
|------|-----------|
| **1** | Open a website using an Implicit Intent. |
| **2** | Open the phone dialer with a specific number. |
| **3** | Open the Call Log application. |
| **4** | Open the Gallery to select an image. |
| **5** | Launch the Camera application. |
| **6** | Set an Alarm with predefined time and label. |
| **7** | Navigate to Login Activity using Explicit Intent. |

---

# ⚙️ Application Logic

## 🔹 Implicit Intent

Implicit Intent is used to perform actions using other applications available on the Android device.

### 🌐 Open Website

```kotlin
val intent = Intent(Intent.ACTION_VIEW)
intent.data = Uri.parse("https://www.google.com")
startActivity(intent)
```

**Purpose:** Opens Google in the default web browser.

---

### 📞 Make Phone Call

```kotlin
val intent = Intent(Intent.ACTION_DIAL)
intent.data = Uri.parse("tel:9876543210")
startActivity(intent)
```

**Purpose:** Opens the dialer with the given phone number.

---

### 📋 Open Call Log

```kotlin
val intent = Intent(Intent.ACTION_VIEW)
intent.type = CallLog.Calls.CONTENT_TYPE
startActivity(intent)
```

**Purpose:** Opens the device Call Log.

---

### 🖼️ Open Gallery

```kotlin
val intent = Intent(Intent.ACTION_PICK)
intent.type = "image/*"
startActivity(intent)
```

**Purpose:** Opens the Gallery for selecting an image.

---

### 📷 Open Camera

```kotlin
val intent = Intent(MediaStore.ACTION_IMAGE_CAPTURE)
startActivity(intent)
```

**Purpose:** Opens the Camera application.

---

### ⏰ Set Alarm

```kotlin
val intent = Intent(AlarmClock.ACTION_SET_ALARM)
intent.putExtra(AlarmClock.EXTRA_HOUR, 7)
intent.putExtra(AlarmClock.EXTRA_MINUTES, 30)
intent.putExtra(AlarmClock.EXTRA_MESSAGE, "Wake Up")
startActivity(intent)
```

**Purpose:** Creates an alarm at **7:30 AM** with the label **Wake Up**.

---

## 🔹 Explicit Intent

Explicit Intent is used to open another Activity inside the same application.

### 🔐 Open Login Activity

```kotlin
val intent = Intent(this, LoginActivity::class.java)
startActivity(intent)
```

**Purpose:** Navigates from `MainActivity` to `LoginActivity`.

---

# 🎨 User Interface (UI)

## 🏠 Main Activity (`activity_main.xml`)

The home screen is designed using **ConstraintLayout**.

### Components Used

- EditText for Website URL.
- EditText for Phone Number.
- Seven Buttons for different Intent operations.

### Buttons Available

- 🌐 Open Website
- 📞 Make Call
- 📋 Call Log
- 🖼️ Gallery
- 📷 Camera
- ⏰ Set Alarm
- 🔐 Login Activity

---

## 🔑 Login Activity (`activity_login.xml`)

A simple login screen created using **Explicit Intent**.

### Components Used

- University Logo (`ImageView`)
- `MaterialCardView`
- Email `EditText`
- Password `EditText`
- Login Button
- Forgot Password TextView

---

# 🔒 Android Permissions

Add the following permissions inside **AndroidManifest.xml**.

```xml
<uses-permission android:name="android.permission.CALL_PHONE"/>
<uses-permission android:name="android.permission.CAMERA"/>
```

These permissions allow the application to access phone calling and camera features.

---

# 📸 Output Screenshots

| Screen | Screenshot |
|--------|------------|
| 🏠 Home Screen | `Screenshots/home.png` |
| 🌐 Website | `Screenshots/website.png` |
| 📞 Phone Call | `Screenshots/call.png` |
| 📋 Call Log | `Screenshots/calllog.png` |
| 🖼️ Gallery | `Screenshots/gallery.png` |
| 📷 Camera | `Screenshots/camera.png` |
| ⏰ Set Alarm | `Screenshots/alarm.png` |
| 🔐 Login Activity | `Screenshots/login.png` |

---

# 📂 Project Structure

```text
Practical-3/
│── app/
│── java/
│   ├── MainActivity.kt
│   └── LoginActivity.kt
│── res/
│   ├── layout/
│   │   ├── activity_main.xml
│   │   └── activity_login.xml
│   ├── drawable/
│   └── mipmap/
│── AndroidManifest.xml
│── Screenshots/
│── README.md
```

---

# 🛠️ Tools & Technology

| Software | Technology |
|----------|------------|
| Android Studio | Kotlin |
| XML | ConstraintLayout |
| Android SDK | Intents |

---
# 📸 Output Screenshots

## 🏠 Home Screen

![Home Screen](Screenshots/home.png)

---

## 🌐 Open Website

![Open Website](Screenshots/website.png)

---

## 📞 Make Phone Call

![Make Phone Call](Screenshots/call.png)

---

## 📋 Open Call Log

![Call Log](Screenshots/calllog.png)

---

## 🖼️ Open Gallery

![Open Gallery](Screenshots/gallery.png)

---

## 📷 Open Camera

![Open Camera](Screenshots/camera.png)

---

## ⏰ Set Alarm

![Set Alarm](Screenshots/alarm.png)

---

## 🔐 Login Activity

![Login Activity](Screenshots/login.png)

# ✅ Result

The Android application was successfully developed to demonstrate both **Implicit Intent** and **Explicit Intent** in Android using Kotlin. The application successfully performs website browsing, phone calling, opening call logs, gallery, camera, alarm setting, and navigation to the Login Activity.
