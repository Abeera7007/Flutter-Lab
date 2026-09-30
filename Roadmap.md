# 🐦 Flutter Lab — Roadmap

### From `flutter doctor` to production-ready apps.

Welcome to **Flutter Lab** — a beginner-first journey through Flutter, Dart, Firebase, Android development, APIs, device features, and the behind-the-scenes pieces that turn code into real applications.

This repository is being built **lecture by lecture**, with the goal of understanding not only *what* to write, but **why it works, how the pieces connect, and when to use them in a real project**.

---

# 🎯 The Goal

We're starting at:

```text
"What even is an SDK?"
```

and working toward:

```text
"I can build, connect, secure,
optimize, and ship a real Flutter app."
```

The focus isn't just on making screens.

It's on understanding the **entire application ecosystem**.

```text
Flutter
   │
   ├── UI
   ├── State
   ├── Navigation
   ├── APIs
   ├── Firebase
   ├── Storage
   ├── Authentication
   ├── Device features
   ├── Background services
   └── Production concerns
```

---

# 🗺️ Course Roadmap

## 🐦 01 — Flutter Foundations

* What is Flutter?
* What is Dart?
* What is an SDK?
* Flutter SDK
* Android SDK
* Android Studio
* Environment variables
* PATH
* Flutter CLI
* `flutter doctor`
* Flutter project structure
* Running the first application

📁 **Current:** [`setup-flutter.md`](setup-flutter.md)

---

## 🎨 02 — Flutter UI

Learn how Flutter actually builds interfaces.

* Widgets
* Stateless widgets
* Stateful widgets
* Widget tree
* Build method
* Layouts
* Rows
* Columns
* Containers
* Padding
* Alignment
* Text
* Images
* Buttons
* Forms
* Lists
* Grids
* Scrolling

---

## 🧠 03 — State & App Architecture

Move from static screens to applications that actually **change**.

* State
* Stateful widgets
* State management
* Provider package
* Application architecture
* Separating UI and logic
* Managing shared state

---

## 🧭 04 — Navigation & Routes

Learn how applications move between screens.

* Routes
* Navigation
* Named routes
* Route arguments
* Transitions
* Navigation stacks
* Back navigation
* Splash screens
* Onboarding screens

---

## ✨ 05 — Animations & Interaction

Make interfaces feel alive.

* Flutter animations
* Native animations
* Page transitions
* Gestures
* Sliders
* Shimmers
* Interactive UI
* Motion effects

---

# 🔥 Firebase

A major part of the course focuses on connecting Flutter applications to Firebase.

## 🔐 Authentication

* Firebase Authentication
* User registration
* Login
* Logout
* Authentication state
* Phone number authentication
* Phone number validation

---

## 🗄️ Cloud Firestore

Learn how applications store and synchronize data.

* Collections
* Documents
* Queries
* CRUD operations
* Real-time updates
* Timestamps
* Timestamp manipulation
* Optimal database calls
* Data persistence
* Caching

---

## ☁️ Firebase Storage

Work with files and media.

* Uploading files
* Downloading files
* Image storage
* File paths
* Image handling
* Image compression
* BlurHash images

---

## ⚡ Firebase Cloud Functions

Move logic to the backend.

* Cloud Functions
* Server-side operations
* Triggered functions
* Automated tasks
* Backend workflows

---

## 🛡️ Firebase Security

Because:

> **A working app with an insecure database is still a broken app.**

Topics include:

* Firebase Security Rules
* Authentication-based access
* Database protection
* Storage protection
* Secure application architecture

---

## 🔔 Firebase Messaging

Learn how applications communicate with users.

* Push notifications
* Firebase Cloud Messaging
* Notification handling
* Background notifications
* Notification-driven workflows

---

## 📊 Firebase Analytics

Understand what happens after users install the app.

* Analytics
* Events
* User interaction
* App usage
* Retention concepts

---

# 🌐 APIs & External Services

Learn how Flutter communicates with the outside world.

* API calls
* HTTP requests
* JSON
* Parsing responses
* Error handling
* Loading states
* API-driven UI

Additional integrations include:

* 🗺️ Google Maps
* 📢 Google Ads
* 💬 In-app messaging
* 📧 Programmed emails
* 💳 In-app purchases

---

# 📱 Device & Native Features

Flutter applications can interact with the device itself.

Topics include:

* Device sensors
* Device permissions
* Phone numbers
* Calls
* SMS
* File paths
* Background services
* Wake locks
* Power management
* Volume control
* Native code

The goal is to understand how Flutter communicates with platform-specific functionality.

```text
Flutter
   │
   ▼
Platform Layer
   │
   ├── Android
   └── iOS
```

---

# 🎨 UI / UX & Production Features

Learn the details that make an application feel polished.

### Visuals

* Theming
* Responsive design
* Color pickers
* Date pickers
* Image handling
* BlurHash
* Thumbnails

### Interaction

* Gestures
* Sliders
* Bottom modals
* Shimmers
* Animations
* Transitions

### Media

* Video player integration
* Image compression
* Photo viewing

### Application Experience

* Splash screens
* Onboarding
* App retention
* Launcher options

---

# 💾 Data & Performance

A production app shouldn't constantly waste resources.

Topics include:

* Cache
* Data persistence
* Efficient database calls
* Real-time data
* Timestamp manipulation
* Image optimization
* Image compression
* Local data handling

---

# 🔒 Production & Security

Moving from:

```text
"It works on my laptop."
```

to:

```text
"Let's actually ship this."
```

Topics include:

* Code obfuscation
* Security rules
* Permissions
* Secure data access
* Performance
* Database optimization
* Production configuration

---

# 🧪 Learning Structure

Each lecture will follow roughly this pattern:

```text
📚 Lecture
     ↓
🧠 Concept
     ↓
💡 Why does it exist?
     ↓
🔍 How does it work?
     ↓
💻 Code
     ↓
🧪 Experiment
     ↓
🛠️ Mini Project
     ↓
🚀 Real-world application
```

The objective is to avoid:

```text
copy → paste → pray
```

Instead:

```text
understand → build → break → debug → rebuild
```

---

# 📂 Repository Structure

The repository will gradually grow into something like:

```text
flutter-lab/
│
├── README.md
├── roadmap.md
├── setup-flutter.md
│
├── lectures/
│   ├── 01-setup/
│   ├── 02-ui/
│   ├── 03-state/
│   ├── 04-navigation/
│   └── ...
│
├── projects/
│   ├── project-01/
│   ├── project-02/
│   └── ...
│
└── notes/
    └── ...
```

The exact structure may evolve as the course gets bigger.

---

# 📈 Progress

| #  | Topic               | Status         |
| -- | ------------------- | -------------- |
| 01 | Flutter Setup       | 🟢 In Progress |
| 02 | Flutter UI          | ⚪ Upcoming     |
| 03 | State Management    | ⚪ Upcoming     |
| 04 | Navigation & Routes | ⚪ Upcoming     |
| 05 | Animations          | ⚪ Upcoming     |
| 06 | Firebase            | ⚪ Upcoming     |
| 07 | Firestore           | ⚪ Upcoming     |
| 08 | Authentication      | ⚪ Upcoming     |
| 09 | Storage             | ⚪ Upcoming     |
| 10 | APIs                | ⚪ Upcoming     |
| 11 | Device Features     | ⚪ Upcoming     |
| 12 | Production Features | ⚪ Upcoming     |
| 13 | Final Projects      | ⚪ Upcoming     |

---

# 🧭 End Goal

By the end of this lab, the goal is to move through this progression:

```text
🐣 Beginner
   │
   ▼
🐦 Flutter Basics
   │
   ▼
🎨 UI Developer
   │
   ▼
🧠 App Developer
   │
   ▼
🔥 Full-stack Flutter + Firebase
   │
   ▼
📱 Production-minded Developer
```

---

> **Don't just learn how to make an app run.**
>
> **Learn what makes the app work.**
