# Generating APK / Signed APK

To test your app, you can plug-in you android device to your computer via USB and run the app directly on it. Or you can generate an APK and install it manually to test it.

## Generating Debug APK (Usually for testing)

1. Open your project in Android Studio.
2. Go to **Build > Build Bundle(s)/APK(s) > Build APK.**

It will start the APK build process. Once its completed, a popup message will be shown (bottom right corner of the android studio) with two buttons on it. Click on **Locate** and it will show the APK in the  File Explorer (Windows) / Finder(Mac).

{% hint style="info" %}
The APK will be generated into the **app > build > outputs > apk > debug** you will see an apk file named **app-debug.apk**
{% endhint %}

## Generating Signed APK (For PlayStore)

Before Generating Signed APK make sure you change the app's **Version Code** and **Version Name (**This is visible to users on play store**).**&#x20;

1. Open your project in Android Studio.
2. Go to **Build > Generate Signed Bundle / APK**&#x20;

![](<../.gitbook/assets/Screenshot 2020-01-28 at 3.09.51 PM.png>)

&#x20;  3\. Choose APK (You can also generate the Android App Bundle. Process is almost same) and click Next.

![](<../.gitbook/assets/Screenshot 2020-01-28 at 3.12.00 PM.png>)

&#x20;   4\. You will this screen. You might see the empty form here. If you have an existing key file then click on **Choose existing...** and choose the existing key file (This is mandatory if you want to update your app on play store). If you don't have any key then click on **Create new...** and fill in the form that appear next. It will generate a key file that you will be using to sign  your app in order to update the app on play store. Otherwise you will loose all your existing user.&#x20;

Fill in the **Key Store password, Key alias and Key password** and click **Next**

![](<../.gitbook/assets/Screenshot 2020-01-28 at 3.18.28 PM.png>)

&#x20;   5\. Click on the **release** and make sure you check both the **V1 (Jar Signature)** and **V2 (Full APK Signature)** and click on **Finish.** Your APK will be generated and a confirmation PopUp message will be shown. You can upload that APK to playstore.
