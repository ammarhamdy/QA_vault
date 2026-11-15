
## Step 1. List Available Android Virtual Devices (AVDs)
`emulator -list-avds`

## Step 2. Start an Emulator
`emulator -avd Pixel_9_Pro`

## Step 3. Install an APK
`adb install beauty.apk`
`adb install -r beauty.apk #re-install`

## Step 4. Launch the App Manually
`adb shell monkey -p com.codlop.daysbeauty 1`

## Step 5. Create a Kotlin Project
```
 ├── src
 │    ├── main
 │    └── test
 │          └── kotlin
 │               └── SmokeTest.kt
 │
 ├── build.gradle.kts
 └── settings.gradle.kts
```

```
│
├── pages/
│      LoginPage.kt
│      HomePage.kt
│
├── models/
│
├── utils/
│
├── base/
│      BaseTest.kt
│
├── tests/
│      LoginTest.kt
│      SmokeTest.kt
│
└── build.gradle.kts
```

## Step 6. Add Dependencies
```
plugins {
    kotlin("jvm") version "2.2.0"
}

repositories {
    mavenCentral()
}

dependencies {

    testImplementation("io.appium:java-client:10.0.0")

    testImplementation("org.seleniumhq.selenium:selenium-java:4.33.0")

    testImplementation("org.junit.jupiter:junit-jupiter:5.13.4")
}

tasks.test {
    useJUnitPlatform()
}
```

## Step 7. Start Appium
`appium`


# Notes

## Check installed packages:
`adb shell pm list packages`

## Gradle
```
./gradlew --version
./gradlew test
./gradlew build
./gradlew compileKotlin
./gradlew --refresh-dependencies
```
### Run the test
```angular2html
./gradlew test --tests SmokeTest
```

