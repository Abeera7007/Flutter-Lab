# 🐦 Flutter Lab — Setup

### Lecture 01 • From `flutter doctor` to a working Flutter environment

> **Mission:** Get the complete Flutter + Android development environment ready before writing our first real app.

---

# 🧭 What Are We Setting Up?

Before writing Flutter code, we need several pieces working together.

Think of the development environment as a chain:

```text
                    👩‍💻 YOU
                      │
                      ▼
                 Dart / Flutter
                      │
                      ▼
                 Flutter SDK
                      │
                      ▼
                Android SDK
                      │
                      ▼
             Android Development Tools
                      │
                      ▼
             Emulator / Physical Phone
                      │
                      ▼
                  📱 APP
```

If one important part is missing, Flutter may not be able to build or run the application correctly.

---

# 🧠 Before We Install Anything

## What is Flutter?

**Flutter** is a UI toolkit/framework used to build applications with the **Dart programming language**.

Instead of creating completely separate UI code for different platforms, Flutter allows us to build applications using a shared Flutter codebase.

```text
             Flutter + Dart
                   │
        ┌──────────┼──────────┐
        ▼          ▼          ▼
     Android      iOS       Other
```

---

# 📦 What is an SDK?

### SDK = Software Development Kit

An SDK is a collection of tools, libraries, APIs, and other resources needed to develop software.

We'll encounter multiple SDKs during this course.

### Flutter SDK

Provides the tools needed to:

* Create Flutter projects
* Run applications
* Build applications
* Debug applications
* Manage Flutter commands
* Work with Flutter packages

### Android SDK

Provides Android-specific:

* APIs
* Build tools
* Platform tools
* Emulator components
* Command-line tools

So:

```text
Flutter SDK
      +
Android SDK
      ↓
Flutter Android Development
```

---

# 💻 System Requirements

The lecture recommends approximately:

```text
RAM:       8 GB minimum
CPU:       Core i5-class / equivalent
Storage:   Enough space for Flutter,
           Android Studio, SDKs & emulator
```

> ⚠️ These are practical course recommendations, not universal hard requirements. Actual requirements vary depending on your operating system, Android Studio version, emulator configuration, and whether you use a physical device.

### Why does RAM matter?

Android Studio + Flutter tooling + an Android emulator can consume a significant amount of memory.

For example:

```text
Android Studio
      +
Flutter tools
      +
Browser
      +
Android Emulator
      ↓
      🧠 RAM usage
```

A physical Android device can reduce the need to run a heavy emulator.

---

# 🐦 Step 01 — Download Flutter SDK

Download the Flutter SDK for your operating system.

After downloading it, we need to **extract** it.

You can use:

* Windows built-in extraction
* WinRAR
* 7-Zip

---

# 📂 Step 02 — Choose an Installation Location

The lecture recommends using a location such as:

```text
D:\flutter
```

Your folder structure should look approximately like:

```text
D:\
└── flutter\
    ├── bin\
    ├── dev\
    ├── packages\
    └── ...
```

The exact contents may differ between Flutter versions.

### Why do we care about the location?

Because we'll need to tell Windows where Flutter's executable tools are located.

Specifically:

```text
D:\flutter\bin
```

---

# ⚠️ Avoid Confusing Nested Folders

After extraction, check that you don't accidentally have:

```text
D:\flutter\flutter\bin
```

when you intended:

```text
D:\flutter\bin
```

The important thing is:

> Find the folder that actually contains Flutter's executable tools.

---

# 🌎 Step 03 — What Are Environment Variables?

An **environment variable** is a value maintained by the operating system that applications and command-line tools can access.

One of the most important variables we'll use is:

```text
PATH
```

---

# 🛣️ What is PATH?

PATH tells Windows:

> **"When the user types a command, these are the locations you should search for it."**

Imagine Flutter is installed here:

```text
D:\flutter\bin
```

but Windows doesn't know that location exists.

You type:

```bash
flutter
```

Windows essentially says:

```text
"Where is flutter.exe?"
```

If the Flutter `bin` directory is in PATH:

```text
You
 ↓
flutter
 ↓
Windows searches PATH
 ↓
D:\flutter\bin
 ↓
Flutter found ✅
```

Without it:

```text
You
 ↓
flutter
 ↓
Windows searches known PATH locations
 ↓
Flutter not found ❌
```

---

# 🛠️ Step 04 — Add Flutter to PATH

On Windows:

### 1. Search for:

```text
Environment Variables
```

Open:

> **Edit the system environment variables**

Then select:

> **Environment Variables**

---

### 2. Find `Path`

Locate the `Path` variable.

Select:

```text
Path
```

then:

```text
Edit
```

---

### 3. Add Flutter's `bin` folder

Select:

```text
New
```

and add the path to your Flutter `bin` directory.

For example:

```text
D:\flutter\bin
```

Then save/confirm the changes.

---

# 🔄 Important: Restart Your Terminal

If Command Prompt or PowerShell was already open while you changed PATH, it may still be using the old environment.

Close the existing terminal.

Open a **new** terminal window.

Then test Flutter.

---

# 🧪 Step 05 — Test Flutter

Open Command Prompt or PowerShell and run:

```bash
flutter
```

If Flutter is correctly available through PATH, you should see Flutter's command-line output/help.

You can also check the installed version with:

```bash
flutter --version
```

---

# 🩺 Step 06 — Meet `flutter doctor`

Now we meet one of the most important commands in Flutter:

```bash
flutter doctor
```

Think of it as:

> 🩺 **A health check for your Flutter development environment.**

It checks the major components Flutter needs and reports what is installed, missing, or incorrectly configured.

Conceptually:

```text
                 flutter doctor
                       │
       ┌───────────────┼───────────────┐
       ▼               ▼               ▼
    Flutter         Android          Devices
      SDK             Tools
       │               │
       └───────────────┼───────────────┘
                       ▼
                  Setup Status
```

---

# 🚦 Understanding Flutter Doctor Output

Flutter Doctor commonly reports status using symbols such as:

```text
✓   Everything is okay

!   Something needs attention

✗   Something is missing or not configured
```

Don't panic if you don't immediately get all green checks.

That's literally one of the reasons `flutter doctor` exists:

> **It tells you what needs fixing.**

---

# 🤖 Step 07 — Install Android Studio

Flutter is the framework we're using, but Android development also requires Android tooling.

Install **Android Studio**.

During installation, the **Standard** installation option is generally the easiest starting point for beginners.

The exact interface can change between Android Studio versions, so don't worry if your screen doesn't look exactly like the lecture screenshots.

---

# 🧩 Flutter vs Android Studio

Don't confuse these two.

### Flutter

```text
Flutter
↓
Cross-platform UI framework/toolkit
```

### Android Studio

```text
Android Studio
↓
Android development IDE
```

They work together, but they are **not the same thing**.

---

# 🤖 Step 08 — Configure Android SDK

Inside Android Studio, locate the **Android SDK** settings.

The exact menu can vary depending on your Android Studio version.

The important concept is:

```text
Android Studio
      ↓
Android SDK
      ↓
Android development tools
```

Make sure the required Android SDK components are installed.

---

# 🧰 Step 09 — Install Command-Line Tools

Inside the Android SDK settings, find:

```text
Android SDK Command-line Tools
```

Enable/install the required version.

Then apply the changes.

### Why do we need command-line tools?

Because Android development isn't performed exclusively through graphical interfaces.

Various development tasks rely on command-line tooling.

Flutter's Android development workflow therefore needs the Android tooling to be correctly configured.

---

# 🔄 Step 10 — Run Flutter Doctor Again

After Android Studio and the Android SDK tools are installed, return to your terminal.

Run:

```bash
flutter doctor
```

again.

This second check is important.

Before Android Studio:

```text
Flutter
   │
   └── Android tools may be missing ❌
```

After configuration:

```text
Flutter
   │
   ├── Flutter SDK       ✅
   ├── Android SDK      ✅
   ├── Android tools    ✅
   └── Device           ?
```

The exact results depend on your setup.

---

# 📱 Emulator vs Physical Device

Eventually, Flutter needs somewhere to run your application.

You can use:

### Android Emulator

A virtual Android device running on your computer.

```text
Computer
   │
   └── Android Emulator
             │
             ▼
        Flutter App
```

### Physical Android Device

A real Android phone connected to your computer.

```text
Computer
   │
   └── USB / wireless connection
             │
             ▼
        Android Phone
             │
             ▼
        Flutter App
```

For development, a physical phone can sometimes be lighter on computer resources than running an emulator.

---

# 🧠 The Complete Setup Flow

```text
              DOWNLOAD FLUTTER
                     │
                     ▼
             EXTRACT FLUTTER SDK
                     │
                     ▼
                FIND /bin
                     │
                     ▼
              ADD /bin → PATH
                     │
                     ▼
                `flutter`
                     │
                     ▼
             `flutter doctor`
                     │
                     ▼
            INSTALL ANDROID STUDIO
                     │
                     ▼
              CONFIGURE SDK
                     │
                     ▼
       INSTALL COMMAND-LINE TOOLS
                     │
                     ▼
             `flutter doctor`
                     │
                     ▼
            CONNECT A DEVICE
                     │
                     ▼
                  📱
                READY!
```

---

# 🧠 The Setup Mental Model

If all the terminology starts blending together, remember this:

```text
Dart
 ↓
Programming language

Flutter
 ↓
Framework / UI toolkit

Flutter SDK
 ↓
Tools required for Flutter development

Android Studio
 ↓
Android development IDE

Android SDK
 ↓
Android development tools + APIs

PATH
 ↓
Tells Windows where commands are located

flutter doctor
 ↓
Checks the development environment
```

---

# 🧪 Lecture 01 Checklist

Before moving on:

### Flutter

* [ ] Flutter SDK downloaded
* [ ] Flutter SDK extracted
* [ ] Flutter `bin` directory located
* [ ] Flutter added to PATH
* [ ] `flutter` command works
* [ ] `flutter --version` works

### Android

* [ ] Android Studio installed
* [ ] Android SDK configured
* [ ] Android SDK Command-line Tools installed
* [ ] Android development tools detected

### Verification

* [ ] `flutter doctor` executed
* [ ] Errors understood
* [ ] Warnings investigated
* [ ] Emulator or physical device available

---

# 🧪 Commands From This Lecture

## Check Flutter

```bash
flutter
```

## Check Flutter version

```bash
flutter --version
```

## Check development environment

```bash
flutter doctor
```

---

# 🐛 If Something Goes Wrong

Don't immediately reinstall everything.

First:

```bash
flutter doctor
```

Then read the output.

A good debugging workflow is:

```text
Something doesn't work
        ↓
Read the error
        ↓
Run flutter doctor
        ↓
Identify the failing component
        ↓
Fix ONE thing
        ↓
Run flutter doctor again
        ↓
Test again
```

### Example

If Flutter isn't recognized:

```text
'flutter' is not recognized...
```

Think:

```text
Is Flutter installed?
        ↓
Is the PATH correct?
        ↓
Did I add the /bin folder?
        ↓
Did I open a new terminal?
```

Don't randomly reinstall Flutter.

---

# 🎯 What You Should Understand After Lecture 01

You should be able to explain:

### 1. What is Flutter?

A framework/toolkit for building applications using Dart.

### 2. What is Dart?

The programming language used to write Flutter applications.

### 3. What is an SDK?

A collection of tools and resources used for software development.

### 4. Why is Flutter's `bin` added to PATH?

So Windows can find and execute Flutter commands from the terminal.

### 5. What does `flutter doctor` do?

It checks the Flutter development environment and reports configuration problems.

### 6. Why do we need Android Studio?

To provide/manage Android development tooling, including the Android SDK.

### 7. What is the Android SDK?

A collection of Android development tools and APIs.

### 8. Why do we install Android SDK Command-line Tools?

They provide command-line Android development tooling used by the Android development workflow.

---

# 🏁 Lecture 01 Milestone

## 🥉 Environment Ready

You've completed this setup milestone when you can:

```text
☑️ Run Flutter from the terminal
☑️ Explain what the Flutter SDK is
☑️ Explain what PATH does
☑️ Run flutter doctor
☑️ Understand the Android SDK's role
☑️ Use Android Studio
☑️ Identify setup errors
☑️ Run Flutter on an Android target
```

The goal isn't simply:

> **"I installed Flutter."**

The goal is:

> **"I understand what I installed and how the pieces connect."**

---

# 🚀 What's Next?

The machine is ready.

Now we can actually start building.

```text
SETUP
  ↓
🐦 FLUTTER BASICS
  ↓
🎨 UI
  ↓
🧠 STATE
  ↓
🧭 NAVIGATION
  ↓
🔥 FIREBASE
  ↓
🌐 APIs
  ↓
📱 DEVICE FEATURES
  ↓
🔒 SECURITY
  ↓
⚡ PERFORMANCE
  ↓
🚀 PRODUCTION APP
```

> **First we make the environment work.**
>
> **Then we make the app work.**
>
> **Then we learn why it works.**
