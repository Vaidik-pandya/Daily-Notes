Daily Notes : Day 91 
APK Pentesting - Part 2 Static analysis

1. Content Providers: If an exported provider is being exposed, you could be able to access/modify interesting information. 

2. Check for FileProviders configurations inside the attribute android:name="http://android.support.FILE_PROVIDER_PATHS"

3. Exposed Services: Depending on what the service is doing internally vulnerabilities could be exploited

4. URL scheme: Read the code of the activity managing the schema and look for vulnerabilities managing the input of the user.

5. minSdkVersion, targetSDKVersion, maxSdkVersion: They indicate the versions of Android the app will run on. It's important to keep them in mind because from a security perspective, supporting old version will allow known vulnerable versions of android to run it.