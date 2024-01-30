Daily Notes : Day 97
APK Pentesting - Part 6 

Unintended Data Leakage: 
Often Developers leave debugging information publicly. So any application with READ_LOGS permission can access those logs and can gain sensitive information through that.

Copy/Paste Buffer Caching:
Android provides clipboard-based framework to provide copy-paste function in android applications. But this creates serious issue when some other application can access the clipboard which contain some sensitive data. Copy/Paste function should be disabled for sensitive part of the application. For example, disable copying credit card details.

Crash Logs: 
If an application crashes during runtime and it saves logs somewhere then those logs can be of help to an attacker especially in cases when android application cannot be reverse engineered. Then, avoid creating logs when applications crashes and if logs are sent over the network then ensure that they are sent over an SSL channel.

Analytics Data Sent To 3rd Parties: 
Most of the application uses other services in their application like Google Adsense but sometimes they leak some sensitive data or the data which is not required to sent to that service. This may happen because of the developer not implementing feature properly. You can look by intercepting the traffic of the application and see whether any sensitive data is sent to 3rd parties or not.