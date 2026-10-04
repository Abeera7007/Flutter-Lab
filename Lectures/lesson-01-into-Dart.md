# 🐦 Lesson 01 — Into Dart

### *Before we make Flutter apps, let's teach the computer how to understand us.*

Welcome to your **first real Dart lesson**.

If Flutter is the shiny restaurant 🍽️, then **Dart is the language spoken in the kitchen**.

You can jump straight into Flutter and copy:

```dart
Scaffold(
  body: ...
)
```

…but eventually you'll stare at an error and think:

> **"WHY ARE YOU LIKE THIS 😭"**

So we're going to learn Dart first.

Not all of Dart.

Just enough to start thinking like a programmer.

---

# 🗺️ Today's Adventure

We're going from:

```text
🤨 What even is Dart?
        ↓
🧪 DartPad
        ↓
📦 Data Types
        ↓
➕ Operators
        ↓
📦 Variables
        ↓
🧠 "Ohhh... THAT'S how programs work."
```

By the end, you'll be able to write little programs that actually **remember information, calculate things, and make decisions**.

---

# 🐦 01 — Meet Dart

## So... what IS Dart?

Dart is a programming language developed by Google.

And Flutter?

Flutter is Google's UI toolkit/framework that uses Dart.

Think of it like this:

```text
                 🐦 DART
              Programming
                Language
                    │
                    ▼
              ┌───────────┐
              │  FLUTTER  │
              │           │
              │ UI + Apps │
              └───────────┘
                    │
          ┌─────────┼─────────┐
          ▼         ▼         ▼
       Android     iOS       Web
```

So when we write Flutter code, we're still writing **Dart**.

---

# 🤔 Why not just learn Flutter?

Because Flutter code contains programming concepts everywhere.

For example:

```dart
String username = "Abeera";
```

That's Dart.

This:

```dart
if (isLoggedIn) {
  print("Welcome!");
}
```

is Dart.

And this:

```dart
List<String> names = [];
```

is also Dart.

Flutter adds the UI layer on top.

So:

> **Dart teaches you how to think. Flutter teaches you how to build the app.**

---

# 🧪 02 — Meet DartPad

Before installing 47 things and sacrificing your laptop to Android Studio...

Let's write some Dart **in the browser**.

That's where **DartPad** comes in.

DartPad lets you experiment with Dart without creating a full Flutter project.

Think:

```text
Idea
 ↓
DartPad
 ↓
Run ▶️
 ↓
"Ohhh!"
```

Perfect for tiny experiments.

---

# 👋 Your First Dart Program

Start with:

```dart
void main() {
  print("Hello, Dart!");
}
```

Run it.

You should get:

```text
Hello, Dart!
```

Congratulations.

You have officially made the computer say something.

Humanity may never recover.

---

# 🔍 Let's Interrogate the Code

Look at:

```dart
void main() {
  print("Hello, Dart!");
}
```

It looks intimidating for approximately 4 seconds.

Let's break it down.

---

## `main()`

```dart
void main() {
}
```

This is where a simple Dart program starts.

Think:

```text
🚦 Program starts
       ↓
    main()
       ↓
   Code runs
```

---

## `print()`

```dart
print("Hello!");
```

means:

> "Computer, show this in the console."

Try:

```dart
void main() {
  print("Flutter Lab");
  print("Dart is kinda fun.");
  print(21);
}
```

Output:

```text
Flutter Lab
Dart is kinda fun.
21
```

---

# 🧪 Tiny Experiment #1

Before running this:

```dart
void main() {
  print(10);
  print(20);
  print(10 + 20);
}
```

### STOP ✋

Predict the output.

<details>
<summary>👀 Reveal Answer</summary>

```text
10
20
30
```

</details>

---

# 📦 03 — Data Types

Now we're getting somewhere.

Programs deal with **data**.

Your app might need to remember:

```text
👤 Name
🎂 Age
💰 Price
📱 Phone number
🔐 Logged-in status
📚 List of courses
```

But these aren't all the same kind of information.

For example:

```text
21
```

is a number.

While:

```text
"Abeera"
```

is text.

And:

```text
true
```

is a yes/no value.

These categories are called:

# 🧩 Data Types

---

# 🔢 `int` — Whole Numbers

`int` = integer.

Basically:

> **No decimal drama.**

```dart
int age = 21;
int marks = 95;
int students = 50;
```

Valid:

```text
0
1
21
500
-10
```

Not:

```text
3.14
```

because that's a decimal.

---

# 💧 `double` — Decimal Numbers

When decimals enter the chat:

```dart
double price = 99.99;
double height = 5.4;
double temperature = 36.5;
```

Think:

```text
int
 ↓
21

double
 ↓
21.5
```

---

# 🔢 `num` — Numbers in General

`num` can represent both integers and decimal numbers.

```dart
num score = 95;

score = 95.5;
```

So:

```text
num
├── int
└── double
```

For now:

> `num` = "I know this is a number, but it might be whole or decimal."

---

# 📝 `String` — Text

Anything you're treating as text:

```dart
String name = "Abeera";
String city = "Lahore";
String course = "Flutter Lab";
```

Strings usually live inside quotes:

```dart
"Hello"
```

or:

```dart
'Hello'
```

---

# ⚠️ Fun Example

Look at this:

```dart
String phone = "03001234567";
```

"But that's numbers!"

Yep.

But we're treating them as **text**, not doing maths with them.

We don't want:

```text
03001234567 + 5
```

We want:

```text
"03001234567"
```

So the context matters.

---

# ✅ `bool` — Yes or No

A boolean has exactly two values:

```dart
true
false
```

Examples:

```dart
bool isStudent = true;
bool isLoggedIn = false;
bool hasInternet = true;
```

Think of it as a tiny switch:

```text
🔘 true
🔘 false
```

---

# 🧠 The Big Four

For now, tattoo these into your brain:

```text
int
 ↓
Whole number

double
 ↓
Decimal number

String
 ↓
Text

bool
 ↓
true / false
```

---

# 🧪 Tiny Experiment #2

Predict which data type each value belongs to:

```text
42
3.14
"42"
false
"Flutter"
100.0
```

### Answer

```text
42          → int
3.14        → double
"42"        → String
false       → bool
"Flutter"   → String
100.0       → double
```

Notice:

```text
42
```

and:

```text
"42"
```

are NOT the same thing.

One is a number.

One is text.

---

# 📚 04 — A Sneak Peek at Collections

Dart also has types that hold **multiple values**.

## List

```dart
List<String> friends = [
  "Ali",
  "Sara",
  "Abeera"
];
```

Think:

```text
friends
   │
   ├── Ali
   ├── Sara
   └── Abeera
```

We'll properly explore collections later.

---

# 🗺️ Map

A `Map` stores information as:

```text
KEY → VALUE
```

Example:

```dart
Map<String, dynamic> student = {
  "name": "Abeera",
  "age": 21
};
```

Think:

```text
"name" → "Abeera"
"age"  → 21
```

This becomes VERY useful later when working with APIs and JSON.

---

# ⚙️ 05 — Operators

Okay.

We can store information.

Now let's **do something with it**.

Meet:

# ⚙️ Operators

Operators are symbols that perform operations.

Like:

```text
+   -   *   /
```

You already know these from maths.

Congratulations.

Your maths teacher was secretly preparing you for programming.

---

# ➕ Addition

```dart
print(10 + 5);
```

Output:

```text
15
```

---

# ➖ Subtraction

```dart
print(10 - 5);
```

Output:

```text
5
```

---

# ✖️ Multiplication

```dart
print(10 * 5);
```

Output:

```text
50
```

---

# ➗ Division

```dart
print(10 / 5);
```

Output:

```text
2.0
```

Notice:

```text
10 / 5
↓
2.0
```

---

# 🤨 Wait... Why `2.0`?

Because `/` performs normal division and produces a numeric result that can represent decimals.

If you specifically want integer division:

```dart
print(10 ~/ 3);
```

Output:

```text
3
```

---

# 🤯 `~/`

This:

```dart
~/
```

means integer division.

Compare:

```dart
print(10 / 3);
print(10 ~/ 3);
```

Result conceptually:

```text
3.333...
3
```

---

# 🧮 `%` — The Remainder Machine

This one is secretly VERY useful.

```dart
print(10 % 3);
```

Output:

```text
1
```

Because:

```text
10 ÷ 3
= 3 remainder 1
```

So `%` gives us the remainder.

---

# 🎮 Why Do We Care About `%`?

Imagine checking if a number is even.

```dart
print(10 % 2);
```

Result:

```text
0
```

Because 10 divides perfectly by 2.

But:

```dart
print(7 % 2);
```

Result:

```text
1
```

So:

```text
remainder 0 → even
remainder 1 → odd
```

Congratulations.

You just discovered one of the oldest programming tricks.

---

# 🧪 Tiny Experiment #3

Predict:

```dart
print(17 % 5);
```

<details>
<summary>👀 Reveal</summary>

```text
2
```

Because:

```text
17 ÷ 5 = 3 remainder 2
```

</details>

---

# 📦 06 — Variables

Now we get to one of the BIGGEST concepts in programming.

# Variables.

A variable is basically a **named place for storing information**.

Imagine:

```text
┌─────────────┐
│     age     │
├─────────────┤
│      21     │
└─────────────┘
```

In Dart:

```dart
int age = 21;
```

That's it.

---

# 🔍 Anatomy of a Variable

Look carefully:

```dart
int age = 21;
```

Breakdown:

```text
int       age       =       21
│         │         │        │
│         │         │        └── value
│         │         └─────────── assignment
│         └──────────────────── variable name
└────────────────────────────── type
```

So we're saying:

> "Create a variable called `age`, make it an integer, and store `21` inside it."

---

# 🧪 Let's Make Some

```dart
String name = "Abeera";
int age = 21;
double cgpa = 3.01;
bool isStudent = true;
```

Now our program knows:

```text
name       → "Abeera"
age        → 21
cgpa       → 3.01
isStudent  → true
```

---

# 🖨️ Print Your Variables

```dart
void main() {
  String name = "Abeera";
  int age = 21;

  print(name);
  print(age);
}
```

Output:

```text
Abeera
21
```

---

# 🔄 Variables Can Change

Watch:

```dart
int age = 21;

age = 22;

print(age);
```

Output:

```text
22
```

We changed the value.

Think:

```text
age
 ↓
21
 ↓
22
```

The **variable** stayed the same.

The **value** changed.

---

# 🤖 `var` — Let Dart Figure It Out

Instead of:

```dart
int age = 21;
```

we can write:

```dart
var age = 21;
```

Dart looks at:

```text
21
```

and thinks:

> "That's an integer."

So it understands the type for us.

---

# 🔍 Compare

```dart
int age = 21;
```

We're explicitly saying:

> "age is an int."

While:

```dart
var age = 21;
```

means:

> "Dart, you figure out what type this is."

Dart isn't confused.

It figures it out.

---

# ⚠️ Important `var` Myth

This:

```dart
var age = 21;
```

does NOT mean:

> "age can become literally anything."

You don't get:

```dart
var age = 21;
age = "hello";
```

and magically escape the type system.

Dart infers the type.

---

# 🔒 `final` — Set Once

Sometimes you don't want a variable to be reassigned.

Example:

```dart
final username = "Abeera";
```

Now:

```dart
username = "Sara";
```

❌ Nope.

Think:

```text
final
 ↓
Assign once
 ↓
Hands off 🔒
```

---

# ⚡ `const` — Compile-Time Constant

Then there's:

```dart
const appName = "Flutter Lab";
```

A `const` value is known at compile time.

For now, remember:

```text
var
 ↓
Can change

final
 ↓
Set once

const
 ↓
Compile-time constant
```

We'll revisit `final` and `const` later when Flutter starts throwing them at you from every direction.

---

# 🧠 Variable Cheat Sheet

| Keyword | Can reassign? | Example           |
| ------- | ------------: | ----------------- |
| `var`   |             ✅ | `var age = 21;`   |
| Type    |             ✅ | `int age = 21;`   |
| `final` |             ❌ | `final age = 21;` |
| `const` |             ❌ | `const age = 21;` |

---

# ⚠️ 07 — `=` vs `==`

This WILL try to betray you.

## `=`

Means:

> **Assign this value.**

```dart
age = 21;
```

## `==`

Means:

> **Are these two values equal?**

```dart
age == 21
```

So:

```text
=     → PUT
==    → ASK
```

Think:

```text
age = 21
```

> "Age, here's your new value."

While:

```text
age == 21
```

> "Hey age... are you 21?"

---

# 🧪 Tiny Experiment #4

What do these produce?

```dart
int age = 21;

print(age == 21);
print(age == 18);
```

Answer:

```text
true
false
```

Because:

```text
21 == 21 → true
21 == 18 → false
```

---

# 🔎 08 — Comparison Operators

We can compare values using:

```text
==     equal
!=     not equal
>      greater than
<      less than
>=     greater than or equal
<=     less than or equal
```

Example:

```dart
int age = 21;

print(age > 18);
```

Output:

```text
true
```

Because:

```text
21 > 18
```

is true.

---

# 🧠 09 — Logical Operators

Now we can combine conditions.

## `&&` — AND

Both need to be true.

```dart
bool hasEmail = true;
bool hasPassword = true;

print(hasEmail && hasPassword);
```

Output:

```text
true
```

Think:

```text
true AND true
      ↓
    true
```

But:

```text
true AND false
      ↓
    false
```

---

# `||` — OR

At least one needs to be true.

```dart
bool hasEmail = true;
bool hasPhone = false;

print(hasEmail || hasPhone);
```

Output:

```text
true
```

Because one is true.

---

# `!` — NOT

Flips a boolean.

```dart
bool isLoggedIn = true;

print(!isLoggedIn);
```

Output:

```text
false
```

Think:

```text
true
 ↓
!
 ↓
false
```

---

# 🎮 Operator Cheat Sheet

```text
MATH
+      add
-      subtract
*      multiply
/      divide
~/     integer divide
%      remainder

COMPARISON
==     equal
!=     not equal
>      greater
<      less
>=     greater/equal
<=     less/equal

LOGIC
&&     AND
||     OR
!      NOT

ASSIGNMENT
=      assign
```

---

# 🧪 LEVEL 1 — Warm-Up

Write a Dart program that stores:

```text
Name
Age
City
```

Then prints them.

Don't copy this:

```dart
String name = "Abeera";
int age = 21;
String city = "Lahore";
```

Try writing it yourself.

---

# 🧪 LEVEL 2 — Mini Calculator

Create:

```dart
int price = 500;
int quantity = 3;
```

Calculate:

```text
total price
```

Your program should produce:

```text
1500
```

---

# 🧪 LEVEL 3 — Even or Odd

Create:

```dart
int number = 17;
```

Use `%` to determine whether it's divisible by 2.

Hint:

```dart
number % 2
```

Don't worry about writing `if` yet.

Just inspect the result.

---

# 🧪 LEVEL 4 — Student Profile

Create variables for:

```text
👤 Name
🎂 Age
📚 Number of courses
📊 CGPA
🎓 Is enrolled
```

Then print everything.

Example output:

```text
Name: Abeera
Age: 21
Courses: 5
CGPA: 3.01
Enrolled: true
```

---

# 🧠 LEVEL 5 — Predict Before Running

What does this produce?

```dart
void main() {
  int a = 10;
  int b = 3;

  print(a + b);
  print(a - b);
  print(a * b);
  print(a / b);
  print(a ~/ b);
  print(a % b);
}
```

Don't run it yet.

Write your prediction.

Then run it.

---

# 💀 BOSS LEVEL — No Copy-Paste

Close this lesson.

Open DartPad.

Your mission:

Build a tiny **shopping calculator**.

It should have:

```text
Product price
Quantity
Discount
Final price
```

For example:

```text
Price: 1000
Quantity: 2
Discount: 100

Final: 1900
```

### Rules:

❌ Don't copy a complete solution.

❌ Don't ask AI to write it for you.

✅ Search syntax if you forget.

✅ Experiment.

✅ Break it.

✅ Fix it.

That's programming.

---

# 🧠 What Just Happened?

You started with:

```text
"What is Dart?"
```

and ended with:

```text
DATA
 ↓
VARIABLES
 ↓
OPERATORS
 ↓
CALCULATIONS
 ↓
RESULT
```

That's the beginning of programming.

---

# 🔥 Why This Matters in Flutter

Eventually, these tiny concepts control actual applications.

For example:

```dart
bool isLoggedIn = true;
```

can decide:

```text
true
 ↓
🏠 Home Screen
```

while:

```text
false
 ↓
🔐 Login Screen
```

Or:

```dart
double price = 500;
int quantity = 3;

double total = price * quantity;
```

can become:

```text
🛒 Cart
────────────
Price     500
Quantity    3
────────────
Total    1500
```

So don't underestimate these tiny lines.

They become the logic behind real apps.

---

# 🧠 Mental Model

Remember this:

```text
             PROGRAM
                │
                ▼
        ┌───────────────┐
        │     DATA      │
        └───────┬───────┘
                │
                ▼
          VARIABLES
                │
                ▼
          OPERATORS
                │
                ▼
          CALCULATION
                │
                ▼
             RESULT
```

Later we'll add:

```text
              RESULT
                │
                ▼
           CONDITIONS
                │
                ▼
             LOOPS
                │
                ▼
           FUNCTIONS
                │
                ▼
             CLASSES
                │
                ▼
             FLUTTER
                │
                ▼
           📱 REAL APP
```

---

# 🏁 Lesson 01 Milestone

Don't mark this lesson complete just because you read it.

Mark it complete when you can open DartPad and create a small program **without copying the answer**.

You should be able to:

* [ ] Explain what Dart is
* [ ] Explain Dart's relationship with Flutter
* [ ] Run Dart in DartPad
* [ ] Use `main()`
* [ ] Use `print()`
* [ ] Explain `int`
* [ ] Explain `double`
* [ ] Explain `String`
* [ ] Explain `bool`
* [ ] Create variables
* [ ] Use `var`
* [ ] Explain `final`
* [ ] Explain `const`
* [ ] Perform arithmetic
* [ ] Use `%`
* [ ] Compare values
* [ ] Explain `=` vs `==`
* [ ] Use `&&`
* [ ] Use `||`
* [ ] Use `!`
* [ ] Build a tiny calculator

---

# 🎯 The One Thing I Want You to Remember

You don't learn programming by reading code.

You learn programming by doing this:

```text
👀 See code
     ↓
🤔 Predict
     ↓
▶️ Run it
     ↓
💥 Break it
     ↓
🐛 Debug it
     ↓
🧠 Understand it
     ↓
⌨️ Write it yourself
```

So don't just read this lesson.

**Open DartPad.**

Type.

Experiment.

Make something ridiculous.

Make the computer calculate your imaginary shopping bill.

Make a variable called:

```dart
String mood = "confused";
```

Then change it to:

```dart
mood = "I GET IT";
```

Because that's exactly how learning to code feels.

---

# 🚀 NEXT LESSON

We've learned how to **store and manipulate information**.

Now we need to teach Dart how to **make decisions**.

```text
Variables
    ↓
Operators
    ↓
🔥 Conditions
    ↓
if / else
    ↓
Loops
    ↓
Functions
```

### Next stop:

# 🧠 Dart Logic — Making Decisions

> **The computer can calculate.**
>
> **Now let's teach it how to think.** 🐦
