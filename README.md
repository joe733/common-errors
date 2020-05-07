# Solutions to common errors for Flutter Devs
Potential errors while working with Flutter and their solutions.

[//]: # (Hey there! We appriciate your effort to contribute.)
[//]: # (1. Please append your contribution\(s\) alphabetically and re-number them if required)
[//]: # (2. Follow the pattern already seen before you)


## 01. Gradle Dependency Error
<details>
  <summary><b>ScreenShots</b></summary>
  <img src=./gradle-dependency-error.png>
</details>
<details>
  <summary><b>Logs</b></summary>
</details>

### Solution 01<br>
*by [@Adheela](https://github.com/adheela)*<br>
**By changing the class path gradle version 1.0.0 build gradle in Android**<br>
By changing the gradle version (which is shown in error (screenshot) as required) in the distribution URL in `gradle-wrapper.properties` (`in project` → `app` → `gradle` → `wrapper` → `gradle-wrapper.properties`)

## 02. Syntax highlighting suddenly missing
<details>
  <summary><b>ScreenShots</b></summary>
  <img src=./syntax-highlighting-suddenly-missing.png>
</details>
<details>
  <summary><b>Logs</b></summary>
</details>

### Solution 02<br>
*by [@joe733](https://github.com/joe733)*<br>
- Check if you have `dart` plugin installed from VSCodium / VSCode marketpace.
- If yes simply close and reopen the file you're working on.
- Try to remove all the errors in your code.
