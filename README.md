
  plugins {
    id "com.android.application"
    id "kotlin-android"
}

android {
    compileSdkVersion setup.compileSdk
    buildToolsVersion setup.buildTools
    defaultConfig {
        applicationId "com.maltaisn.calcdialoglib.demo"
        minSdkVersion setup.minSdk
        targetSdkVersion setup.targetSdk
        versionCode 1
        versionName "1.0"
    }
    buildFeatures {
        viewBinding = true
    }
    sourceSets {
        main.java.srcDirs += "src/main/kotlin"
    }
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
    kotlinOptions {
        jvmTarget = "1.8"
    }
}

dependencies {
    implementation project(":lib")

    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk8:$kotlinVersion"

    implementation "androidx.core:core-ktx:$ktxVersion"
    implementation "androidx.appcompat:appcompat:$appCompatVersion"
    implementation "androidx.constraintlayout:constraintlayout:$constraintLayoutVersion"
    implementation "com.google.android.material:material:$materialVersion"
}
