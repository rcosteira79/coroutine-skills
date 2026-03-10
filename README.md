# Android Skills for Claude Code

Claude Code skills for Android and KMP development — covering architecture, data layer, networking, testing, debugging, Jetpack Compose, coroutines, flows, Gradle, and RxJava migration.

## Skills

### `android-dev`
Senior Android engineering knowledge and best practices for Android and KMP projects. Covers architecture, code quality, and platform-specific patterns.

### `android-tdd`
Test-driven development for Android/KMP — extends TDD with Android's three-tier test model, fake-first strategy, coroutine testing, and Compose UI testing.

### `android-ux`
Material Design 3 UX principles for Android — touch targets (48×48dp), 8dp spacing grid, navigation patterns (Bottom Bar, Rail, Drawer), safe area handling, accessibility, animation timing, and keyboard input types.

### `android-debugging`
Debugging Android and KMP issues — Logcat, ADB, ANR traces, R8 stack trace decoding, memory leaks, Gradle build failures, and Compose recomposition bugs.

### `compose`
Jetpack Compose expert guidance — state management (`@Composable`, `remember`, `mutableStateOf`, `derivedStateOf`, state hoisting), Modifier chains, lazy lists, navigation, animation, side effects, theming, accessibility, and performance optimization.

### `aosp-search`
Verify Android framework internals, find `@hide` APIs and internal constants, confirm underdocumented behavior, and trace how framework classes actually implement things.

### `kotlin-coroutines`
Dispatcher selection, scope management, structured concurrency, cancellation, exception handling, and Android/KMP async patterns. Includes the DispatcherProvider pattern for testable dispatcher injection.

### `kotlin-flows`
Flow type selection (`Flow`/`StateFlow`/`SharedFlow`), operator chains, callback bridging, lifecycle-safe collection, Channel migration, and UI state management.

### `rxjava-migration`
Triggered only when you explicitly ask to migrate. Assesses complexity, maps RxJava types and operators to coroutines equivalents, and provides interop patterns for incremental migration.

### `xml-to-compose-migration`
Migrate Android XML layouts to Jetpack Compose — layout mapping tables (RecyclerView → LazyColumn, LinearLayout → Column/Row, etc.), attribute mapping, state migration from LiveData/ViewBinding, and incremental adoption via `ComposeView`.

### `android-retrofit`
Retrofit setup for Android — service interface patterns (`@GET`, `@POST`, `@Path`, `@Query`, `@Body`), coroutines integration, OkHttp configuration, Hilt module, and error handling in the repository layer.

### `android-data-layer`
Data layer implementation — Repository pattern as single source of truth, Room DAOs with `Flow`, offline-first strategies (stale-while-revalidate, outbox pattern), and model mapping between DTO/entity/domain types.

### `coil-compose`
Image loading in Compose with Coil — `AsyncImage` vs `SubcomposeAsyncImage` vs `rememberAsyncImagePainter`, `ImageRequest` configuration, performance in lazy lists, and Hilt setup for a shared `ImageLoader`.

### `android-gradle-logic`
Scalable Gradle build logic — Convention Plugins, composite builds, shared `compileSdk`/`minSdk`/Compose configuration across modules, and clean per-module `build.gradle.kts` files.

### `gradle-build-performance`
Gradle build optimisation — Build Scans, configuration cache, build cache, kapt→KSP migration, parallel execution, lazy task configuration, and a recommended `gradle.properties` baseline.

## Installation

### Claude Code

Copy the skill directories into your Claude Code skills folder:

```bash
git clone https://github.com/rcosteira79/android-skills.git
cp -r android-skills/skills/* ~/.claude/skills/
```

Skills are invoked automatically based on context:

- Working on Android or KMP code → `android-dev` skill activates
- Writing or fixing tests → `android-tdd` skill activates
- Debugging Android issues → `android-debugging` skill activates
- Designing or reviewing Android UI → `android-ux` skill activates
- Working with Compose → `compose` skill activates
- Verifying framework internals → `aosp-search` skill activates
- Working with coroutines → `kotlin-coroutines` skill activates
- Working with Flow/StateFlow/SharedFlow → `kotlin-flows` skill activates
- Migrating from RxJava → ask Claude to migrate, `rxjava-migration` skill activates
- Migrating XML layouts to Compose → `xml-to-compose-migration` skill activates
- Setting up networking with Retrofit → `android-retrofit` skill activates
- Implementing the data/repository layer → `android-data-layer` skill activates
- Loading images with Coil → `coil-compose` skill activates
- Setting up Gradle build logic → `android-gradle-logic` skill activates
- Optimising build performance → `gradle-build-performance` skill activates

### Cursor, Windsurf, and other agentic editors

The skills are plain markdown files. Copy the content of whichever `SKILL.md` files are relevant into your editor's context mechanism:

- **Cursor** — add to `.cursor/rules/` as `.mdc` files
- **Windsurf** — add to `.windsurf/rules/` as `.md` files
- **Copilot** — add to `.github/copilot-instructions.md`
- **Other editors** — paste into your project's custom instructions or context file

Each skill is self-contained and can be used independently.

## Inspiration

These skills drew inspiration from:

- [awesome-android-agent-skills](https://github.com/new-silvermoon/awesome-android-agent-skills)
- [compose-skill](https://github.com/aldefy/compose-skill)
- [ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)

## License

MIT
