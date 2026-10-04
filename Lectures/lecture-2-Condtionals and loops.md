# 🔀 Lesson 02 — Conditionals & Loops

### *Teaching CampusMate to think, decide, and repeat.*

> **Story Mode 🎬**
>
> Ari has created the first version of CampusMate.
>
> It knows who the student is.
>
> It knows Ari's semester and CGPA.
>
> But there's a problem...
>
> **CampusMate is dumb.** 💀
>
> It can store information, but it can't *do anything intelligent with it*.
>
> Ari wants the app to answer questions like:
>
> * Is my attendance below 75%?
> * Should I get a warning?
> * Did I pass this course?
> * Which courses need my attention?
> * How many courses do I have?
>
> To solve these problems, we're going to teach CampusMate two things:
>
> **🔀 How to make decisions**
>
> **🔁 How to repeat tasks**

---

# 🗺️ What We're Building Today

By the end of this lesson, CampusMate will be able to:

```text
Student Data
     ↓
   🔀 Decide
     ↓
   🔁 Repeat
     ↓
Smart CampusMate
```

We'll learn:

```text
if
if / else
else if
nested conditions
logical operators
for loops
while loops
do...while
break
continue
nested loops
```

And we'll use every concept inside our **CampusMate story**.

---

# 🎬 PART 1 — Ari Has a Problem

Last lecture, we created basic student information.

Something like:

```dart
String name = "Ari";
int age = 21;
double cgpa = 3.2;
bool isEnrolled = true;
```

CampusMate can answer:

> "What's Ari's CGPA?"

```dart
print(cgpa);
```

It can calculate things.

But imagine Ari opens the app and sees:

```text
CGPA: 3.2
Attendance: 68%
```

The app simply displays:

> 68%

😐

Ari wants the app to understand what that means.

A human immediately thinks:

> "68%? That's below the university requirement. I should probably get a warning."

But Dart doesn't automatically know that.

We need to **teach it the rule**.

---

# 🧠 PART 2 — Conditions

A **condition** is basically a question whose answer is:

```text
true
```

or:

```text
false
```

For example:

```dart
68 < 75
```

Dart evaluates it:

```text
68 < 75
 ↓
true
```

So we can think of conditions as:

> **Questions with a yes/no answer.**

---

# 🔍 CampusMate's First Question

Ari's university requires at least 75% attendance.

Let's tell Dart:

```dart
double attendance = 68;

print(attendance < 75);
```

Output:

```text
true
```

CampusMate now knows:

> "Ari's attendance is below the requirement."

But knowing isn't enough.

We want the app to **do something**.

That's where `if` comes in.

---

# 🔀 PART 3 — `if`

Basic Dart structure:

```dart
if (condition) {
  // code
}
```

Let's teach CampusMate:

```dart
double attendance = 68;

if (attendance < 75) {
  print("⚠️ Attendance is below 75%!");
}
```

Output:

```text
⚠️ Attendance is below 75%!
```

We've just given CampusMate its first piece of decision-making logic.

---

# 🧠 How `if` Thinks

Imagine CampusMate standing at a decision point:

```text
             Attendance < 75?
                    │
             ┌──────┴──────┐
             │             │
            YES            NO
             │             │
             ▼             ▼
       Show warning     Do nothing
```

The code inside `{ }` only runs when the condition is `true`.

---

# 🧪 Experiment

Change:

```dart
double attendance = 68;
```

to:

```dart
double attendance = 82;
```

Now:

```text
82 < 75
 ↓
false
```

So nothing happens.

That's exactly what we told Dart to do.

---

# 🎬 STORY UPDATE

Ari tests CampusMate.

```text
Attendance: 68%
```

CampusMate:

> ⚠️ "Attendance is below 75%!"

Ari fixes the attendance.

```text
Attendance: 82%
```

CampusMate:

> ...

Nothing.

Ari says:

> "Okay... but can you tell me that I'm SAFE too?"

Fair.

We need another path.

---

# ↔️ PART 4 — `if / else`

We can tell Dart what to do when the condition is **false**.

```dart
if (condition) {
  // true
} else {
  // false
}
```

CampusMate:

```dart
double attendance = 82;

if (attendance < 75) {
  print("⚠️ Attendance is below 75%!");
} else {
  print("✅ Attendance is safe!");
}
```

Output:

```text
✅ Attendance is safe!
```

---

# 🧠 The Two-Path System

```text
                 ATTENDANCE
                     │
                     ▼
              Is it < 75%?
                /       \
              YES       NO
               │         │
               ▼         ▼
            WARNING     SAFE
```

This is the basic idea behind an enormous amount of software.

---

# 📱 Where You'll See This in Flutter

Later, our Flutter UI might do something like:

```dart
if (attendance < 75) {
  // show warning card
} else {
  // show safe card
}
```

Instead of printing text, Flutter could display an actual widget.

```text
┌──────────────────────────────┐
│ ⚠️ Attendance Warning        │
│                              │
│ Your attendance is 68%.      │
│ You need to attend more      │
│ classes.                     │
└──────────────────────────────┘
```

Same logic.

Different output.

---

# 🎬 STORY UPDATE — Ari Adds Courses

Ari doesn't have just one course.

CampusMate now has:

```text
Programming       82%
Database           74%
Android            91%
Management         68%
Architecture       79%
```

Ari asks:

> "Can the app tell me what kind of situation each course is in?"

There are more than two possibilities now.

---

# 🔀 PART 5 — `else if`

Suppose CampusMate uses:

```text
90%+     Excellent
80–89%   Good
75–79%   Safe
Below 75 Warning
```

We can use:

```dart
double attendance = 86;

if (attendance >= 90) {
  print("🌟 Excellent");
} else if (attendance >= 80) {
  print("✅ Good");
} else if (attendance >= 75) {
  print("🙂 Safe");
} else {
  print("⚠️ Warning");
}
```

Output:

```text
✅ Good
```

---

# 🧠 How `else if` Works

Dart checks from **top → bottom**.

```text
attendance >= 90?
       │
      NO
       ↓
attendance >= 80?
       │
      YES
       ↓
    "Good"
       ↓
      STOP
```

Once Dart finds a condition that is `true`, it runs that block and skips the rest.

---

# ⚠️ ORDER MATTERS

Look at this:

```dart
if (attendance >= 75) {
  print("Safe");
} else if (attendance >= 90) {
  print("Excellent");
}
```

For:

```text
95%
```

Dart checks:

```text
95 >= 75
 ↓
true
```

So it prints:

```text
Safe
```

It never reaches the `90` condition.

### Rule:

> **When conditions overlap, put the more specific/higher-priority condition first.**

Correct:

```dart
if (attendance >= 90) {
  print("🌟 Excellent");
} else if (attendance >= 75) {
  print("🙂 Safe");
}
```

---

# 🎯 CAMPUSMATE CHALLENGE #1

Ari wants CampusMate to classify a student's CGPA:

```text
3.5+       → Excellent
3.0–3.49   → Good
2.5–2.99   → Average
Below 2.5  → Needs Improvement
```

Create the logic.

Try it yourself before looking at the solution.

<details>
<summary>👀 Reveal Solution</summary>

```dart
double cgpa = 3.2;

if (cgpa >= 3.5) {
  print("🌟 Excellent");
} else if (cgpa >= 3.0) {
  print("✅ Good");
} else if (cgpa >= 2.5) {
  print("🙂 Average");
} else {
  print("⚠️ Needs Improvement");
}
```

</details>

---

# 🔐 PART 6 — Multiple Conditions

Ari now wants CampusMate to decide whether someone can register for an exam.

There are two requirements:

```text
Attendance >= 75%
AND
Fees paid
```

So:

```dart
double attendance = 82;
bool feesPaid = true;

if (attendance >= 75 && feesPaid) {
  print("✅ Exam registration allowed.");
} else {
  print("❌ Exam registration blocked.");
}
```

---

# 🧠 Remember Our Logic Operators

From Lecture 1:

```text
&&   AND
||   OR
!    NOT
```

### `&&`

Both conditions must be true.

```text
A && B

true  + true  → true
true  + false → false
false + true  → false
false + false → false
```

---

### `||`

At least one condition must be true.

```text
A || B

true  + true  → true
true  + false → true
false + true  → true
false + false → false
```

---

### `!`

Flips the boolean.

```dart
bool isAbsent = false;

print(!isAbsent);
```

Output:

```text
true
```

---

# 🎬 STORY UPDATE

Ari says:

> "Great. But I have FIVE courses."

CampusMate currently checks one course at a time.

That's annoying.

```dart
print("Checking Programming...");
print("Checking Database...");
print("Checking Android...");
print("Checking Management...");
print("Checking Architecture...");
```

And Ari has a thought:

> "Why don't we make the computer do this?"

Enter:

# 🔁 LOOPS

---

# 🔁 PART 7 — Why Loops Exist

Suppose Ari has:

```text
5 courses
```

We *could* manually write:

```dart
print("Programming");
print("Database");
print("Android");
print("Management");
print("Architecture");
```

But what if Ari has:

```text
50 courses?
500 courses?
5000 students?
```

We don't want:

```text
copy
paste
copy
paste
copy
paste
😭
```

We want:

> **Repeat this instruction automatically.**

---

# 🔁 PART 8 — The `for` Loop

Basic structure:

```dart
for (initialization; condition; update) {
  // repeated code
}
```

Example:

```dart
for (int i = 0; i < 5; i++) {
  print(i);
}
```

Output:

```text
0
1
2
3
4
```

---

# 🧠 Breaking It Apart

This:

```dart
for (int i = 0; i < 5; i++)
```

has three parts.

### 1️⃣ Initialization

```dart
int i = 0
```

Where do we start?

> 0

### 2️⃣ Condition

```dart
i < 5
```

Should we continue?

> Yes, while `i` is less than 5.

### 3️⃣ Update

```dart
i++
```

What happens after every round?

> Increase `i` by 1.

---

# 🔄 The Loop in Slow Motion

```text
i = 0
 ↓
0 < 5 → YES
 ↓
print(0)
 ↓
i++
 ↓
i = 1
 ↓
1 < 5 → YES
 ↓
print(1)
 ↓
i++
 ↓
...
 ↓
i = 5
 ↓
5 < 5 → FALSE
 ↓
STOP
```

---

# 🎬 CAMPUSMATE USES A LOOP

Let's say we have course names:

```dart
String course1 = "Programming";
String course2 = "Database";
String course3 = "Android";
```

We'll learn better ways to store these later.

For now, imagine CampusMate needs to process several items.

The key idea is:

```text
ONE INSTRUCTION
       ↓
REPEAT
       ↓
REPEAT
       ↓
REPEAT
```

This becomes extremely important once we reach Dart collections.

---

# 🔢 PART 9 — Counting

A loop doesn't have to start at zero.

```dart
for (int i = 1; i <= 5; i++) {
  print(i);
}
```

Output:

```text
1
2
3
4
5
```

Compare:

```dart
i < 5
```

with:

```dart
i <= 5
```

### `<`

```text
0 1 2 3 4
```

### `<=`

```text
1 2 3 4 5
```

Tiny symbol.

Huge difference.

---

# ➕ What Is `i++`?

This:

```dart
i++;
```

means:

```dart
i = i + 1;
```

So:

```text
0 → 1 → 2 → 3 → 4 → 5
```

Similarly:

```dart
i--;
```

means:

```dart
i = i - 1;
```

---

# 🎬 STORY — EXAM COUNTDOWN

Ari has an exam tomorrow.

CampusMate wants to create a countdown:

```text
5
4
3
2
1
🚨 EXAM!
```

We can use:

```dart
for (int i = 5; i >= 1; i--) {
  print(i);
}

print("🚨 EXAM!");
```

Now our loop is moving backwards.

---

# 🎯 CAMPUSMATE CHALLENGE #2

Create a countdown from:

```text
10 → 1
```

Then print:

```text
🚀 Good luck, Ari!
```

Don't copy the example above.

Write it yourself.

---

# 🔁 PART 10 — `while`

Now imagine Ari has a study session.

The rule is:

> "Keep studying while there is time left."

That's naturally expressed with `while`.

```dart
int minutes = 5;

while (minutes > 0) {
  print("Study!");
  minutes--;
}
```

Output:

```text
Study!
Study!
Study!
Study!
Study!
```

---

# 🧠 `while` Mental Model

A `while` loop asks:

> **"Is this still true?"**

```text
          CONDITION
              │
         ┌────┴────┐
         ▼         ▼
       TRUE      FALSE
         │         │
         ▼         ▼
        RUN       STOP
         │
         ▼
      CHECK AGAIN
```

---

# ⚠️ THE INFINITE LOOP

Look carefully:

```dart
int minutes = 5;

while (minutes > 0) {
  print("Study!");
}
```

What's wrong?

`minutes` never changes.

So:

```text
5 > 0 → true
5 > 0 → true
5 > 0 → true
5 > 0 → true
...
```

💀

The loop never stops.

This is an:

# ♾️ Infinite Loop

---

# 🧠 The Golden Loop Question

Whenever you create a loop, ask:

> **"What eventually makes my condition false?"**

If you don't know...

🚨 Stop and check your loop.

---

# 🎬 STORY UPDATE

Ari has another requirement.

When CampusMate starts a task, it must perform it **at least once**, even if the condition is initially false.

For that:

# 🔂 PART 11 — `do...while`

Example:

```dart
int attempts = 0;

do {
  print("Checking connection...");
  attempts++;
} while (attempts < 3);
```

The important difference:

### `while`

```text
CHECK
 ↓
RUN
```

### `do...while`

```text
RUN
 ↓
CHECK
```

So `do...while` always runs **at least once**.

---

# 🧪 Experiment

What happens here?

```dart
int x = 10;

do {
  print("CampusMate");
} while (x < 5);
```

The condition:

```text
10 < 5
```

is false.

But you'll still get:

```text
CampusMate
```

because the body executes before the condition is checked.

---

# 🛑 PART 12 — `break`

Imagine CampusMate is searching for Ari's assignment.

It checks:

```text
Programming
Database
Android
Management
```

Once it finds the assignment, it doesn't need to continue searching.

We can stop a loop using:

```dart
break;
```

Example:

```dart
for (int i = 1; i <= 10; i++) {
  if (i == 5) {
    break;
  }

  print(i);
}
```

Output:

```text
1
2
3
4
```

When `i` reaches 5:

```text
break
 ↓
STOP LOOP
```

---

# ⏭️ PART 13 — `continue`

Now imagine CampusMate wants to check every course **except** a course Ari has already completed.

That's where:

```dart
continue;
```

comes in.

Example:

```dart
for (int i = 1; i <= 5; i++) {
  if (i == 3) {
    continue;
  }

  print(i);
}
```

Output:

```text
1
2
4
5
```

The loop did NOT stop.

It simply skipped iteration 3.

---

# 🧠 Remember

```text
break
 ↓
🚪 LEAVE THE LOOP

continue
 ↓
⏭️ SKIP THIS ROUND
```

---

# 🪆 PART 14 — Nested Loops

Ari has courses.

Each course has assignments.

So conceptually:

```text
Programming
 ├── Assignment 1
 ├── Assignment 2
 └── Assignment 3

Database
 ├── Assignment 1
 ├── Assignment 2
 └── Assignment 3
```

This is where nested loops become useful.

A loop inside another loop:

```dart
for (int course = 1; course <= 2; course++) {
  for (int assignment = 1; assignment <= 3; assignment++) {
    print("Course $course - Assignment $assignment");
  }
}
```

Output:

```text
Course 1 - Assignment 1
Course 1 - Assignment 2
Course 1 - Assignment 3
Course 2 - Assignment 1
Course 2 - Assignment 2
Course 2 - Assignment 3
```

---

# 🧠 Visualize It

```text
COURSE 1
 ├── Assignment 1
 ├── Assignment 2
 └── Assignment 3

COURSE 2
 ├── Assignment 1
 ├── Assignment 2
 └── Assignment 3
```

The outer loop handles:

> Courses.

The inner loop handles:

> Assignments.

We'll use this kind of thinking later when working with real app data.

---

# 🧪 CAMPUSMATE CHALLENGE #3

Ari has:

```text
3 courses
5 assignments each
```

Create nested loops that produce:

```text
Course 1 - Assignment 1
Course 1 - Assignment 2
...
Course 3 - Assignment 5
```

---

# 🧮 PART 15 — `%` + Conditions + Loops

Ari wants CampusMate to identify special numbers.

Remember `%`?

```dart
10 % 2
```

gives:

```text
0
```

So:

```dart
number % 2 == 0
```

means:

> The number is even.

Now combine it with a loop:

```dart
for (int i = 1; i <= 10; i++) {
  if (i % 2 == 0) {
    print(i);
  }
}
```

Output:

```text
2
4
6
8
10
```

We just combined:

```text
LOOP
 +
CONDITION
 +
OPERATOR
```

This is where programming starts getting interesting.

---

# 🎯 CAMPUSMATE CHALLENGE #4 — Attendance Scanner

Imagine these attendance values:

```text
82
74
91
68
79
```

For now, manually test each value.

CampusMate should print:

```text
82 → ✅ Safe
74 → ⚠️ Warning
91 → 🌟 Excellent
68 → ⚠️ Warning
79 → 🙂 Safe
```

Your job:

> Build the conditional logic.

---

# 🧠 PART 16 — Why This Matters for Flutter

Right now we're printing:

```text
⚠️ Warning
```

But eventually Flutter will replace that with an actual UI.

For example:

```text
┌─────────────────────────────────┐
│ 📚 Database                     │
│                                 │
│ Attendance: 68%                 │
│                                 │
│ ⚠️ Attendance below 75%         │
│                                 │
│ Attend the next 3 classes.      │
└─────────────────────────────────┘
```

The UI is different.

The **decision-making logic is the same.**

That's an important idea:

> **Dart handles the logic. Flutter gives that logic a visual home.**

---

# 🎮 PART 17 — Mini Project

## 🏫 CampusMate Attendance Checker

Let's combine everything we've learned.

Ari wants CampusMate to check attendance.

Start with:

```dart
double attendance = 68;
```

The app should classify it:

```text
90+ → 🌟 Excellent
80–89 → ✅ Good
75–79 → 🙂 Safe
Below 75 → ⚠️ Warning
```

Then add:

```text
If attendance is below 75:
    show a warning
```

Then add another rule:

```text
If attendance is below 50:
    show "🚨 Critical"
```

Think carefully about **condition order**.

---

# 💀 BOSS CHALLENGE — FizzBuzz

Now we temporarily leave Ari's university life.

Why?

Because every programmer eventually meets:

# FizzBuzz

Create a loop from:

```text
1 → 30
```

Rules:

```text
Divisible by 3 → Fizz

Divisible by 5 → Buzz

Divisible by both → FizzBuzz

Otherwise → number
```

Expected beginning:

```text
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
...
```

---

# 🧠 Don't Look for the Answer Immediately

Translate the problem into questions.

```text
Is the number divisible by 3?

Is the number divisible by 5?

Is it divisible by BOTH?

What should I print?
```

You're learning something much more important than FizzBuzz.

You're learning:

> **How to translate human instructions into machine logic.**

That is programming.

---

# 🏆 FINAL CAMPUSMATE CHALLENGE

Ari wants to test the entire system.

Build a tiny **CampusMate Console Prototype**.

Your program should:

### 1. Store Ari's information

```text
Name
Age
CGPA
```

### 2. Store attendance for one course

```text
Attendance
```

### 3. Decide the attendance status

```text
90+ → Excellent
80+ → Good
75+ → Safe
Below 75 → Warning
```

### 4. Check whether Ari can take the exam

Requirements:

```text
Attendance >= 75
AND
Fees are paid
```

### 5. Create a countdown

```text
5
4
3
2
1
🚀 Exam Time!
```

### 6. Add an emergency rule

If attendance is below 50:

```text
🚨 CRITICAL ATTENDANCE
```

---

# 🧠 Before You Code

Don't start by typing random Dart.

First turn the problem into logic:

```text
             CAMPUSMATE
                  │
          ┌───────┴───────┐
          ▼               ▼
       ATTENDANCE        FEES
          │               │
          ▼               ▼
      >= 75%?          PAID?
          │               │
          └───────┬───────┘
                  ▼
             EXAM ACCESS
```

Then:

```text
Attendance
    ↓
Classify
    ↓
Warning / Safe / Excellent
```

Then:

```text
Countdown
    ↓
Loop
```

You're not just writing syntax anymore.

You're **designing behavior**.

---

# 🧪 DEBUGGING MISSION

Ari's developer wrote this:

```dart
int attempts = 1;

while (attempts <= 3) {
  print("Login attempt: $attempts");
}
```

CampusMate freezes. 💀

### Your mission:

1. What is wrong?
2. Why does it happen?
3. Fix it.
4. Explain what makes the loop eventually stop.

---

# 🚨 Common Beginner Traps

## ❌ `=` vs `==`

Assignment:

```dart
age = 21;
```

Comparison:

```dart
age == 21;
```

Remember:

```text
=   → PUT this value here

==  → ARE these equal?
```

---

## ❌ Forgetting to update a loop

```dart
while (i < 10) {
  print(i);
}
```

Ask:

> Does `i` ever change?

---

## ❌ Wrong condition order

```dart
if (marks >= 50) {
  print("Pass");
} else if (marks >= 90) {
  print("A");
}
```

The `A` condition becomes unreachable for 90+.

---

## ❌ Off-by-one errors

```dart
i < 10
```

is not the same as:

```dart
i <= 10
```

Always ask:

> **Should the final number be included?**

---

# 📌 CAMPUSMATE KNOWLEDGE CHECK

Before moving on, explain these in your own words:

### 1.

What is a condition?

### 2.

What's the difference between:

```dart
if
```

and:

```dart
if / else
```

### 3.

Why does the order of `else if` conditions matter?

### 4.

What's the difference between:

```text
&&
```

and:

```text
||
```

### 5.

What are the three parts of a `for` loop?

### 6.

What's the difference between `while` and `do...while`?

### 7.

What's the difference between `break` and `continue`?

### 8.

What causes an infinite loop?

If you can explain these without looking at the notes, you're ready.

---

# 🏁 LESSON 02 MILESTONE

Don't check this box just because you read the lesson.

You should be able to **write these yourself**:

* [ ] `if`
* [ ] `if / else`
* [ ] `else if`
* [ ] Nested `if`
* [ ] `&&`
* [ ] `||`
* [ ] `!`
* [ ] `for`
* [ ] `while`
* [ ] `do...while`
* [ ] `break`
* [ ] `continue`
* [ ] Nested loops
* [ ] Conditions inside loops
* [ ] Understand infinite loops
* [ ] Build a countdown
* [ ] Build a number filter
* [ ] Build a grading system
* [ ] Solve FizzBuzz
* [ ] Build the CampusMate Attendance Checker

---

# 💾 CAMPUSMATE — CURRENT STATE

At the end of Lecture 2, our app has evolved:

```text
                 📱 CAMPUSMATE
                       │
             ┌─────────┴─────────┐
             ▼                   ▼
        Student Data        App Logic
             │                   │
             │             ┌─────┴─────┐
             │             ▼           ▼
             │       🔀 Decisions   🔁 Repetition
             │             │           │
             └─────────────┴───────────┘
                           │
                           ▼
                   Smart Decisions
```

CampusMate can now:

```text
👤 Know Ari
🔀 Make decisions
⚠️ Detect problems
🔁 Repeat tasks
🔢 Process numbers
🚨 Generate warnings
```

But there's a problem...

---

# 🚪 THE NEXT PROBLEM

Ari opens the code.

And sees:

```dart
if (attendance < 75) {
  print("Warning");
}

if (cgpa < 2.5) {
  print("Warning");
}

if (feesPaid == false) {
  print("Warning");
}
```

Then Ari adds more features.

And more.

And more.

Soon the same logic is being written everywhere.

```text
copy
paste
copy
paste
copy
paste
```

Ari looks at the code and says:

> **"There has to be a better way to reuse this."**

And Ari is right.

Next, we're going to learn how to package logic into reusable blocks.

# 🧩 NEXT → FUNCTIONS

```text
             FUNCTION
                 │
       ┌─────────┼─────────┐
       ▼         ▼         ▼
     INPUT     LOGIC     OUTPUT
       │         │         │
       └─────────┼─────────┘
                 ▼
              REUSE ♻️
```

> **Lecture 2 taught CampusMate how to think.**
>
> **Lecture 3 will teach CampusMate how to reuse what it knows.** 🚀
