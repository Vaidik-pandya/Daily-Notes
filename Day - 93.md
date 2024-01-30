Daily Notes : Day 93 
APK Pentesting - Part 3 
Broken TLS

Accept All Certificates: 
For some reason sometimes developers accept all the certificates even if for example the hostname does not match with lines of code like the following one:

SSLSocketFactory sf = new cc(trustStore);
sf.setHostnameVerifier(SSLSocketFactory.ALLOW_ALL_HOSTNAME_VERIFIER);

A good way to test this is to try to capture the traffic using some proxy like Burp without authorising Burp CA inside the device. Also, you can generate with Burp a certificate for a different hostname and use it.

Certificate Pinning: 
Another reason why developers might resort to custom TLS configurations actually stems from the opposite desire. Malicious actors could add an attacker-controlled certificate authority to the default trust store, which can then be used to issue forged certificates for any server.