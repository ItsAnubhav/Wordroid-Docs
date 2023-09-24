# Configure Login

Version 4 supports WordPress login using JSON Web Token. You need to install the [https://wordpress.org/plugins/jwt-authentication-for-wp-rest-api/](https://wordpress.org/plugins/jwt-authentication-for-wp-rest-api/) plugin to make the WordPress authentication work.&#x20;

However you can skip that if you want and go for Google/Phone login (via Firebase). Google and Phone login requires the SHA-1 key to be added to your firebase console.&#x20;

Setup various login options in the app.

Make sure your app is [configured with Firebase](https://wordroid.gitbook.io/wordroid-docs/firebase-configuration) properly. Also make sure you have added the debug SHA-1 key for debugging and release SHA-1 key for release.

### Generate Debug SHA-1 Key <a href="#generate-debug-sha-1-key" id="generate-debug-sha-1-key"></a>

1. Select Gradle in android studio from right panel
2. Select Your App
3. In tasks -> android-> `signingReport`
4. &#x20;Double click `signingReport`
5.  You will find the SHA-1 fingerprint in the "**Gradle Console**"

    Copy this SHA-1 key and paste it in firebase console (**Project Structure** page).

### Enable SignIn Option in Firebase Console <a href="#enable-signin-option-in-firebase-console" id="enable-signin-option-in-firebase-console"></a>

1. Click on **Authentication**
2. Switch to **Sign-in method** tab.
3. Enable the options that you want to add to the app.

![](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-L9mbIjYBYPentmi3p5G%2F-LTVy-edGyMaJd2bT1lh%2F-LTVy9d5lmwrRVH0C0bI%2Fauthentication.PNG?alt=media\&token=67b156a9-aaa2-49f5-a9ca-4b00fc088e3b)

### Add code to the app <a href="#add-code-to-the-app" id="add-code-to-the-app"></a>

1. Go to AuthFragment.java
2. Find this code

{% code title="AuthFragment.java" %}
```java
private void signIn(){
        startActivityForResult(
                AuthUI.getInstance()
                        .createSignInIntentBuilder()
                        .setAvailableProviders(Arrays.asList(
                                new AuthUI.IdpConfig.GoogleBuilder().build(), //Google Login
                                new AuthUI.IdpConfig.PhoneBuilder().build())  //Phone Login
                        )
                        .build(),
                RC_SIGN_IN);
    }
```
{% endcode %}

This will add Email, Phone and Google sign in option to the app. You can remove / add / rearrange them to adjust the option.

You can add your siginin provides as mentioned [here](https://github.com/firebase/FirebaseUI-Android/blob/master/auth/README.md#adding-providers)

Note that if you will generate the signed APK for play store, the login will not work until you paste in the Google App Signing keys to the firebase console.

### Facebook Login​ <a href="#facebook-login" id="facebook-login"></a>

1. On the [Facebook for Developers](https://developers.facebook.com/) site, get the **App ID** and an **App Secret** for your app.
2. In the [Firebase console](https://console.firebase.google.com/), open the **Auth** section.
3. On the **Sign in method** tab, enable the **Facebook** sign-in method and specify the **App ID** and **App Secret** you got from Facebook.
4. Then, make sure your **OAuth redirect URI** (e.g. `my-app-12345.firebaseapp.com/__/auth/handler`) is listed as one of your **OAuth redirect URIs** in your Facebook app's settings page on the [Facebook for Developers](https://developers.facebook.com/) site in the **Product Settings > Facebook Login** config.

You also need to generate a separate Key Hash in order to use the Facebook login using the openssl. You'll find more information about this on Facebook login Quick-start page on Facebook for developers site.
