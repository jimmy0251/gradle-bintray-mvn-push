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

-   Add `bintray.properties` files to your library module
-   Configure `bintray.properties`
-   Add this line to END of your library module's `build.gradle`

```groovy
apply from : 'https://raw.githubusercontent.com/jimmy0251/gradle-bintray-mvn-push/master/gradle-mvn-push.gradle'
```

-   Run `gradlew bintrayUpload`


Credits
=======
[Canopas Software LLP](https://canopas.com)
