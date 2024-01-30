Daily Notes : day 99
APK Pentesting - Part 8 

Authorisation bypass:
When an Activity is exported you can invoke its screen from an external app. Therefore, if an activity with sensitive information is exported you could bypass the authentication mechanisms to access it.
Learn how to exploit exported activities with Drozer.
Link: https://book.hacktricks.xyz/mobile-pentesting/android-app-pentesting/drozer-tutorial#activities

You can also start an exported activity from adb:
* PackageName is com.example.demo
* Exported ActivityName is com.example.test.MainActivity

ADB:
adb shell am start -n com.example.demo/com.example.test.MainActivity

NOTE: MobSF will detect as malicious the use of singleTask/singleInstance as android:launchMode in an activity, but due to this, apparently this is only dangerous on old versions (API versions < 21).

Note that an authorisation bypass is not always a vulnerability, it would depend on how the bypass works and which information is exposed.

Sensitive information leakage: 
Activities can also return results. If you manage to find an exported and unprotected activity calling the setResult method and returning sensitive information, there is a sensitive information leakage.