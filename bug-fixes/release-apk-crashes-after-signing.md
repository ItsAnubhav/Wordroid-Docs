---
description: >-
  Debug APK works fine but APK crashes/stuck on splash screen when signed with
  release key
---

# Release APK Crashes after signing

The problem causes when you generate the release APK because Android Studio removed some classes that are not in use. Sometimes it deletes the file that is being used. This introduces the crash.&#x20;

To fix this bug we need to exclude the files we are using in the app. The excluded files are mentioned in the `proguard-rules.pro`

## Steps to fix this issue

1 :  Open the file **app > proguard-rules.pro**

The file would look something like this

{% code title="proguard-rules.pro" %}
```
# Add project specific ProGuard rules here.
# You can control the set of applied configuration files using the
# proguardFiles setting in build.gradle.
#
# For more details, see
#   http://developer.android.com/guide/developing/tools/proguard.html

# If your project uses WebView with JS, uncomment the following
# and specify the fully qualified class name to the JavaScript interface
# class:
#-keepclassmembers class fqcn.of.javascript.interface.for.webview {
#   public *;
#}

# Uncomment this to preserve the line number information for
# debugging stack traces.
#-keepattributes SourceFile,LineNumberTable

# If you keep the line number information, uncomment this to
# hide the original source file name.
#-renamesourcefileattribute SourceFile
-keep class com.itsanubhav.** { *; }
-keep class com.synnapps.carouselview.** { *; }
-keep class .R
-keep class **.R$* {
    <fields>;
}

```
{% endcode %}

2\. You need to replace the file contents with below file

{% code title="proguard-rules.pro" %}
```
# Add project specific ProGuard rules here.
# You can control the set of applied configuration files using the
# proguardFiles setting in build.gradle.
#
# For more details, see
#   http://developer.android.com/guide/developing/tools/proguard.html

# If your project uses WebView with JS, uncomment the following
# and specify the fully qualified class name to the JavaScript interface
# class:
#-keepclassmembers class fqcn.of.javascript.interface.for.webview {
#   public *;
#}

# Uncomment this to preserve the line number information for
# debugging stack traces.
#-keepattributes SourceFile,LineNumberTable

# If you keep the line number information, uncomment this to
# hide the original source file name.
#-renamesourcefileattribute SourceFile
-keep class com.itsanubhav.wordroid.** { *; }
-keep class com.itsanubhav.libdroid.** { *; }
-keep class com.synnapps.carouselview.** { *; }
-keep class .R
-keep class **.R$* {
    <fields>;
}

```
{% endcode %}

3 : Replace the package name (com.itsanubhav.wordroid) with your package name (com.example.app) (**line no 22**).

{% hint style="success" %}
If you have also renamed the **libdroid** package then you need to replace that as well (**line no 23**).
{% endhint %}

### More Info

Notification issues were fixed and published on codecanyon on **9 February 2020**. If you are facing the notification not working issue then you need to update the plugin. _**You can optionally update the app but it is not mandatory.**_









