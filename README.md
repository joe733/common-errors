# Common Errors
Common errors in working with Flutter

## Gradle Dependencies

![Gradle Dependency Error](./gradle-dependency-error.png)

### Solution

Contributed by [@Adheela](https://github.com/adheela)

#### By changing the class path gradle version 1.0.0 build gradle in Android

By changing the gradle version(which is shown in error as required) in the distributionURL in gradle-wrapper.properties(in project->app->gradle->wrapper->gradle-wrapper.properties)

