Daily Notes : Day 90 
APK Pentesting - Part 1 Static analysis

1.  check if the application is debuggeable. A production APK shouldn't be (or others will be able to connect to it). You can check if an application is debbugeable looking in the manifest for the attribute debuggable="true" inside the tag <application Example: <application theme="@2131296387" debuggable="true"

2. ackup: The android:allowBackup attribute defines whether application data can be backed up and restored by a user who has enabled usb debugging. If backup flag is set to true, it allows an attacker to take the backup of the application data via adb even if the device is not rooted. Therefore applications that handle and store sensitive information such as card details, passwords etc. should have this setting explicitly set to false because by default it is set to true to prevent such risks.
<application android:allowBackup="false"

3. NetworkSecurity: The application network security can be overwritten the defaults values with android:networkSecurityConfig="@xml/network_security_config". A file with that name may be put in res/xml. This file will configure important security settings like certificate pins or if it allows HTTP traffic. You can read here more information about all the things that can be configure, but check this example about how to configure HTTP traffic for some domains:
<domain-config cleartextTrafficPermitted="true"> <domain includeSubdomains="true">http://formation-software.co.uk </domain></domain-config>

4. Exported activities: Check for exported activities inside the manifest as this could be dangerous.