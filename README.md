# MyFragment Android Application

<div align="center">
  <h3>🚀 Modern Android App with MVVM Architecture</h3>
  <p>An Android application demonstrating user authentication, entity dashboard viewing, and detailed entity inspection</p>
  
  <img src="https://img.shields.io/badge/Platform-Android-green.svg" alt="Platform">
  <img src="https://img.shields.io/badge/Language-Kotlin-blue.svg" alt="Language">
  <img src="https://img.shields.io/badge/Architecture-MVVM-orange.svg" alt="Architecture">
  <img src="https://img.shields.io/badge/DI-Hilt-purple.svg" alt="Dependency Injection">
</div>

---

## 📱 Features

| Screen | Description |
|--------|-------------|
| **🔐 Login Screen** | User authentication with first name as username and student ID as password<br/>• Graceful error handling for failed attempts<br/>• Automatic navigation to Dashboard on success |
| **📊 Dashboard Screen** | Entity list display using RecyclerView<br/>• Data fetching via keypass from login response<br/>• Summary view (excludes descriptions)<br/>• Tap-to-navigate to Details |
| **📋 Details Screen** | Complete entity information display<br/>• Includes full description<br/>• Structured layout for readability |

## 🛠️ Technical Stack

```
Language:     Kotlin
Architecture: MVVM (Model-View-ViewModel)
DI:          Hilt
Networking:  Retrofit
UI:          RecyclerView, Navigation Component
Testing:     JUnit, Mockito
```

## 📁 Project Structure

<details>
<summary>Click to expand project structure</summary>

```
MyFragment/
├── 📱 app/
│   ├── 📄 manifests/
│   │   └── AndroidManifest.xml
│   ├── ☕ java/com/example/mygragment/
│   │   ├── 📦 RecyclerView/
│   │   │   └── [Adapters, ViewHolders]
│   │   ├── 🌐 ApiClient.kt
│   │   ├── 🔐 AuthApi.kt
│   │   ├── 📨 AuthResponse.kt
│   │   ├── 🔑 Credentials.kt
│   │   ├── 📊 DashboardApi.kt
│   │   ├── 📈 DashboardResponse.kt
│   │   ├── 🏷️ Entity.kt
│   │   ├── 🧩 FragmentA.kt (Login)
│   │   ├── 🧩 FragmentB.kt (Dashboard)
│   │   ├── 🧩 FragmentC.kt (Details)
│   │   ├── 🏠 MainActivity.kt
│   │   └── 👤 User.kt
│   ├── 🎨 res/
│   │   ├── layout/
│   │   │   ├── activity_main.xml
│   │   │   ├── fragment_a.xml
│   │   │   ├── fragment_b.xml
│   │   │   ├── fragment_c.xml
│   │   │   └── item_entity.xml
│   │   ├── navigation/
│   │   │   └── nav_graph.xml
│   │   ├── drawable/
│   │   ├── mipmap/
│   │   ├── menu/
│   │   ├── values/
│   │   └── xml/
│   └── 🔧 build.gradle.kts
├── 🔧 build.gradle.kts (Project)
└── 📖 README.md
```

</details>

## 🔧 Prerequisites

> **⚠️ Important:** Ensure you have the following installed before proceeding

| Requirement | Version | Notes |
|------------|---------|-------|
| **Android Studio** | Arctic Fox (2020.3.1)+ | Latest stable version recommended |
| **JDK** | Java 11+ | Required for Kotlin compilation |
| **Android SDK** | API Level 21+ | Android 5.0 (Lollipop) minimum |
| **Gradle** | 7.0+ | Usually bundled with Android Studio |

## 🚀 Quick Start

### Step 1: Clone Repository
```bash
git clone https://github.com/yourusername/MyFragment.git
cd MyFragment
```

### Step 2: Open in Android Studio
1. Launch **Android Studio**
2. Select `Open an existing Android Studio project`
3. Navigate to the cloned `MyFragment` directory
4. Click **OK** to open

### Step 3: Sync Dependencies
- Android Studio will auto-sync
- If not: `File` → `Sync Project with Gradle Files`

---

## 📦 Dependencies

<details>
<summary>Click to view all dependencies</summary>

```kotlin
dependencies {
    // 🔄 Hilt - Dependency Injection
    implementation("com.google.dagger:hilt-android:2.44")
    kapt("com.google.dagger:hilt-android-compiler:2.44")
    
    // 🌐 Networking
    implementation("com.squareup.retrofit2:retrofit:2.9.0")
    implementation("com.squareup.retrofit2:converter-gson:2.9.0")
    
    // ⚡ Coroutines
    implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:1.6.4")
    
    // 🧩 Jetpack Components
    implementation("androidx.navigation:navigation-fragment-ktx:2.5.3")
    implementation("androidx.navigation:navigation-ui-ktx:2.5.3")
    implementation("androidx.recyclerview:recyclerview:1.3.0")
    implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:2.6.2")
    implementation("androidx.lifecycle:lifecycle-livedata-ktx:2.6.2")
    
    // 🧪 Testing
    testImplementation("junit:junit:4.13.2")
    testImplementation("org.mockito:mockito-core:4.8.1")
    androidTestImplementation("androidx.test.ext:junit:1.1.5")
    androidTestImplementation("androidx.test.espresso:espresso-core:3.5.1")
}
```

</details>

## 🏗️ Building the Application

### Option 1: Android Studio (Recommended)
```
1. Open project in Android Studio
2. Wait for Gradle sync ⏳
3. Build → Make Project (Ctrl+F9 / Cmd+F9)
4. APK location: app/build/outputs/apk/debug/
```

### Option 2: Command Line
```bash
# Make gradlew executable (Linux/Mac)
chmod +x gradlew

# Build debug APK
./gradlew assembleDebug

# Build release APK
./gradlew assembleRelease
```

---

## ▶️ Running the Application

<table>
<tr>
<td width="50%">

### 🖥️ Android Studio
```
1. Connect device/start emulator
2. Select target device
3. Click Run ▶️ (Shift+F10)
```

</td>
<td width="50%">

### 💻 Command Line
```bash
# Install and run
./gradlew installDebug

# Build + Install
./gradlew assembleDebug installDebug
```

</td>
</tr>
</table>

---

## 📱 Device Setup

### 🤖 Android Emulator
```
Tools → AVD Manager → Create Virtual Device
├── Select device (e.g., Pixel 4)
├── Choose system image (API 21+)
└── Click Finish
```

### 📲 Physical Device
```
1. Enable Developer Options
2. Turn on USB Debugging
3. Connect via USB
4. Accept debugging authorization
```

---

## 🔐 Application Usage

### Login Credentials Format
| Field | Format | Example |
|-------|--------|---------|
| **Username** | First Name | `John` |
| **Password** | Student ID | `s12345678` |

### 🔄 Navigation Flow
```
Login Screen → Dashboard Screen → Details Screen
     ↓              ↓              ↓
  Authenticate   View Entities   Full Details
```

---

## 🧪 Testing

<table>
<tr>
<td width="50%">

### Unit Tests
```bash
# Run all tests
./gradlew test

# Specific test class
./gradlew test --tests "YourTestClass"
```

</td>
<td width="50%">

### Instrumentation Tests
```bash
# Run all instrumentation tests
./gradlew connectedAndroidTest

# Specific test
./gradlew connectedAndroidTest \
  -Pandroid.testInstrumentationRunnerArguments.class=YourTest
```

</td>
</tr>
</table>

## 🐛 Troubleshooting

<details>
<summary>🔧 Common Issues & Solutions</summary>

### Gradle Sync Failed
```bash
# Solutions:
1. Check internet connection
2. File → Invalidate Caches and Restart
3. ./gradlew clean
```

### Build Errors
```bash
# Clean and rebuild:
./gradlew clean
./gradlew build
```

### Network Issues
```
✅ Check device internet connectivity
✅ Verify API endpoints
✅ Check network permissions in manifest
```

### Hilt Compilation Errors
```
✅ Ensure @HiltAndroidApp on Application class
✅ Check all Hilt annotations are correct
✅ Verify kapt plugin is applied
```

</details>

---

## 💡 Architecture Overview

```
┌─────────────────────────────────────────────────────────────┐
│                     📱 PRESENTATION LAYER                   │
├─────────────────────────────────────────────────────────────┤
│  FragmentA (Login) → FragmentB (Dashboard) → FragmentC      │
│                           ↕️                                │
│                    ViewModels (MVVM)                        │
├─────────────────────────────────────────────────────────────┤
│                      🔄 BUSINESS LAYER                      │
├─────────────────────────────────────────────────────────────┤
│                    Repository Pattern                       │
│                           ↕️                                │
│                    Hilt (Dependency Injection)              │
├─────────────────────────────────────────────────────────────┤
│                      🌐 DATA LAYER                          │
├─────────────────────────────────────────────────────────────┤
│  Retrofit APIs → AuthApi, DashboardApi                      │
│  Data Models → User, Entity, Responses                      │
└─────────────────────────────────────────────────────────────┘
```

---

## 📚 Development Notes

> **Key Implementation Details**

- **🏗️ MVVM Architecture**: Clean separation of concerns
- **💉 Hilt DI**: Automatic dependency management  
- **🌐 Retrofit**: Type-safe HTTP client with Coroutines
- **🧭 Navigation Component**: Single Activity, multiple Fragments
- **♻️ RecyclerView**: Efficient list rendering with ViewHolders
- **🔄 Coroutines**: Asynchronous programming for network calls

---

## 🤝 Contributing

<table>
<tr>
<td width="20%"><strong>1. Fork</strong></td>
<td width="80%">Fork the repository to your GitHub account</td>
</tr>
<tr>
<td><strong>2. Branch</strong></td>
<td><code>git checkout -b feature/amazing-feature</code></td>
</tr>
<tr>
<td><strong>3. Commit</strong></td>
<td><code>git commit -m 'Add amazing feature'</code></td>
</tr>
<tr>
<td><strong>4. Push</strong></td>
<td><code>git push origin feature/amazing-feature</code></td>
</tr>
<tr>
<td><strong>5. PR</strong></td>
<td>Open a Pull Request with detailed description</td>
</tr>
</table>

---

## 📄 License

```
MIT License - see LICENSE file for details
```

## 📞 Support

<div align="center">

**Need Help?** 

[![Issues](https://img.shields.io/badge/GitHub-Issues-red?style=for-the-badge&logo=github)](https://github.com/yourusername/MyFragment/issues)
[![Wiki](https://img.shields.io/badge/Project-Wiki-blue?style=for-the-badge&logo=wikipedia)](https://github.com/yourusername/MyFragment/wiki)

</div>

---

<div align="center">
  <h3>🎯 Built with ❤️ using Android Studio and Kotlin</h3>
  <p><strong>Happy Coding! 🚀</strong></p>
</div>
