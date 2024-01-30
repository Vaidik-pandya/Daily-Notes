Daily Notes : Day 94 
APK Pentesting - Part 4 

Broken Cryptography: 
Poor Key Management Processes
Some developers save sensitive data in the local storage and encrypt it with a key hardcoded/predictable in the code. This shouldn't be done as some reversing could allow attackers to extract the confidential information.

Use of Insecure and/or Deprecated Algorithms
Developers shouldn't use deprecated algorithms to perform authorisation checks, store or send data. Some of these algorithms are: RC4, MD4, MD5, SHA1... If hashes are used to store passwords for example, hashes brute-force resistant should be used with salt.

Other checks
1. It's recommended to obfuscate the APK to difficult the reverse engineer labour to attackers.
2. If the app is sensitive (like bank apps), it should perform it's own checks to see if the mobile is rooted and act in consequence.
3. If the app is sensitive (like bank apps), it should check if an emulator is being used.
4. If the app is sensitive (like bank apps), it should check it's own integrity before executing it to check if it was modified.
5. Use APKiD to check which compiler/packer/obfuscator was used to build the APK