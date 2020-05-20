# Solutions to common errors for Flutter Devs
Potential errors while working with Flutter and their solutions.

[//]: # (Hey there! We appriciate your effort to contribute.)
[//]: # (1. Please append your contribution\(s\) alphabetically and re-number them if required)
[//]: # (2. Follow the pattern already seen before you)

## 01. A dependency may have only one source
<details>
  <summary><b>ScreenShots</b></summary>
  <img src=./a-dependency-may-have-only-one-source.png>
</details>
<details>
  <summary><b>Logs</b></summary>
<pre>Running flutter pub get` in demo app
sdk: flutter
shared_prefrences: 0.5.x+y <2.0.0
.
.
.
pub get failed (65) exit code 65.</pre>
</details>

### Solution 01<br>
*by [@joe733](https://github.com/joe733)*<br>
- If you are using `smoother ecosystem migration` then re-check the version(s) of the plugin.
- Replace `x`'s and `y`'s with recomended version numbers (for example as of 10 May 2020 the version(s) of [shared preferences](https://pub.dev/packages/shared_preferences) must be like `'>=0.5.7+1' <2.0.0`).
- Check if your intendation is correct (in the screenshot the `shared_preferences` dependency must be aligned to `flutter` i.e. not within the flutter block).
e.g.
```yaml
dependencies:
  flutter:
    sdk: flutter
  shared_prefrences: '>=0.5.7+1 <2.0.0' # note the intendation
```

---

## 02. Gradle Dependency Error
<details>
  <summary><b>ScreenShots</b></summary>
  <img src=./gradle-dependency-error.png>
</details>
<details>
  <summary><b>Logs</b></summary>
</details>

### Solution 02<br>
*by [@Adheela](https://github.com/adheela)*<br>
**Try changing the class path gradle version 1.0.0 build gradle in Android**<br>
By changing the gradle version (which is shown in the screenshot as required) in the distribution URL in `gradle-wrapper.properties` (`in project` → `app` → `gradle` → `wrapper` → `gradle-wrapper.properties`)

---

## 03. No rule to make target

<details>
  <summary><b>ScreenShots</b></summary>
</details>

<details>
  <summary><b>Logs</b></summary>

```make
Launching lib/main.dart on Linux in debug mode...
Makefile:117: warning: overriding recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:109: warning: ignoring old recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:117: warning: overriding recipe for target 'weekly_challenge/week_2'
Makefile:109: warning: ignoring old recipe for target 'weekly_challenge/week_2'
Makefile:117: warning: overriding recipe for target '-'
Makefile:109: warning: ignoring old recipe for target '-'
Makefile:116: *** mixed implicit and normal rules: deprecated syntax
Makefile:121: warning: overriding recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:117: warning: ignoring old recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:121: warning: overriding recipe for target 'weekly_challenge/week_2'
Makefile:117: warning: ignoring old recipe for target 'weekly_challenge/week_2'
Makefile:121: warning: overriding recipe for target '-'
Makefile:117: warning: ignoring old recipe for target '-'
Makefile:125: warning: overriding recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:121: warning: ignoring old recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:125: warning: overriding recipe for target 'weekly_challenge/week_2'
Makefile:121: warning: ignoring old recipe for target 'weekly_challenge/week_2'
Makefile:125: warning: overriding recipe for target '-'
Makefile:121: warning: ignoring old recipe for target '-'
Makefile:131: warning: overriding recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:125: warning: ignoring old recipe for target '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'
Makefile:131: warning: overriding recipe for target 'weekly_challenge/week_2'
Makefile:125: warning: ignoring old recipe for target 'weekly_challenge/week_2'
Makefile:131: warning: overriding recipe for target '-'
Makefile:125: warning: ignoring old recipe for target '-'
Makefile:130: *** mixed implicit and normal rules: deprecated syntax
make: *** No rule to make target '%.cc', needed by '/home/joe/Documents/Workspace/GitHub/Flutter/LearnFlutter/flutter_kerala'. Stop.
Exception: Build process failed
Exited (sigterm)

```

</details>

### Solution 03<br>
*by [@joe733](https://github.com/joe733)*<br>

<p align='center'> Happens while building on Linux (Ubuntu based) <br> Solution Status: NAY </p>

---

## 04. Syntax highlight is suddenly missing
<details>
  <summary><b>ScreenShots</b></summary>
  <img src=./syntax-highlighting-suddenly-missing.png>
</details>
<details>
  <summary><b>Logs</b></summary>
</details>

### Solution 04<br>
*by [@joe733](https://github.com/joe733)*<br>
- Check if you have `dart` plugin installed from VSCodium / VSCode [marketpace](https://marketplace.visualstudio.com/search?term=dart&target=VSCode&category=All%20categories&sortBy=Installs).
- If yes simply close and reopen the file you're working on.
- Try to remove all the errors in your code.
