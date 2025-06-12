# MyFragment Android Application

An Android application that demonstrates user authentication, entity dashboard viewing, and detailed entity inspection using a modern architecture approach.

## Features

### 1. **Login Screen**
- User login with **first name** as username and **student ID** (e.g., `s12345678`) as password.
- Handles errors gracefully for unsuccessful login attempts.
- On successful authentication, navigates to the **Dashboard** screen.

### 2. **Dashboard Screen**
- Displays a list of entities using **RecyclerView**.
- Fetches data using a `keypass` from login response.
- Each list item shows a summary (excluding the description).
- Clicking an item navigates to the **Details** screen.

### 3. **Details Screen**
- Shows full entity details including description.
- Structured layout for improved readability.

---

## Technical Stack

- **Language**: Kotlin  
- **Architecture**: MVVM  
- **Dependency Injection**: Hilt  
- **Networking**: Retrofit  
- **UI Components**: RecyclerView, Navigation Component  
- **Testing**: JUnit, Mockito

---

## Project Structure

MyFragment/
├── app/
│   ├── manifests/
│   │   └── AndroidManifest.xml
│   ├── java/
│   │   └── com.example.mygragment/
│   │       ├── RecyclerView/
│   │       │   └── [RecyclerView adapter and related classes]
│   │       ├── ApiClient.kt
│   │       ├── AuthApi.kt
│   │       ├── AuthResponse.kt
│   │       ├── Credentials.kt
│   │       ├── DashboardApi.kt
│   │       ├── DashboardResponse.kt
│   │       ├── Entity.kt
│   │       ├── FragmentA.kt
│   │       ├── FragmentB.kt
│   │       ├── FragmentC.kt
│   │       ├── MainActivity.kt
│   │       └── User.kt
│   ├── res/
│   │   ├── drawable/
│   │   ├── layout/
│   │   │   ├── activity_main.xml
│   │   │   ├── fragment_a.xml
│   │   │   ├── fragment_b.xml
│   │   │   ├── fragment_c.xml
│   │   │   └── item_entity.xml
│   │   ├── menu/
│   │   ├── mipmap/
│   │   ├── navigation/
│   │   │   └── nav_graph.xml
│   │   ├── values/
│   │   └── xml/
│   └── build.gradle.kts
│
├── build.gradle.kts (Project-level)
└── README.md
