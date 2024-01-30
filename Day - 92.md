Daily Notes : Day 92
APK Pentesting - Part 3 
Tapjacking 

Information : Tapjacking is an attack where a malicious application is launched and positions itself on top of a victim application.

Detection : In order to detect apps vulnerable to this attacked you should search for exported activities in the android manifest (note that an activity with an intent-filter is automatically exported by default). Once you have found the exported activities, check if they require any permission. This is because the malicious application will need that permission also.

Exploitation : https://github.com/carlospolop/Tapjacking-ExportedActivity