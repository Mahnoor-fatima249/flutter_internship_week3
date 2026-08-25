<div align="center">

# 🚀 Flutter Internship - Week 3

### CRUD Operations & Local Data with Provider

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Provider](https://img.shields.io/badge/Provider-State%20Management-FF5722?style=for-the-badge)

**1-Month Flutter Development Internship | Week 3 of 4**

</div>

---

## 📋 Overview

**Week 3** focuses on building a complete **To-Do App** with full CRUD operations using **Provider** for state management. This week demonstrates the transition from `setState()` to a scalable `Provider` pattern.

## 🎯 Objectives

- Build a To-Do App with complete CRUD operations
- Implement Add, Edit, Delete, and Mark as Completed functionality
- Display tasks using `ListView.builder`
- Migrate from `setState()` to **Provider** for state management

## ✨ Features

| Feature | Description |
|---------|-------------|
| **Add Task** | Text input to create new tasks |
| **Edit Task** | Dialog popup to modify existing tasks |
| **Delete Task** | Swipe or tap to remove tasks |
| **Mark Complete** | Checkbox to toggle task completion with strikethrough |
| **ListView.builder** | Efficient lazy rendering of task list |
| **Provider State Management** | `ChangeNotifier` + `Consumer` pattern |

## 🏗️ Architecture

### Before (Week 3 - setState)
```
setState(() {
  _tasks.add(Task(title: "New Task"));
});
```

### After (Week 3 - Provider)
```dart
// In TodoProvider
void addTask(String title) {
  _tasks.add(Task(title: title.trim()));
  notifyListeners();
}

// In Widget
context.read<TodoProvider>().addTask("New Task");
```

## 📂 Project Structure

```
lib/
├── main.dart                      # App entry with ChangeNotifierProvider
├── providers/
│   └── todo_provider.dart         # TodoProvider - State management
├── screens/
│   ├── splash_screen.dart         # Splash / Loading screen
│   ├── login_screen.dart          # Login authentication screen
│   ├── signup_screen.dart         # User registration screen
│   ├── home_screen.dart           # Home with Bottom Nav Bar
│   └── todo_screen.dart           # To-Do App with CRUD
└── widgets/
    ├── custom_button.dart         # Reusable button widget
    ├── custom_textfield.dart      # Reusable text field widget
    └── product_card.dart          # Reusable card widget
```

## 🧠 State Management - Provider

### TodoProvider Class
```dart
class TodoProvider extends ChangeNotifier {
  final List<Task> _tasks = [];

  void addTask(String title)     { /* add + notify */ }
  void editTask(int i, String t) { /* edit + notify */ }
  void deleteTask(int i)         { /* remove + notify */ }
  void toggleCompletion(int i)   { /* toggle + notify */ }
}
```

### Consumer in Widget
```dart
Consumer<TodoProvider>(
  builder: (context, todoProvider, child) {
    return ListView.builder(...);
  },
)
```

## 🛠️ Getting Started

### Prerequisites
- [Flutter SDK](https://docs.flutter.dev/get-started/install) installed
- [Android Studio](https://developer.android.com/studio) or [VS Code](https://code.visualstudio.com/) with Flutter extension

### Installation

```bash
# Clone the repository
git clone https://github.com/Mahnoor-fatima249/flutter_internship_week3.git

# Navigate to project directory
cd flutter_internship_week3

# Install dependencies
flutter pub get

# Run the app
flutter run
```

### Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| `provider` | ^6.1.2 | State management |

## 📸 Screenshots

> Screenshots will be added after app testing.

| Login | Dashboard | To-Do App | Edit Task | Completed Tasks |
|:---:|:---:|:---:|:---:|:---:|
| *Coming Soon* | *Coming Soon* | *Coming Soon* | *Coming Soon* | *Coming Soon* |

## 👩‍💻 Author

**Mahnoor Fatima**
- BSIT 6th Semester Student
- Backend & AI Developer

---

<div align="center">

[← Week 2](https://github.com/Mahnoor-fatima249/flutter_internship_week2) | **Week 3 of 4** | [Week 4 →](https://github.com/Mahnoor-fatima249/flutter_internship_week4)

</div>
