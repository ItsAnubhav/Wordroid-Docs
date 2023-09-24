# Build & Release for Android

To release the android app you need to sign the app with your own key. If you don't have a key file, [generate it using the android studio](https://developer.android.com/studio/publish/app-signing#generate-key).&#x20;

Go to the **android > key.properties** file and change the YOUR\_KEYSTORE\_PASSWORD with your own keystore password**,** YOUR\_KEY\_PASSWORD with your key password and YOUR\_KEY\_NAME with you key alias.

Also, replace the key file (.jks) **android > app > cert > key.jks** with your own key file. Make sure you rename the key file as key.jks

```
storePassword=YOUR_KEYSTORE_PASSWORD
keyPassword=YOUR_KEY_PASSWORD
keyAlias=YOUR_KEY_NAME
storeFile=cert/key.jks
```

After all that configured, fun the command&#x20;

```
flutter build apk
```

to generate the signed apk that can be uploaded into the playstore.
