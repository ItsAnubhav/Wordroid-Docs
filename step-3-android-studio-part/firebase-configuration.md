# Firebase Configuration

### Create a Firebase project and add you app automatically (Recommened) <a href="#create-a-firebase-project-and-add-you-app-automatically-recommened" id="create-a-firebase-project-and-add-you-app-automatically-recommened"></a>

#### Use the Firebase Assistant <a href="#use_the_firebase_assistant" id="use_the_firebase_assistant"></a>

To open the Firebase Assistant in Android Studio:

* Click **Tools > Firebase** to open the **Assistant** window.
* Click to expand one of the listed features (for example, Analytics), then click the provided tutorial link (for example, Log an Analytics event).
* Click the **Connect to Firebase** button to connect to Firebase and add the necessary code to your app.

### Create a Firebase project Manually (Ignore this if you already have one) <a href="#create-a-firebase-project-manually-ignore-this-if-you-already-have-one" id="create-a-firebase-project-manually-ignore-this-if-you-already-have-one"></a>

1. Create a Firebase project in the [Firebase console](https://console.firebase.google.com/), if you don't already have one. Click **Add project**. If you already have an existing Google project associated with your mobile app, select it from the **Project name** drop down menu. Otherwise, enter a project name to create a new project.
2. _Optional_: Edit your **Project ID**. Your project is given a unique ID automatically, and it's used in publicly visible Firebase features such as database URLs and your Firebase Hosting subdomain. You can change it now if you want to use a specific subdomain.
3. Follow the remaining setup steps and click **Create project** (or **Add Firebase** if you're using an existing project) to begin provisioning resources for your project. This typically takes a few minutes. When the process completes, you'll be taken to the project overview.

### Add your app to your Firebase Project <a href="#add-your-app-to-your-firebase-project" id="add-your-app-to-your-firebase-project"></a>

1. Click **Add Firebase to your Android app** and follow the setup steps. If you're importing an existing Google project, this may happen automatically and you can just [download the config file](http://support.google.com/firebase/answer/7015592).
2. When prompted, enter your app's package name. It's important to enter the package name your app is using; this can only be set when you add an app to your Firebase project.
3. During the process, you'll download a `google-services.json` file. You can [download this file](http://support.google.com/firebase/answer/7015592) again at any time. Replace the exisiting `google-services.json`file with the one you just downloaded.
4. After you add the initialization code, run your app to send verification to the Firebase console that you've successfully installed Firebase.
