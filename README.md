<div align="center">

<img src="./banner.svg" alt="Flutter Lab — learn, experiment, build" width="100%">

<br>

### *Learning Flutter by turning ideas into apps — one experiment, one bug, and one questionable UI decision at a time.*

<br>

![Flutter](https://img.shields.io/badge/Flutter-40E0D0?style=for-the-badge&logo=flutter&logoColor=0B1A1E)
![Dart](https://img.shields.io/badge/Dart-E8B93A?style=for-the-badge&logo=dart&logoColor=0B1A1E)
![Course](https://img.shields.io/badge/Course-eHunar_Flutter-40E0D0?style=for-the-badge&labelColor=0B1A1E)
![Status](https://img.shields.io/badge/Status-Learning_in_Public-E8B93A?style=for-the-badge&labelColor=0B1A1E)
![Last Commit](https://img.shields.io/github/last-commit/Abeera7007/flutter-lab?style=for-the-badge&color=40E0D0&labelColor=0B1A1E)

<br>

**[About](#about) · [The Journey](#journey) · [Roadmap](#roadmap) · [Projects](#projects) · [The Lab](#the-lab) · [Real Builds](#real-builds) · [Tech](#tech) · [Progress](#progress) · [What I'm Learning](#learning)**

</div>

---

## Hey!!

This is my Flutter workshop. Part notebook, part playground, part "why is this widget 400 pixels too wide."

I'm learning Flutter the slow, honest way: following a course, breaking things on purpose, and slowly building the confidence (and the skills) to make real apps out of my own ideas. I'm a CS undergrad, I'm early in this, and I'm documenting all of it here, including the parts that don't work yet.

<a id="about"></a>

## 📖 About This Repo

Flutter Lab is my learning-in-public repo for Flutter and Dart.

The backbone is the **eHunar Flutter course**. I'm working through Dart, Flutter fundamentals, and the guided projects (**Tyamo** and **Fizzux** so far). That's the foundation, and I'm taking it seriously.

But the course is the starting line, not the finish line. The actual goal is learning how to **turn an idea into an app**, which is a different skill from following along with a tutorial. So this repo runs on three tracks:

| Track | What it is | Where it lives |
|:--:|:--|:--|
| 📚 **LEARN** | Following the eHunar Flutter course. Notes, code, and guided projects. | [`/learn`](./learn) |
| 🧪 **EXPERIMENT** | Small, weird, fun stuff. Mini games, UI experiments, animations, "can I build this?" attempts. | [`/lab`](./lab) |
| 🚀 **BUILD** | My own app ideas, taken from concept to UI/UX to Flutter prototype to MVP, and maybe someday a real product. | [`/builds`](./builds) |

If you're also learning Flutter, feel free to poke around. Just know that some of the code here is *educational*, not *exemplary*.

---

<a id="journey"></a>

<div align="center">

##  THE JOURNEY

*Nobody ships on the first try. This is the loop.*

</div>

```text
   ┌──────────────┐
   │    LEARN     │   understand the thing
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │  EXPERIMENT  │   try it in a small, safe, silly way
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │    BUILD     │   make something that actually runs
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │    BREAK     │   it crashes. obviously.
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │     FIX      │   read the error. actually read it.
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │   IMPROVE    │   cleaner code, better UI, fewer regrets
   └──────┬───────┘
          ▼
   ┌──────────────┐
   │     SHIP     │   put it in front of real people
   └──────────────┘
```

> **BREAK → FIX → IMPROVE** is the part where most of the learning happens. I'm not skipping it.

---

<a id="roadmap"></a>

## 🗺️ Roadmap

A rough map of the course so far. Topic lists are based on what I expect the modules to cover. I'll adjust them as I go through each one, and I'll add the exact lecture/module titles once I've actually worked through them.

Tap a phase to expand it.

<details>
<summary><b>Phase 01 — Getting Started with Flutter</b></summary>

<br>

This is where the journey actually starts. Before building questionable apps at 2AM, I need to figure out why Flutter is yelling at me.

- [ ] What is Flutter?
- [ ] Installing Flutter
- [ ] Android Studio
- [ ] Flutter SDK
- [ ] Android SDK
- [ ] Emulator setup
- [ ] VS Code setup
- [ ] `flutter doctor` (and making it stop complaining)
- [ ] Creating the first Flutter project
- [ ] Understanding the project structure
- [ ] Running the first app

</details>

<details>
<summary><b>Phase 02 — Introduction to Flutter</b></summary>

<br>

The "everything is a widget" chapter. Learn the vocabulary before writing the sentences.

- [ ] Flutter overview
- [ ] Flutter architecture
- [ ] Widgets
- [ ] The widget tree
- [ ] `MaterialApp`
- [ ] `Scaffold`
- [ ] `BuildContext`
- [ ] `StatelessWidget`
- [ ] `StatefulWidget`
- [ ] Hot Reload
- [ ] Hot Restart

</details>

<details>
<summary><b>Phase 03 — Dart</b> <i>(6 parts)</i></summary>

<br>

Flutter is written in Dart, so Dart comes first. Split into six parts so it doesn't turn into one giant blob.

**Dart Part 01 — The Basics**
- [ ] Variables
- [ ] Data types
- [ ] Strings
- [ ] Numbers
- [ ] Booleans
- [ ] Operators

**Dart Part 02 — Making Decisions**
- [ ] Conditions
- [ ] `if` / `else`
- [ ] `switch`
- [ ] Loops

**Dart Part 03 — Functions**
- [ ] Functions
- [ ] Parameters
- [ ] Return values
- [ ] Arrow functions

**Dart Part 04 — Collections**
- [ ] Lists
- [ ] Sets
- [ ] Maps
- [ ] Working with collections

**Dart Part 05 — OOP**
- [ ] Classes
- [ ] Objects
- [ ] Constructors
- [ ] OOP concepts

**Dart Part 06 — The Grown-Up Stuff**
- [ ] Null safety
- [ ] Exceptions
- [ ] Async programming
- [ ] Futures
- [ ] `async` / `await`

</details>

<details>
<summary><b>Phase 04 — Flutter 3.0</b> <i>(7 parts)</i></summary>

<br>

Now the fun part: actually building screens. I've grouped the topics below in a way that makes sense to me. The real course order may differ, and I'll update this as I go.

**Flutter 3.0 Part 01 — Layouts**
- [ ] Container
- [ ] Row
- [ ] Column
- [ ] Stack
- [ ] Expanded

**Flutter 3.0 Part 02 — Everyday Widgets**
- [ ] Text
- [ ] Images
- [ ] Icons
- [ ] Buttons

**Flutter 3.0 Part 03 — User Input**
- [ ] TextFields
- [ ] Forms

**Flutter 3.0 Part 04 — Lists & Grids**
- [ ] Lists
- [ ] Grids

**Flutter 3.0 Part 05 — Navigation & Feedback**
- [ ] Navigation
- [ ] Dialogs
- [ ] Snackbars
- [ ] Bottom sheets

**Flutter 3.0 Part 06 — Look & Feel**
- [ ] Themes
- [ ] Styling

**Flutter 3.0 Part 07 — State Management**
- [ ] State management

</details>

---

<a id="projects"></a>

<div align="center">

##  PROJECTS

*Guided builds from the course. These are where the concepts stop being theory.*

</div>

<br>

<table>
  <tr>
    <td width="50%" valign="top">

### 🅣 Tyamo
**Type:** Guided course project

One of the guided Flutter projects from my learning journey.

**Status:** ⬜ Not started

`Coming soon...`

<sub>📁 [`learn/projects/tyamo`](./learn/projects/tyamo)</sub>

</td>
<td width="50%" valign="top">

### 🅕 Fizzux
**Type:** Guided course project

Another guided project from the learning journey.

**Status:** ⬜ Not started

`Coming soon...`

<sub>📁 [`learn/projects/fizzux`](./learn/projects/fizzux)</sub>

</td>
  </tr>
  <tr>
    <td colspan="2" align="center">

### ➕ More course projects
`Coming soon...`

</td>
  </tr>
</table>

Every project gets its own folder and its own README with the same sections:

| Section | What goes in it |
|:--|:--|
| 📝 **Description** | What it is, in plain words |
| 🧠 **Concepts learned** | The Flutter/Dart ideas it taught me |
| ✨ **Features** | What the app actually does |
| 📸 **Screenshots** | Real screenshots or GIFs from my emulator/device |
| 🐛 **Challenges** | What broke, and what I did about it |
| 💡 **What I learned** | The honest takeaway |
| 🔮 **Future improvements** | What I'd change or add next |

---

<a id="the-lab"></a>

<div align="center">

## 🧪 THE LAB

*Where I experiment outside the course.*

> **"It doesn't have to be useful.**
> **It has to teach me something."**

</div>

<br>

The course teaches me how Flutter works. The Lab is where I find out whether I actually understood it. If I learn about animations, I'll make something silly move around. If I get curious about a game mechanic, I'll try to build it badly and then less badly.

Some of these will be polished. Some will be half-finished. All of them are here on purpose.

| | Category | What lives here | Status |
|:--:|:--|:--|:--:|
| 🧪 | **Mini Experiments** | Tiny tests for one specific idea or widget | `Coming soon...` |
| 🎮 | **Mini Games** | Small games built to learn state, logic, and timing | `Coming soon...` |
| 🎨 | **UI Experiments** | Layouts, styles, and "what if the button did this instead" | `Coming soon...` |
| ✨ | **Animation Experiments** | Motion, transitions, and things that move for no good reason | `Coming soon...` |
| 📱 | **App Recreations** | Rebuilding UIs from apps I like, to see how they're put together | `Coming soon...` |
| 💡 | **Random Ideas** | 1AM thoughts that turned into a `flutter create` | `Coming soon...` |
| 🤨 | **"Can I actually build this?"** | Ambitious attempts. Failure is a valid outcome. | `Coming soon...` |

**Lab rules:**

1. Every experiment is allowed to be messy.
2. Every experiment must teach me at least one thing.
3. Failed experiments stay in the repo, with notes on what went wrong.

---

<a id="real-builds"></a>

<div align="center">

## 🚀 REAL BUILDS

*Original app ideas that go beyond learning exercises.*

</div>

<br>

This is the long game. These are my own ideas, not tutorial projects, and I want to treat them like real products: figure out the problem first, then design, then build, then test with actual people.

To be clear about where things stand: **none of these are market-ready yet.** Some may stay prototypes. Some may get dropped once I learn something that changes the plan. A few might grow into real products. This section is where I find out which.

```text
 IDEA ─► PROBLEM ─► RESEARCH ─► USER FLOW ─► UI/UX
                                                │
                                                ▼
 SHIP ◄─ ITERATE ◄─ TEST ◄─ FLUTTER MVP ◄─ PROTOTYPE
```

Each build will be documented at every stage, including the version where the idea turned out to be worse than I thought.

| # | Build | Stage | Status |
|:--:|:--|:--|:--:|
| 01 | *Idea in progress* | Idea | `Coming soon...` |
| 02 | *Idea in progress* | Idea | `Coming soon...` |
| 03 | *Idea in progress* | Idea | `Coming soon...` |

---

<a id="tech"></a>

## ⚙️ Skills & Technology

I'm keeping this list honest: **Current** is what I'm actively working with. **Exploring** is what I'm curious about and plan to learn. It doesn't mean I know it yet.

### Current

![Dart](https://img.shields.io/badge/Dart-E8B93A?style=for-the-badge&logo=dart&logoColor=0B1A1E)
![Flutter](https://img.shields.io/badge/Flutter-40E0D0?style=for-the-badge&logo=flutter&logoColor=0B1A1E)

### Exploring

| | Topic |
|:--:|:--|
| 🔥 | Firebase |
| 🌐 | APIs |
| 🔐 | Authentication |
| 🗄️ | Databases |
| 💾 | Local storage |
| 🧭 | State management |
| 📐 | Responsive UI |
| 🧪 | Testing |
| 📦 | Deployment |

---

<a id="progress"></a>

## ✅ Progress Tracker

Update the status column as I go: `⬜` not started · `🟨` in progress · `✅` done

| # | Module | Status |
|:--:|:--|:--:|
| 01 | Getting Started with Flutter | ⬜ |
| 02 | Introduction to Flutter | ⬜ |
| 03 | Dart Part 01 | ⬜ |
| 04 | Dart Part 02 | ⬜ |
| 05 | Dart Part 03 | ⬜ |
| 06 | Dart Part 04 | ⬜ |
| 07 | Dart Part 05 | ⬜ |
| 08 | Dart Part 06 | ⬜ |
| 09 | Flutter 3.0 | ⬜ |
| 10 | Tyamo | ⬜ |
| 11 | Fizzux | ⬜ |
| 12 | Experiments | ⬜ |
| 13 | First Original App | ⬜ |
| 14 | First App Launch | ⬜ |

---

<a id="learning"></a>

## 🧠 What I'm Actually Learning

Finishing a course is not the goal. Being able to build things is.

- **Learning by building.** Watching a tutorial feels productive. Building something from an empty file is where it sticks.
- **Understanding over memorizing.** I'd rather know *why* a widget works than copy it and hope.
- **Debugging.** Reading errors, tracing problems, and not panicking at red screens.
- **UI/UX thinking.** An app that runs isn't automatically an app that feels good to use.
- **Problem solving.** Breaking a big idea into small pieces I can actually build.
- **Turning ideas into working software.** The whole point of this repo.
- **Learning from failed experiments.** They stay in the repo. They taught me the most.

---

<div align="center">

## 🏁

**Started with Flutter.**
**Stayed for the bugs.**
**Building until the ideas work.**

<br>

<sub>Built in public by <a href="https://github.com/Abeera7007">Abeera Zainab</a> · CS undergrad · currently in the BREAK → FIX loop</sub>

<br>

⭐ *If this helps you on your own Flutter journey, a star is always appreciated.*

</div>
