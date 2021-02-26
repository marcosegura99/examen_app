# examen_app
aplicaciones moviles
{
  "project_info": {
    "project_number": "796989309170",
    "project_id": "examenes-ee590",
    "storage_bucket": "examenes-ee590.appspot.com"
  },
  "client": [
    {
      "client_info": {
        "mobilesdk_app_id": "1:796989309170:android:ae82f72d67c77a9e9e906b",
        "android_client_info": {
          "package_name": "com.example.examen"
        }
      },
      "oauth_client": [
        {
          "client_id": "796989309170-t9biam50r7irhskrqnqdgfemfqd892in.apps.googleusercontent.com",
          "client_type": 1,
          "android_info": {
            "package_name": "com.example.examen",
            "certificate_hash": "d48fc6632a74a7362f6c7f1a2bad147d1c55416b"
          }
        },
        {
          "client_id": "796989309170-e8j71hf3pudiid7i91g1nnrdga2jnae4.apps.googleusercontent.com",
          "client_type": 3
        }
      ],
      "api_key": [
        {
          "current_key": "AIzaSyAoPfMMFJnQh7ALI8AWERHa5T4J9P09s7o"
        }
      ],
      "services": {
        "appinvite_service": {
          "other_platform_oauth_client": [
            {
              "client_id": "796989309170-e8j71hf3pudiid7i91g1nnrdga2jnae4.apps.googleusercontent.com",
              "client_type": 3
            }
          ]
        }
      }
    }
  ],
  "configuration_version": "1"
}
// Top-level build file where you can add configuration options common to all sub-projects/modules.
buildscript {

    repositories {
        google()
        jcenter()
    }
    dependencies {
        classpath 'com.google.gms:google-services:4.3.5'
        classpath "com.android.tools.build:gradle:4.1.1"

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

allprojects {
    repositories {
        google()  // Google's Maven repository
        google()
        jcenter()
    }
}

task clean(type: Delete) {
    delete rootProject.buildDir
}
plugins {

    id 'com.android.application'
}

android {
    compileSdkVersion 30
    buildToolsVersion "30.0.3"

    defaultConfig {
        applicationId "com.example.examenappmoviles"
        minSdkVersion 16
        targetSdkVersion 30
        versionCode 1
        versionName "1.0"

        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
    }

    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
        }
    }
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}

dependencies {
    implementation platform('com.google.firebase:firebase-bom:26.5.0')


    implementation 'androidx.appcompat:appcompat:1.2.0'
    implementation 'com.google.android.material:material:1.3.0'
    implementation 'androidx.constraintlayout:constraintlayout:2.0.4'
    testImplementation 'junit:junit:4.+'
    androidTestImplementation 'androidx.test.ext:junit:1.1.2'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.3.0'
    implementation 'com.google.firebase:firebase-analytics'
}
apply plugin: 'com.google.gms.google-services'

apply plugin: 'com.android.application'
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.examenappmoviles">
    <uses-permission android:name="android.permission.INTERNET"
    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.ExamenappMoviles">
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>



