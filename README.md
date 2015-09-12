# gradle-bintray-mvn-push
Sample project for bintray push from gradle

Steps
-----

-   Signup on bintray  
-   Create repository and package
-   Obtain apikey from Edit profile and set it in `local.properties` of Project

```groovy
    bintray.apikey=API_KEY
    bintray.user=USER_ID
```

-   Add this `classpath` to your root project `build.gradle`'s buildscript dependencies

```groovy
    classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.3.1'
    classpath 'com.github.dcendents:android-maven-gradle-plugin:1.3'
```

-   Add `gradle-mvn-push.gradle` and `bintray.properties` files to your module
-   Configure `bintray.properties` file
-   Add this line to end of your module's `build.gradle`

```groovy
    apply from : 'gradle-mvn-push.gradle'
```

-   `gradlew binrayUpload`
