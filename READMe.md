# Bill Odida — Senior Mobile Engineer | Android & Kotlin Multiplatform

<p align="left">
  <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android" />
  <img src="https://img.shields.io/badge/Kotlin_Multiplatform-F88900?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin Multiplatform" />
  <img src="https://img.shields.io/badge/Compose_Multiplatform-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" alt="Compose Multiplatform" />
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/Ktor-087CFA?style=for-the-badge&logo=ktor&logoColor=white" alt="Ktor" />
</p>

<p align="left">
  <a href="https://billodida.dev/"><img src="https://img.shields.io/badge/Portfolio-billodida.dev-181717?style=flat-square&logo=googlechrome&logoColor=white" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/bill-odida-282140186/"><img src="https://img.shields.io/badge/LinkedIn-Bill_Odida-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="https://dev.to/wolfof420street"><img src="https://img.shields.io/badge/DEV.to-wolfof420street-0A0A0A?style=flat-square&logo=devdotto&logoColor=white" alt="DEV.to" /></a>
  <a href="mailto:bill@billodida.dev"><img src="https://img.shields.io/badge/Email-bill%40billodida.dev-EA4335?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
</p>

Mobile software engineer specializing in **native Android (Jetpack Compose, Coroutines, Flow)** and **Kotlin Multiplatform (KMP / Compose Multiplatform)**, with production experience extending to **Flutter** cross-platform development and **Ktor** backend services.

I focus on what makes client applications dependable in production: offline-first data synchronization, resilient local persistence, lifecycle-aware concurrency, clear architectural boundaries (Clean Architecture / UDF), and reproducible build and release pipelines. In addition to software engineering, I am pursuing **Data Science and Analytics**, applying statistical thinking and data modeling to system design.

---

## Selected Engineering Projects

### [Leta-Pay-KMP](https://github.com/Wolfof420Street/Leta-Pay-KMP) &mdash; Kotlin Multiplatform & Distributed Architecture

![Kotlin Multiplatform](https://img.shields.io/badge/KMP-7F52FF?style=flat-square&logo=kotlin&logoColor=white)
![Compose Multiplatform](https://img.shields.io/badge/Compose_Multiplatform-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![Ktor](https://img.shields.io/badge/Ktor_3.x-087CFA?style=flat-square&logo=ktor&logoColor=white)
![Gradle Plugins](https://img.shields.io/badge/Gradle_Convention_Plugins-02303A?style=flat-square&logo=gradle&logoColor=white)
![CI/CD](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

*A modular Kotlin Multiplatform wallet and client application sharing domain logic and UI across Android, iOS, Desktop, and Web, backed by a production-structured Ktor backend service.*
- **Cross-Platform UI & Architecture:** Built with Compose Multiplatform (`cmp-shared`, `cmp-navigation`, `cmp-android`, `cmp-ios`, `cmp-desktop`, `cmp-web`) adhering to Unidirectional Data Flow.
- **Backend Service:** Ktor 3.x microservice (`backend-ktor`) handling RS256 JWT authentication, SIWE verification, rate limiting, and client orchestration.
- **Build & CI Engineering:** Custom Gradle convention plugins (`build-logic`) managing multiplatform target compilation, dependency catalogs, and 10 GitHub Actions workflows for multi-target build validation and deployment.

### [WeatherAIApp](https://github.com/Wolfof420Street/WeatherAIApp) &mdash; Production-Grade Native Android Engineering

![Android](https://img.shields.io/badge/Android_SDK-3DDC84?style=flat-square&logo=android&logoColor=white)
![Jetpack Compose](https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white)
![Room](https://img.shields.io/badge/Room_DB-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Hilt](https://img.shields.io/badge/Hilt_DI-black?style=flat-square)
![Coroutines & Flow](https://img.shields.io/badge/Coroutines_&_Flow-7F52FF?style=flat-square)

*A reference native Android application engineered to demonstrate modern Android architecture, offline resilience, and dynamic Material 3 design.*
- **Clean Architecture & UDF:** Strict separation of Data, Domain, and UI layers with unidirectional data flow driven by Kotlin Coroutines, StateFlow, and Jetpack ViewModel.
- **Jetpack Compose UI:** Material 3 dynamic color theming, custom Canvas cubic-spline temperature charts (`HourlyChart.kt`), haptic interaction, and responsive bottom sheets.
- **Offline-First & Concurrency:** Room persistence (`WeatherDatabase`, `WeatherDao`) serving local cached state, integrated with active connectivity monitoring (`AndroidNetworkMonitor`) and exponential backoff retry policies (`RetryStrategy`).
- **Testing & Verification:** Comprehensive unit test suite covering ViewModel, Repository, and UseCase layers using `MainDispatcherRule`, verified via automated GitHub Actions CI pipelines.

### [SyncForge (`flutter_sync_engine`)](https://github.com/Wolfof420Street/flutter_sync_engine) &mdash; Distributed Mobile Synchronization Engine

![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Drift SQLite](https://img.shields.io/badge/Drift_SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![CRDTs](https://img.shields.io/badge/CRDT_Engine-6f42c1?style=flat-square)

*An open-source, backend-agnostic offline synchronization engine for Flutter applications requiring deterministic conflict resolution and durable local writes.*
- **CRDT Core:** Implemented in pure Dart with state-based Conflict-free Replicated Data Types (G-Counter, G-Set, LWW-Register) and vector clocks for distributed causal ordering.
- **Storage & Code Generation:** Features a Drift (SQLite) persistence adapter and a dedicated generator package (`sync_engine_generator`) using `build_runner` to produce schema serializers for `@Syncable` models.
- **Verification:** Verified through property-based tests, outbox serialization checks, and multi-replica convergence integration tests. Documented in depth in [*Building Offline-First Flutter Apps with SyncForge*](https://dev.to/wolfof420street/building-offline-first-flutter-apps-with-syncforge-36cl).

### [TitleTrust](https://github.com/Wolfof420Street/TitleTrust) &mdash; Realtime Investigation Platform & Device Security

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Redis Streams](https://img.shields.io/badge/Redis_Streams-DC382D?style=flat-square&logo=redis&logoColor=white)
![Device Security](https://img.shields.io/badge/Device_Signing-black?style=flat-square)

*A distributed land verification system combining a resilient Flutter client with a FastAPI and Redis Streams backend for high-integrity audit trails.*
- **Mobile Resilience & Streaming:** Client-side Server-Sent Events (SSE) streaming with sequence-aware event deduplication, reconnection coordinators, and offline session resilience.
- **Security & Integrity:** Device-bound cryptographic request signing, tamper-evident audit logs with deterministic SHA-256 hashing, and transport-level hardening.
- **System Architecture:** Detailed in the technical case study [*I Built an AI Land Fraud Detector for Kenya*](https://dev.to/wolfof420street/i-built-an-ai-land-fraud-detector-for-kenya-heres-the-full-engineering-story-4n5).

---

## Commercial & Production Applications

- **[ChurchPad](https://billodida.dev/projects/churchpad)** &mdash; Mobile community platform serving **10,000+ active users** ([Google Play](https://play.google.com/store/apps/details?id=net.vomoz.vomoznet.android.churchpad) / [App Store](https://apps.apple.com/us/developer/churchpad-llc/id1572138872)). Led Android architecture, in-app subscription billing, background isolate synchronization, and automated release pipelines.
- **[Dabclassic Radio](https://billodida.dev/projects/dabclassic-radio)** &mdash; Production audio streaming client on [Google Play](https://play.google.com/store/apps/details?id=com.dabclassic.player) and [App Store](https://apps.apple.com/us/app/dabclassic-radio/id6468898926). Engineered using Android, Kotlin, and Media3 / ExoPlayer with battery-aware buffering and foreground service management for background audio playback.
- **[Affirmi](https://billodida.dev/projects/affirmi)** &mdash; Local-first wellness and reflection application ([Google Play](https://play.google.com/store/apps/details?id=org.wolf) / [affirmi.tech](https://www.affirmi.tech/)). Designed with Kotlin, Jetpack Compose, and cross-platform RevenueCat subscription entitlements.
- **[On-farm Feed Advisor](https://play.google.com/store/apps/details?id=org.ilri.ilrifeedadvisor)** &mdash; Digital advisory mobile application for the International Livestock Research Institute (ILRI) on [Google Play](https://play.google.com/store/apps/details?id=org.ilri.ilrifeedadvisor). Designed to help extension staff and farmers balance livestock feed rations and optimize animal diets using locally available feed resources.
- **[Imara TV](https://www.imara.tv/)** &mdash; Educational video and media streaming platform ([imara.tv](https://www.imara.tv/)) delivering youth-oriented edutainment and digital content in collaboration with community and public health initiatives.

---

## Open-Source Contributions

- **[muxable/rtchat](https://github.com/muxable/rtchat)** &mdash; An open-source streaming chat application built with Flutter and native platform integrations.
  - Implemented native Android sharing intent ingestion ([PR #1178](https://github.com/muxable/rtchat/pull/1178)).
  - Diagnosed and resolved Flutter lifecycle listener memory leaks during widget unmounting ([PR #1224](https://github.com/muxable/rtchat/pull/1224)).

---

## Technical Toolkit

| Domain | Badges & Core Technologies |
| :--- | :--- |
| **Mobile & Multiplatform** | <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white" /> <img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white" /> <img src="https://img.shields.io/badge/Jetpack_Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white" /> <img src="https://img.shields.io/badge/KMP-F88900?style=flat-square&logo=kotlin&logoColor=white" /> <img src="https://img.shields.io/badge/Compose_Multiplatform-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white" /> <img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white" /> <img src="https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white" /> <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" /> |
| **Architecture & Reliability** | <img src="https://img.shields.io/badge/Clean_Architecture-black?style=flat-square" /> <img src="https://img.shields.io/badge/UDF_/_MVI-black?style=flat-square" /> <img src="https://img.shields.io/badge/Coroutines_&_Flow-7F52FF?style=flat-square" /> <img src="https://img.shields.io/badge/Hilt_DI-black?style=flat-square" /> <img src="https://img.shields.io/badge/Room_DB-003B57?style=flat-square&logo=sqlite&logoColor=white" /> <img src="https://img.shields.io/badge/Drift_SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" /> <img src="https://img.shields.io/badge/CRDTs-6f42c1?style=flat-square" /> |
| **Backend & Services** | <img src="https://img.shields.io/badge/Ktor-087CFA?style=flat-square&logo=ktor&logoColor=white" /> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" /> <img src="https://img.shields.io/badge/REST_APIs-black?style=flat-square" /> <img src="https://img.shields.io/badge/SSE_Streaming-black?style=flat-square" /> <img src="https://img.shields.io/badge/Redis_Streams-DC382D?style=flat-square&logo=redis&logoColor=white" /> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" /> <img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black" /> |
| **Build, Testing & DevOps** | <img src="https://img.shields.io/badge/Gradle_Plugins-02303A?style=flat-square&logo=gradle&logoColor=white" /> <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" /> <img src="https://img.shields.io/badge/Fastlane-00F200?style=flat-square&logo=fastlane&logoColor=black" /> <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" /> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" /> |

---

## Data Science & Systems Engineering

Alongside my mobile engineering practice, I am pursuing **Data Science and Analytics** at university. I treat data science as an engineering discipline that informs distributed architectures, fraud detection, and offline heuristics:

- **[African Credit Scoring Pipeline](https://github.com/Wolfof420Street/Credit-Scoring):** A hybrid modeling pipeline coupling a Kotlin data preprocessor (StratifiedGroupKFold splitting, ratio extraction) with a Python CatBoost classification model. Implements Platt probability calibration and Points-to-Double-Odds (PDO) log-odds scoring transformations for credit risk evaluation.

---

## Technical Writing & Field Notes

I regularly write about mobile architecture, concurrency trade-offs, and platform internals on [DEV](https://dev.to/wolfof420street):

- [Building Offline-First Flutter Apps with SyncForge](https://dev.to/wolfof420street/building-offline-first-flutter-apps-with-syncforge-36cl) &mdash; *Designing CRDTs, vector clocks, and durable local storage in Dart.*
- [Wiring Up RevenueCat in a Kotlin Multiplatform App: Entitlements, Webhooks, and Why the Client Should Never Be Trusted](https://dev.to/wolfof420street/wiring-up-revenuecat-in-a-kotlin-multiplatform-app-entitlements-webhooks-and-why-the-client-1387) &mdash; *Cross-platform billing, webhook verification, and state synchronization.*
- [Building Home Screen Widgets for a Kotlin Multiplatform App: Android, iOS, and the Privacy Problem](https://dev.to/wolfof420street/building-home-screen-widgets-for-a-kotlin-multiplatform-app-android-ios-and-the-privacy-problem-3kai) &mdash; *Widget architecture across platforms, Glance, WidgetKit, and background data safety.*

---

## ⚡ GitHub Activity

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Wolfof420Street&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="Wolfof420Street GitHub Stats" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Wolfof420Street&layout=compact&theme=tokyonight&hide_border=true&langs_count=6" alt="Top Languages" />
</p>

---

## Contact & Connect

- **Portfolio:** [billodida.dev](https://billodida.dev/)
- **LinkedIn:** [linkedin.com/in/bill-odida-282140186](https://www.linkedin.com/in/bill-odida-282140186/)
- **GitHub:** [github.com/Wolfof420Street](https://github.com/Wolfof420Street)
- **Email:** [bill@billodida.dev](mailto:bill@billodida.dev)
