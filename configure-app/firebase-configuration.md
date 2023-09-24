# Firebase Configuration

### Add your app to your Firebase Project (Android) <a href="#add-your-app-to-your-firebase-project" id="add-your-app-to-your-firebase-project"></a>

1. Click **Add Firebase to your Android app** and follow the setup steps. If you're importing an existing Google project, this may happen automatically and you can just [download the config file](http://support.google.com/firebase/answer/7015592).
2. When prompted, enter your app's package name. It's important to enter the package name your app is using; this can only be set when you add an app to your Firebase project.
3. During the process, you'll download a `google-services.json` file. You can [download this file](http://support.google.com/firebase/answer/7015592) again at any time. Replace the exisiting`google-services.json`file  located in the **android > app** with the one you just downloaded.
4. After you add the initialization code, run your app to send verification to the Firebase console that you've successfully installed Firebase.

### Add your app to your Firebase Project (iOS) <a href="#add-your-app-to-your-firebase-project" id="add-your-app-to-your-firebase-project"></a>

1. Go to the [Firebase console](https://console.firebase.google.com/).
2.  In the center of the project overview page, click the **iOS** icon to launch the setup workflow.

    If you've already added an app to your Firebase project, click **Add app** to display the platform options.
3. Enter your app's bundle ID in the **iOS bundle ID** field.
4. _(Optional)_ Enter other app information: **App nickname** and **App Store ID**.
5. Click **Register app**.
6. Click **Download GoogleService-Info.plist** to obtain your Firebase iOS config file (`GoogleService-Info.plist`).
7. Move your config file into the **ios >** **Runner** folder of your project. If prompted, select to add the config file to all targets.

