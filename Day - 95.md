Daily Notes : Day 95 
APK Pentesting - Part 5

Superpacked Applications:
talks about the possibility of creating an app that decompress these kind of apps... and a faster way which involves to execute the application and gather the decompressed files from the filesystem.

Automated Static Code Analysis z; 
The tool mariana-trench is capable of finding vulnerabilities by scanning the code of the application. This tool contains a series of known sources (that indicates to the tool the places where the input is controlled by the user), sinks (which indicates to the tool dangerous places where malicious user input could cause damages) and rules. These rules indicates the combination of sources-sinks that indicates a vulnerability.
With this knowledge, mariana-trench will review the code and find possible vulnerabilities on it.

Secrets leaked:
An application may contain secrets (API keys, passwords, hidden urls, subdomains...) inside of it that you might be able to discover