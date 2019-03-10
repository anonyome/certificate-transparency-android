# Certificate Transparency Android

This repository contains a modified version of [https://github.com/google/certificate-transparency-java](https://github.com/google/certificate-transparency-java). 

The following modifications were made to adapt the code so that it will work on Android.
*   Delete the classes that use Apache HTTP components. These conflict with the Android networking classes.
*   Replace uses of BouncyCastle with SpongyCastle which is the preferred BC implementation on Android.
*   Replace use of com.google-code.json-simple with Google's Gson, which contains newer bytecode which is compatible with Android.
*   Change the Maven component name from ctlog to ctlog-android.

For an example of how to use the code in this repository please examine [SslConnectionCheckingTest.java](src/test/java/org/certificatetransparency/ctlog/comm/SslConnectionCheckingTest.java)

Warwick Hunter 2019-03-10
