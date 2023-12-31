# Add Site URL and Other Configuration

You need to add your Site URL, RTL Setting, YouTube API Key, Chanel ID etc.

Go to **com > itsanubhav > wordroid4 > Config.java**

### **Change SITE URL**

{% code title="Config.java" %}
```java
public static final String SITE_URL = "http://dev.itsanubhav.com/";
```
{% endcode %}

Change this to your site url 

Also make sure you put your URL in the **AndroidManifest.xml** file so that you app can deal with the deeplinks.

{% code title="AndroidManifest.xml" %}
```markup
<data
    android:host="dev.itsanubhav.com"
    android:scheme="https" />
```
{% endcode %}

 

### YouTube Configuration

{% code title="Config.java" %}
```java
public static final String chanelID = "UCWU5xE86VniV8eZ6mKce-Tw";

public static final String YT_API_KEY = "AIzaSyBtENkElp2xxxxxxxoYErJCGlMY8XPxxxxx";

public static final String YT_LATEST_CHANEL_ID = "UUNhT2txZHDfeIS0g7ZK7uRg";
```
{% endcode %}

 [Create your own API key](https://www.slickremix.com/docs/get-api-key-for-youtube/) and replace the value of **YT\_API\_KEY**.

Find your YouTube Chanel ID [here](https://commentpicker.com/youtube-channel-id.php) and paste it in the value of **chanelID**

**YT\_LATEST\_CHANEL\_ID** is the playlist id of your latest videos channel.

### OneSignal ID

You need to put your OneSingal App ID in the **build.gradle (Module: app)** file.



{% code title="build.gradle" %}
```
manifestPlaceholders = [
        onesignal_app_id               : '82fa91c3-9c88-4c3f-9fc5-dc88a0149038',
        // Project number pulled from dashboard, local value is ignored.
        onesignal_google_project_number: 'REMOTE'
]
```
{% endcode %}

###  Force RTL

You can force the app to support the RTL (Right to left). Just go to the **Config.java** and change the **FORCE\_RTL = false** to **FORCE\_RTL = true**

{% code title="Config.java" %}
```java
public static final boolean FORCE_RTL = false;
```
{% endcode %}

 
