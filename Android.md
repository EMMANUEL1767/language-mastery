# Android developer A→Z roadmap: Zero to king in 6 months

> **Daily commitment:** 3–5 hours · **Milestones:** 26 (A–Z) · **Goal:** No Android concept left unanswered

---

## Month 1 — Kotlin & foundations

### A. Kotlin language mastery

**Topics:** Variables, types, null safety, control flow, functions, lambdas, extension functions, scope functions (let/run/apply/also/with), string templates, type aliases, destructuring declarations, operator overloading.

**Goal:** Write any Kotlin construct from memory. Solve 50+ Kotlin exercises on Exercism.

**Resources:**
- [Kotlin official docs — Basics](https://kotlinlang.org/docs/basic-syntax.html)
- [Kotlin Koans (interactive)](https://play.kotlinlang.org/koans/overview)
- [Exercism Kotlin track](https://exercism.org/tracks/kotlin)
- [Kotlin in Action (book) — Dmitry Jemerov](https://www.manning.com/books/kotlin-in-action)

---

### B. Kotlin OOP & advanced types

**Topics:** Classes, data classes, sealed classes, enum classes, value classes, abstract classes, interfaces, generics (in/out variance), reified types, delegation (by keyword), companion objects, object declarations, type-safe builders.

**Goal:** Implement a sealed class hierarchy for a state machine. Build a generic repository interface.

**Resources:**
- [Kotlin docs — Classes & Inheritance](https://kotlinlang.org/docs/classes.html)
- [Kotlin docs — Generics](https://kotlinlang.org/docs/generics.html)
- [Effective Kotlin (book) — Marcin Moskala](https://leanpub.com/effectivekotlin)

---

### C. Coroutines & concurrency

**Topics:** Coroutine basics (launch, async, runBlocking), suspend functions, CoroutineScope, Dispatchers (Main/IO/Default), structured concurrency, SupervisorJob, exception handling (CoroutineExceptionHandler), cancellation & timeouts, channels, mutex, flow basics.

**Goal:** Build a coroutine-powered data fetcher with proper cancellation and error handling from scratch.

**Resources:**
- [Kotlin Coroutines guide (official)](https://kotlinlang.org/docs/coroutines-guide.html)
- [Coroutines deep dive — Manuel Vivo (Android Devs blog)](https://medium.com/androiddevelopers/coroutines-on-android-part-i-getting-the-background-3e0e54d20bb)
- [Kotlin Coroutines: Deep Dive (book) — Marcin Moskala](https://leanpub.com/coroutines)
- [KotlinConf coroutines talk — Roman Elizarov (YouTube)](https://www.youtube.com/watch?v=_hfBv0a09Jc)

---

### D. Kotlin Flow & reactive streams

**Topics:** Cold vs Hot flows, Flow builders (flow{}, flowOf, asFlow), flow operators (map, filter, transform, combine, zip, flatMapConcat/Merge/Latest), StateFlow, SharedFlow, conflate, buffer, catch, onCompletion, flowOn, launchIn, callbackFlow, channelFlow.

**Goal:** Rewrite a LiveData-based feature to use StateFlow + SharedFlow. Implement a real-time search with debounce using flow operators.

**Resources:**
- [Kotlin Flow official docs](https://kotlinlang.org/docs/flow.html)
- [StateFlow and SharedFlow (Android docs)](https://developer.android.com/kotlin/flow/stateflow-and-sharedflow)
- [Android Developers: Kotlin Flows in practice](https://medium.com/androiddevelopers/a-safer-way-to-collect-flows-from-android-uis-23080b1f8bda)

---

### E. Android Studio & project anatomy

**Topics:** Project structure (app/, build.gradle.kts, manifests, res/), Gradle build system (plugins, dependencies, build variants, product flavors, build types), AGP (Android Gradle Plugin), version catalogs (libs.versions.toml), signing configs, ProGuard/R8, AndroidManifest.xml deep dive, resource qualifiers.

**Goal:** Set up a multi-module project with version catalog from scratch. Configure debug/release build types with different API endpoints.

**Resources:**
- [Android developer docs — Project overview](https://developer.android.com/studio/projects)
- [Gradle for Android (official)](https://developer.android.com/build)
- [Now in Android (Google sample project)](https://github.com/android/nowinandroid)

---

## Month 2 — Core Android & Jetpack Compose

### F. Activity & Fragment lifecycle

**Topics:** Activity lifecycle (onCreate → onDestroy), Fragment lifecycle (onAttach → onDetach), savedInstanceState, ViewModel survival across config changes, onSaveInstanceState vs ViewModel, process death & restoration, singleTop/singleTask/singleInstance launch modes, intent flags, taskAffinity, back stack management.

**Goal:** Draw the full lifecycle from memory. Build a demo that survives rotation, process death, and deep links correctly.

**Resources:**
- [Android docs — Activity lifecycle](https://developer.android.com/guide/components/activities/activity-lifecycle)
- [Android docs — Fragment lifecycle](https://developer.android.com/guide/fragments/lifecycle)
- [Process death explained — Pierre-Yves Ricau (YouTube)](https://www.youtube.com/watch?v=JxVnx0MKfHk)

---

### G. Jetpack Compose fundamentals

**Topics:** Composable functions, @Composable annotation, remember, mutableStateOf, State hoisting, recomposition rules, Column/Row/Box, Modifier chain, LazyColumn/LazyRow/LazyGrid, Scaffold, TopAppBar, BottomNavigation, Text/Image/Button/TextField, Material 3 components, theming (MaterialTheme, custom color schemes, typography).

**Goal:** Build a complete 3-screen app in pure Compose with Material 3 theme, no XML.

**Resources:**
- [Jetpack Compose official pathway](https://developer.android.com/courses/jetpack-compose/course)
- [Compose docs — State](https://developer.android.com/develop/ui/compose/state)
- [Composables.com — component catalog](https://www.composables.com/)
- [Thinking in Compose](https://developer.android.com/develop/ui/compose/mental-model)

---

### H. Compose internals & performance

**Topics:** Composition, Layout, Drawing phases, slot table, Composer, restartable vs skippable, @Stable/@Immutable annotations, derivedStateOf, snapshotFlow, remember vs rememberSaveable, LaunchedEffect/DisposableEffect/SideEffect, movableContentOf, CompositionLocal, SubcomposeLayout, Layout intrinsics, custom modifiers, recomposition debugging (Layout Inspector, recomposition counts).

**Goal:** Profile and fix recomposition issues in a complex list. Implement a custom layout modifier.

**Resources:**
- [Compose internals (book) — Jorge Castillo](https://jorgecastillo.dev/compose-internals)
- [Android Developers — Compose performance](https://developer.android.com/develop/ui/compose/performance)
- [Leland Richardson — How Compose Works (YouTube)](https://www.youtube.com/watch?v=6BRlI5zfCCk)

---

### I. Navigation in Compose

**Topics:** Navigation component (NavHost, NavController, NavGraph), argument passing (required, optional, complex types), deep links, nested navigation graphs, bottom nav integration, type-safe navigation with Kotlin Serialization, navigation animation (AnimatedNavHost), multi-back-stack, conditional navigation (auth flows), navigation testing.

**Goal:** Build an app with authenticated/unauthenticated nav graphs, deep link support, and animated transitions.

**Resources:**
- [Compose Navigation docs](https://developer.android.com/develop/ui/compose/navigation)
- [Type-safe navigation in Compose](https://developer.android.com/guide/navigation/design/type-safety)
- [Now in Android — navigation implementation](https://github.com/android/nowinandroid)

---

## Month 3 — Architecture & data layer

### J. Architecture patterns (MVVM, MVI, Clean)

**Topics:** MVVM (ViewModel + StateFlow + UI), MVI (unidirectional data flow, Intent/State/Effect), Clean Architecture (domain/data/presentation layers), Repository pattern, UseCases/Interactors, separation of concerns, mapping between layers (Entity → Domain → UI model), architecture in multi-module projects.

**Goal:** Build the same feature in MVVM and MVI. Articulate trade-offs for each in an interview setting.

**Resources:**
- [Android app architecture guide (official)](https://developer.android.com/topic/architecture)
- [Guide to app architecture — UI layer](https://developer.android.com/topic/architecture/ui-layer)
- [Clean Architecture for Android — Fernando Cejas](https://fernandocejas.com/2018/05/07/architecting-android-reloaded/)
- [MVI architecture — Hannes Dorfmann](http://hannesdorfmann.com/android/model-view-intent/)

---

### K. Dependency injection (Hilt & Koin)

**Topics:** DI principles (IoC, service locator vs DI), Dagger basics (Component, Module, @Inject, @Provides, @Binds, Scope), Hilt (AndroidEntryPoint, HiltViewModel, @InstallIn, custom components), Hilt with Compose, Hilt with WorkManager, testing with Hilt (TestInstallIn, UninstallModules), Koin (module, single, factory, viewModel), Koin vs Hilt trade-offs.

**Goal:** Migrate a manual DI project to Hilt. Set up scoped dependencies (Singleton, Activity, ViewModel).

**Resources:**
- [Hilt documentation (official)](https://developer.android.com/training/dependency-injection/hilt-android)
- [Dagger fundamentals codelab](https://developer.android.com/codelabs/android-dagger)
- [Koin documentation](https://insert-koin.io/docs/quickstart/android)

---

### L. Room database & local storage

**Topics:** Room setup (Database, DAO, Entity), TypeConverters, migrations (auto vs manual), destructive migration, Room with Flow/coroutines, embedded objects, relations (@Relation, @Embedded), FTS (full-text search), multi-mapping return types, pre-packaged databases, Room testing, DataStore (Preferences & Proto), encrypted SharedPreferences, SQLite fundamentals.

**Goal:** Build an offline-first notes app with Room + Flow, including schema migration between versions.

**Resources:**
- [Room persistence library (official)](https://developer.android.com/training/data-storage/room)
- [Room with a View codelab](https://developer.android.com/codelabs/android-room-with-a-view-kotlin)
- [DataStore documentation](https://developer.android.com/topic/libraries/architecture/datastore)

---

### M. Networking (Retrofit, OkHttp, Ktor)

**Topics:** Retrofit (interface definition, converters, call adapters, coroutine integration), OkHttp (interceptors, logging, caching, certificate pinning, connection pooling), Ktor Client (engines, plugins, serialization), kotlinx.serialization vs Moshi vs Gson, error handling strategies (sealed Result types), pagination (Paging 3 with RemoteMediator), network-bound resource pattern, caching strategies (ETags, Cache-Control).

**Goal:** Build a paginated API client with offline caching, proper error handling, and certificate pinning.

**Resources:**
- [Retrofit official site](https://square.github.io/retrofit/)
- [OkHttp documentation](https://square.github.io/okhttp/)
- [Paging 3 library](https://developer.android.com/topic/libraries/architecture/paging/v3-overview)
- [Ktor Client docs](https://ktor.io/docs/client-create-and-configure.html)

---

## Month 4 — Advanced UI, testing & background work

### N. Compose animations & custom drawing

**Topics:** animate*AsState, AnimatedVisibility, AnimatedContent, Crossfade, updateTransition, infiniteTransition, Animatable, AnimationSpec (tween, spring, keyframes), gesture animations, Canvas API (drawLine, drawArc, drawPath), Path operations, custom shapes, Brush (gradient, shader), blend modes, graphicsLayer, custom drawing with DrawScope.

**Goal:** Build an animated onboarding flow and a custom animated chart component from scratch.

**Resources:**
- [Compose animation docs](https://developer.android.com/develop/ui/compose/animation/introduction)
- [Custom drawing in Compose](https://developer.android.com/develop/ui/compose/graphics/draw/overview)
- [Compose animation cookbook (Alex Zhukovich)](https://alexzh.com/jetpack-compose-animations/)

---

### O. Testing pyramid (Unit, Integration, UI)

**Topics:** JUnit 5, MockK (mocking, spying, relaxed mocks, coEvery/coVerify), Turbine (Flow testing), Robolectric, Compose testing (ComposeTestRule, semantics, onNodeWithText, performClick), instrumented tests (AndroidJUnit4), Espresso basics, test coroutines (TestDispatcher, StandardTestDispatcher vs UnconfinedTestDispatcher), Hilt testing, Room in-memory testing, UI testing patterns (Robot pattern), test doubles (fake vs mock vs stub).

**Goal:** Achieve 80%+ test coverage on a feature module. Write unit tests for ViewModel, Repository, and UseCase layers. Write Compose UI tests.

**Resources:**
- [Android testing guide (official)](https://developer.android.com/training/testing)
- [Testing Compose layouts](https://developer.android.com/develop/ui/compose/testing)
- [MockK documentation](https://mockk.io/)
- [Turbine — Flow testing](https://github.com/cashapp/turbine)

---

### P. WorkManager & background processing

**Topics:** WorkManager (OneTimeWorkRequest, PeriodicWorkRequest, Constraints, chaining, unique work, ExistingWorkPolicy), Worker vs CoroutineWorker, input/output data, retry policy (BackoffPolicy), expedited work, foreground services (types: location, mediaPlayback, dataSync), JobScheduler, AlarmManager, Doze mode & App Standby, battery optimization restrictions.

**Goal:** Implement a sync system that chains multiple workers with constraints and handles all edge cases.

**Resources:**
- [WorkManager docs](https://developer.android.com/develop/background-work/background-tasks/persistent/getting-started)
- [Foreground services guide](https://developer.android.com/develop/background-work/services/foreground-services)
- [Background processing guide](https://developer.android.com/develop/background-work/background-tasks)

---

### Q. Notifications, BroadcastReceivers & Services

**Topics:** NotificationCompat, notification channels, notification styles (BigText, BigPicture, Inbox, Messaging), actions, PendingIntent (mutable/immutable), FCM (data vs notification payloads, topic messaging, device groups), BroadcastReceiver (manifest vs context-registered, ordered broadcasts, local broadcasts), bound services, AIDL (IPC), content providers.

**Goal:** Build a notification system with channels, actions, custom styles, and FCM integration. Handle all Android 13+ permission requirements.

**Resources:**
- [Notifications guide](https://developer.android.com/develop/ui/views/notifications)
- [FCM documentation](https://firebase.google.com/docs/cloud-messaging/android/client)
- [BroadcastReceiver docs](https://developer.android.com/reference/android/content/BroadcastReceiver)

---

## Month 5 — Performance, security & advanced patterns

### R. Performance optimization

**Topics:** Android Profiler (CPU, Memory, Network, Energy), baseline profiles, startup optimization (App Startup library, lazy initialization, Macrobenchmark), memory leaks (LeakCanary), R8 shrinking/obfuscation, reducing APK size (App Bundle, resource shrinking, on-demand delivery), overdraw detection, jank detection (FrameTimeline), Compose stability, lazy layout performance (keys, contentType).

**Goal:** Profile a real app, identify 3+ bottlenecks, fix them, and measure before/after. Generate baseline profiles.

**Resources:**
- [Android performance docs](https://developer.android.com/topic/performance)
- [Macrobenchmark](https://developer.android.com/topic/performance/benchmarking/macrobenchmark-overview)
- [LeakCanary](https://square.github.io/leakcanary/)
- [Baseline profiles](https://developer.android.com/topic/performance/baselineprofiles/overview)

---

### S. Security & data protection

**Topics:** Android Keystore system, EncryptedSharedPreferences, BiometricPrompt, certificate pinning (CertificatePinner, network_security_config.xml), SafetyNet/Play Integrity API, root detection, code obfuscation (R8 rules), secure network communication (TLS, HSTS), WebView security, intent redirection vulnerabilities, SQL injection prevention, secure data serialization, OWASP Mobile Top 10.

**Goal:** Implement biometric auth + encrypted storage + certificate pinning + Play Integrity in a demo app.

**Resources:**
- [Android security best practices](https://developer.android.com/topic/security/best-practices)
- [Network security config](https://developer.android.com/privacy-and-security/security-config)
- [OWASP Mobile Security Testing Guide](https://owasp.org/www-project-mobile-security-testing-guide/)

---

### T. Multi-module architecture & modularization

**Topics:** Module types (app, feature, core, data, domain, common), api vs implementation dependencies, module visibility, build time optimization, module graph design, convention plugins, composite builds, dependency management at scale, feature toggles, dynamic feature modules (Play Feature Delivery), navigation across modules.

**Goal:** Modularize a monolithic app into 8+ modules with proper dependency boundaries. Study the Now in Android module graph.

**Resources:**
- [Android modularization guide](https://developer.android.com/topic/modularization)
- [Now in Android — modularization](https://github.com/android/nowinandroid)
- [Modularization by convention — Google I/O talk](https://www.youtube.com/watch?v=16SwTvzDO0A)

---

### U. Accessibility & internationalization

**Topics:** Content descriptions, semantics in Compose, touch target sizing (48dp), TalkBack testing, Switch Access, live regions, custom accessibility actions, traversal order, accessibility scanner, RTL layout support, string resources and plurals, ICU message format, locale-aware formatting (dates, numbers, currency), per-app language preferences, pseudo-locales for testing.

**Goal:** Make an app fully accessible (pass Accessibility Scanner with 0 issues). Add 2 language translations with RTL support.

**Resources:**
- [Accessibility in Compose](https://developer.android.com/develop/ui/compose/accessibility)
- [Android accessibility guide](https://developer.android.com/guide/topics/ui/accessibility)
- [Localization guide](https://developer.android.com/guide/topics/resources/localization)

---

### V. Kotlin Multiplatform & Compose Multiplatform

**Topics:** KMP project setup (shared module, expect/actual), KMP for networking (Ktor), KMP for persistence (SQLDelight), KMP for DI (Koin), Compose Multiplatform basics, sharing UI across Android/iOS/Desktop, platform-specific implementations, KMP vs Flutter vs React Native trade-offs.

**Goal:** Build a KMP project that shares networking + data layer between Android and iOS targets.

**Resources:**
- [KMP documentation](https://kotlinlang.org/docs/multiplatform.html)
- [Compose Multiplatform](https://www.jetbrains.com/compose-multiplatform/)
- [KMP project template](https://kmp.jetbrains.com/)

---

## Month 6 — Expert-level & interview dominance

### W. CI/CD, release engineering & Play Store

**Topics:** GitHub Actions for Android (build, test, lint, publish), Fastlane, signing pipeline (upload key vs app signing key), Play Console (staged rollouts, internal/closed/open tracks, crash reporting, vitals, pre-launch reports), version management (versionCode strategy), App Bundle (split APKs, on-demand modules), in-app updates, in-app reviews, feature flags (Firebase Remote Config).

**Goal:** Set up a full CI/CD pipeline: lint → test → build → sign → deploy to Play Console internal track.

**Resources:**
- [GitHub Actions for Android](https://github.com/marketplace/actions/android-build)
- [Fastlane for Android](https://docs.fastlane.tools/getting-started/android/setup/)
- [Play Console docs](https://developer.android.com/distribute/play-console)

---

### X. Advanced Compose & custom design systems

**Topics:** Custom design system tokens (color, typography, shape, spacing), custom CompositionLocals for theming, building reusable component libraries, adaptive layouts (WindowSizeClass, multi-pane), large screen support (tablets, foldables), Compose + custom views interop, GraphicsLayer composable, custom gesture detection (detectTapGestures, detectDragGestures, detectTransformGestures), nested scrolling interop.

**Goal:** Build a custom design system library with 10+ components. Support phone, tablet, and foldable layouts.

**Resources:**
- [Adaptive layouts in Compose](https://developer.android.com/develop/ui/compose/layouts/adaptive)
- [Custom design systems guide](https://developer.android.com/develop/ui/compose/designsystems/custom)
- [Large screen support](https://developer.android.com/guide/topics/large-screens/overview)

---

### Y. System-level knowledge & interview prep

**Topics:** Android OS internals (Zygote, ART, Binder IPC, AIDL, system services, process lifecycle), Dalvik vs ART, garbage collection (generational, concurrent), class loading, dex compilation, app startup sequence (Application → Activity), Linux kernel basics for Android, memory model (heap, native, graphics), ANR analysis (traces.txt), strict mode, IPC mechanisms.

**Goal:** Explain the entire journey from tapping an app icon to the first frame rendered. Answer any system-level interview question.

**Resources:**
- [Android Internals — Jonathan Levin](http://newandroidbook.com/)
- [ART documentation](https://source.android.com/docs/core/runtime)
- [Android platform architecture](https://developer.android.com/guide/platform)

---

### Z. Capstone: Build, publish & teach

**Topics:** End-to-end project: design → architecture → implement → test → optimize → publish. Code review practices, PR templates, documentation (KDoc, Dokka), open source contribution, technical blogging, interview simulation (system design: design a chat app, design an offline-first app, design an image loading library).

**Goal:** Publish a polished app on Play Store. Write 3 deep-dive technical articles. Ace a mock system design interview.

**Resources:**
- [Android interview questions — MindOrks](https://github.com/MindorksOpenSource/android-interview-questions)
- [System design for mobile — Alex Nguyen](https://github.com/nicknguyen22/android-system-design-interview)
- [Grokking the Mobile System Design interview](https://www.designgurus.io/course/grokking-the-mobile-system-design-interview)
- [Dev.to Android tag (for publishing articles)](https://dev.to/t/android)

---

## Weekly schedule template

| Day | Focus | Hours |
|-----|-------|-------|
| Mon–Fri | Study current milestone topics + code along | 3–4 hrs |
| Saturday | Build milestone project / practice exercises | 4–5 hrs |
| Sunday | Review, write notes, revise previous milestones | 2–3 hrs |

## Key books (full journey)

1. **Kotlin in Action** — Dmitry Jemerov & Svetlana Isakova
2. **Kotlin Coroutines: Deep Dive** — Marcin Moskala
3. **Effective Kotlin** — Marcin Moskala
4. **Compose Internals** — Jorge Castillo
5. **Android Internals** — Jonathan Levin

## Key YouTube channels

- [Android Developers (official)](https://www.youtube.com/@AndroidDevelopers)
- [Philipp Lackner](https://www.youtube.com/@PhilippLackner)
- [Coding with Mitch](https://www.youtube.com/@CodingWithMitch)
- [Stevdza-San](https://www.youtube.com/@StevdzaSan)

---

*Generated April 2026. Verify resource links are current before starting each milestone.*