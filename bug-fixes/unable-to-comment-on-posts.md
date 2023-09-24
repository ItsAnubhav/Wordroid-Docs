---
description: >-
  This page will help you fix the Indefinite comment sending animation when the
  user is not logged in via WordPress in the app.
---

# Unable to comment on posts

This problem arises because WordPress does not allows the unauthenticated users to comment by default. So we need to enable it by adding a few lines of code into the WordPress plugin.&#x20;

{% hint style="info" %}
If you are using the plugin updated after 15 June 20, then you can skip this article.&#x20;
{% endhint %}

### Solution

1. Go to your WordPress Dashboard
2. Clink on Plugins > Plugin Editor&#x20;
3. Now from the **Select plugin to edit :** dropdown menu, choose **WorDroid 4** and click **Select**
4. Now click on **home\_api.php,** you will see some code like this

```
<?php
add_action( 'rest_api_init', 'add_homepage_route');
```

&#x20; 5\. You need to replace above code with this code

```
<?php
add_action( 'rest_api_init', 'add_homepage_route');
add_filter( 'rest_allow_anonymous_comments', '__return_true' );
```

That's all. Now you'll be able to post comments from the app. **You don't need to regenerate the apk from android studio.**
