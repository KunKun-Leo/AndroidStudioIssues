## Issue1
### Error
#### java.lang.RuntimeException: Duplicate class kotlin.collections.jdk8.CollectionsJDK8Kt found in modules kotlin-stdlib-1.8.20 (org.jetbrains.kotlin:kotlin-stdlib:1.8.20) and kotlin-stdlib-jdk8-1.6.21 (org.jetbrains.kotlin:kotlin-stdlib-jdk8:1.6.21)
### Solution
add <b>implementation(platform("org.jetbrains.kotlin:kotlin-bom:1.8.0"))</b> in build.gradle file

## Issue2
### Error 
#### Can't download by implementation in buid.gradle file
### Solution
set **setttings.gradle** as:
```pluginManagement {
    repositories {
        gradlePluginPortal()
        google()
        mavenCentral()
    }
}
dependencyResolutionManagement {
    repositoriesMode.set(RepositoriesMode.FAIL_ON_PROJECT_REPOS)
    repositories {
        google()
        mavenCentral()
    }
}

rootProject.name = "projectname"
include ':app'
```
