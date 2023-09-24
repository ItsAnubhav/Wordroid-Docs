# Change Package Name

## Changing Package Name

This page will help you to change the package name from com.itsanubhav.wordroid4 to whatever you want.

​

For example, if you want to change `com.example.app` to `com.awesome.game`, then:

1. In your _**Project pane**_, click on the little gear icon ( ![Gears icon](https://i.stack.imgur.com/lkezT.png) )
2. Uncheck / De-select the `Compact Empty Middle Packages` option

![Compact Empty Middle Packages](https://i.imgur.com/3j5pzNa.png)

1. Your package directory will now be broken up in individual directories
2. Individually select each directory you want to rename, and:
   * Right-click it
   * Select `Refactor`
   * Click on `Rename`
   * In the Pop-up dialog, click on `Rename Package` instead of Rename Directory
   * Enter the new name and hit **Refactor**
   * Click **Do Refactor** in the bottom
   * Allow a minute to let Android Studio update all changes
   * _Note: When renaming_ _`com`_ _in Android Studio, it might give a warning. In such case, select_ **Rename All**

![](https://i.imgur.com/PW9oZll.png)

1. Now open your _**Gradle Build File**_ (`build.gradle` - Usually `app` ). Update the `applicationId` to your new Package Name and Sync Gradle, if it hasn't already been updated automatically:

![](https://i.imgur.com/hMx08b7.png)

1. You may need to change the `package=` attribute in your manifest.
2. Clean and Rebuild.
3. _**Done!**_

{% hint style="info" %}
You might see an error after changing the package name because of the mismatched google-services.json. It will be fixed when you replace the existing google-services.json file with your own. It is inside the **app** folder.
{% endhint %}

[\
](https://wordroid.gitbook.io/wordroid-docs/changing-default-homepage)
