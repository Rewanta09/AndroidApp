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
│ ├── manifests/
│ │ └── AndroidManifest.xml
│ ├── java/
│ │ └── com.example.mygragment/
│ │ ├── RecyclerView/
│ │ │ └── [Adapters, ViewHolders]
│ │ ├── ApiClient.kt
│ │ ├── AuthApi.kt
│ │ ├── AuthResponse.kt
│ │ ├── Credentials.kt
│ │ ├── DashboardApi.kt
│ │ ├── DashboardResponse.kt
│ │ ├── Entity.kt
│ │ ├── FragmentA.kt
│ │ ├── FragmentB.kt
│ │ ├── FragmentC.kt
│ │ ├── MainActivity.kt
│ │ └── User.kt
│ ├── res/
│ │ ├── layout/
│ │ │ ├── activity_main.xml
│ │ │ ├── fragment_a.xml
│ │ │ ├── fragment_b.xml
│ │ │ ├── fragment_c.xml
│ │ │ └── item_entity.xml
│ │ ├── navigation/
│ │ │ └── nav_graph.xml
│ │ ├── values/
│ │ └── drawable/, mipmap/, menu/, xml/
├── build.gradle.kts (Project)
└── README.md

---

## 🔌 Dependencies

All dependencies are managed via Gradle Kotlin DSL:

```kotlin
// Hilt for dependency injection
implementation("com.google.dagger:hilt-android:<version>")
kapt("com.google.dagger:hilt-android-compiler:<version>")

// Retrofit for networking
implementation("com.squareup.retrofit2:retrofit:<version>")
implementation("com.squareup.retrofit2:converter-gson:<version>")

// Coroutines
implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:<version>")

// Jetpack components
implementation("androidx.navigation:navigation-fragment-ktx:<version>")
implementation("androidx.navigation:navigation-ui-ktx:<version>")
implementation("androidx.recyclerview:recyclerview:<version>")
implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:<version>")
implementation("androidx.lifecycle:lifecycle-livedata-ktx:<version>")

// Testing
testImplementation("junit:junit:<version>")
testImplementation("org.mockito:mockito-core:<version>")

