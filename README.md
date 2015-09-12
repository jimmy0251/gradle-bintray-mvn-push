# gradle-bintray-mvn-push
Sample project for bintray push from gradle

Steps
-----

1. Signup on bintray
2. Create repository and package
3. Obtain apikey from Edit profile and set it in `local.properties` of Project

```groovy
    bintray.apikey=API_KEY
    bintray.user=USER_ID
```

4. Add this `classpath` to your root project `build.gradle`'s buildscript dependencies

```groovy
    classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.3.1'
    classpath 'com.github.dcendents:android-maven-gradle-plugin:1.3'
```

5. Add gradle-mvn-push.gradle and bintray.properties files to your module
6. Configure bintray.properties file (Add remaining info)
7. Add this line to end of your module's build.gradle

```groovy
    apply from : 'gradle-mvn-push.gradle'
```

8. `gradlew binrayUpload`
