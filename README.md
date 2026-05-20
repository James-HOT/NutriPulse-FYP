# NutriPulse-FYP

NutriPulse-FYP is an Android health and wellness application that provides role-based experiences for **Adults**, **Children**, and **Elderly** users.  
The project includes health tracking, medication support, nutrition workflows, activity/sleep monitoring, and AI-assisted recommendation features across multiple modules.

## Table of Contents

- [Overview](#overview)
- [Core Features](#core-features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Build and Run](#build-and-run)
- [Useful Gradle Tasks](#useful-gradle-tasks)
- [Configuration Notes](#configuration-notes)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository contains a native Android application organized around user groups and health domains.  
Based on the current module/package naming, the app includes:

- Role-specific home flows (`Adults`, `Children`, `Elderly`)
- Medication management and reminder handling
- Nutrition, food records, and meal planning features
- Activity and sleep tracking flows
- Consultation and report/history experiences
- AI-powered recommendation/analysis helper classes

## Core Features

### Adults

- Activity tracking and related history
- Sleep tracking and sleep reminder components
- Medication management, logs, and reminders
- Goal setting and recommendation components
- Nutrition and diet records

### Children

- Child health monitoring and growth/report features
- Kids fit tracker and badge/reward style progress
- Sleep hygiene tracker flows
- Medication manager with reminder support
- Online consultation and Q&A pages

### Elderly

- Health management dashboards and reports
- Medication and reminder flows
- Health challenge, social support, and lifestyle modules
- Device/data source integration screens
- Health question and recommendation components

## Tech Stack

- **Platform:** Android (native)
- **Language:** Java (primary in `app/src/main/java`)
- **Build System:** Gradle with Kotlin DSL (`*.gradle.kts`)
- **UI:** Android XML layouts (`app/src/main/res/layout`)
- **Data/Storage:** Local helper classes (for example, multiple `*DatabaseHelper` classes)
- **Automation:** Broadcast receivers and Android service components in module packages

## Project Structure

```text
NutriPulse-FYP/
├─ app/
│  ├─ src/main/
│  │  ├─ java/com/example/nutripulseftp/
│  │  │  ├─ Adults/
│  │  │  ├─ Children/
│  │  │  ├─ Elderly/
│  │  │  └─ loginpage/
│  │  ├─ res/
│  │  │  ├─ layout/
│  │  │  ├─ drawable/
│  │  │  └─ values/
│  │  └─ AndroidManifest.xml
├─ build.gradle.kts
├─ settings.gradle.kts
└─ gradle.properties
```

## Prerequisites

Before running the app locally, make sure you have:

- **JDK 17** (recommended for modern Android Gradle Plugin setups)
- **Android Studio** (latest stable recommended)
- **Android SDK** installed (matching project compile/target settings)
- **Git**
- **Git LFS** (required for this repository content)

## Getting Started

1. Clone the repository:

   ```bash
   git clone <your-repository-url>
   cd NutriPulse-FYP
   ```

2. Install Git LFS (if not already installed):

   ```bash
   git lfs install
   ```

3. Download actual LFS-managed files:

   ```bash
   git lfs pull
   ```

4. Open the project in Android Studio.

5. Allow Gradle sync to complete.

## Build and Run

### Option A: Android Studio

1. Open the project root in Android Studio.
2. Select an emulator or connected device.
3. Click **Run** for the `app` module.

### Option B: Command Line (after LFS files are available)

On macOS/Linux:

```bash
chmod +x gradlew
./gradlew assembleDebug
./gradlew installDebug
```

## Useful Gradle Tasks

Run from project root:

```bash
./gradlew tasks
./gradlew clean
./gradlew assembleDebug
./gradlew test
./gradlew connectedAndroidTest
./gradlew lint
```

## Configuration Notes

- If the app uses API keys, tokens, or service credentials, keep them out of source control.
- Prefer `local.properties`, environment variables, or ignored config files for machine-specific secrets.
- Verify package identifiers and app IDs if you need custom build variants.

## Troubleshooting

### Files look like `version https://git-lfs.github.com/spec/v1`

This indicates Git LFS pointers were checked out without fetching real file contents.

Fix:

```bash
git lfs install
git lfs pull
```

### Gradle wrapper script does not execute

```bash
chmod +x gradlew
```

### Gradle sync/build fails

- Confirm Java version compatibility (JDK 17 recommended).
- Re-sync Gradle in Android Studio.
- Run `./gradlew clean` and retry.
- Ensure Android SDK components required by the project are installed.

## Contributing

1. Create a feature branch.
2. Make focused, reviewable changes.
3. Run tests/lint before opening a PR.
4. Open a pull request with clear scope and testing notes.

## License

No license is currently defined in this repository.  
Add a `LICENSE` file (for example, MIT, Apache-2.0, or GPL) if you plan to distribute this project.
