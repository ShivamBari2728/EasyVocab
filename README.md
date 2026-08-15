
# EasyVocab

EasyVocab is an educational mobile application initially designed to help children improve their vocabulary through structured lessons and interactive assessments.

The application provides separate experiences for **teachers and students**. Teachers can create lessons and assessments, while students can access the learning material and complete tests. Teachers can also review student participation and performance through assessment results.

> **Repository:** Private
> **Platform:** Android / iOS
> **Current Backend:** Firebase
> **Status:** Active development

---

## Overview

EasyVocab was initially developed with a focus on vocabulary learning for children.

The application is designed around a simple learning workflow:

```text
Teacher
   │
   ├── Create Lessons
   │
   ├── Create Tests
   │       ├── Multiple Choice Questions
   │       └── Fill in the Blanks
   │
   └── Review Student Performance
             │
             ▼
          Student
             │
             ├── Attend Lessons
             └── Attempt Tests
```

The goal is to provide teachers with a structured way to create learning content while giving students an interactive environment for learning and assessment.

---

## Key Features

### Lesson Management

Teachers can create and manage lessons that students can access through the application.

The initial content model is focused on vocabulary learning, but the structure is designed to support broader educational content in the future.

### Interactive Assessments

EasyVocab currently supports multiple assessment formats, including:

* Multiple-choice questions
* Fill-in-the-blank questions

The assessment system evaluates student responses and records their results.

### Student Performance

Teachers can view assessment participation and performance, including:

* Students who attended an assessment
* Individual scores
* Assessment results
* Student performance data

This provides teachers with visibility into how students are progressing.

### Authentication

The application currently uses basic **Firebase Authentication** for user authentication and login.


---

## Screenshots


### Authentication

<img  height="240" alt="photo_2026-08-16_00-21-09" src="https://github.com/user-attachments/assets/312d1e23-b469-4266-893e-97006688236c" />
<img height="240" alt="photo_2026-08-16_00-21-11" src="https://github.com/user-attachments/assets/b1b22568-e3dd-4576-89af-436705b3b29b" />


---

### Student Experience

<img  height="240" alt="photo_2026-08-16_00-24-11" src="https://github.com/user-attachments/assets/9049b3a9-8c6e-4d90-89db-e4fbb2128838" />
<img  height="240" alt="photo_2026-08-16_00-24-13" src="https://github.com/user-attachments/assets/4c41a672-50b6-491a-89da-276a8dc092b4" />
<img  height="240" alt="photo_2026-08-16_00-24-15" src="https://github.com/user-attachments/assets/330aeb54-04b3-421d-9762-fe79b67c9748" />
<img  height="240" alt="photo_2026-08-16_00-24-09" src="https://github.com/user-attachments/assets/c7bfc0d4-b5bf-490e-a574-b7077868a7cb" />


---

### Teacher Experience
<img  height="240" alt="photo_2026-08-16_00-25-11" src="https://github.com/user-attachments/assets/cb81d96a-6b4a-4054-910f-4789cae5167e" />
<img  height="240" alt="photo_2026-08-16_00-25-13" src="https://github.com/user-attachments/assets/b9e7cb75-b6e8-48bd-b528-5591b8e10ee8" />
<img  height="240" alt="photo_2026-08-16_00-25-15" src="https://github.com/user-attachments/assets/32ecb7ed-3cce-4d21-a321-03dd99f0fe5b" />
<img  height="240" alt="photo_2026-08-16_00-25-08" src="https://github.com/user-attachments/assets/4988355d-3b84-46ef-9324-5ab46173779a" />


---

## Project Structure

The Flutter application follows a feature-oriented structure separating models, providers, screens, services, and application-level configuration.

```text
lib/
│
├── Models/
│   ├── learningItemsModel.dart
│   ├── learningWordsModel.dart
│   ├── oppositeWordsModel.dart
│   └── TeacherDashboardModel.dart
│
├── Providers/
│   └── practiceProgressProvider.dart
│
├── screens/
│   ├── ClassRoomScreen/
│   │
│   ├── HomeScreen/
│   │   └── homeScreen.dart
│   │
│   ├── LearningScreen/
│   │
│   ├── PracticeScreen/
│   │   ├── PracticeSubjectUI/
│   │   ├── TeacherTestViewer/
│   │   ├── PracticeCards.dart
│   │   └── PracticeHomeScreen.dart
│   │
│   ├── Teacher_Screens/
│   │
│   ├── TestScreen/
│   │   ├── testHomeScreen.dart
│   │   └── mainScreen.dart
│   │
│   └── signUpScreen.dart
│
├── services/
│   ├── learning_words_service.dart
│   └── opposite_words_service.dart
│
├── constants.dart
├── firebase_options.dart
├── generalImports.dart
├── main.dart
├── sessionManager.dart
└── StartupScreen.dart
```

---


## Backend Migration

The current version uses Firebase for authentication and backend functionality.

The backend is planned to migrate toward a dedicated Node.js backend.

---

