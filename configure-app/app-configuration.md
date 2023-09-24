# App Configuration

### Basic Configuration

This will let you change the website URL, RTL Configuration, YouTube & OneSignal, and many more. Most of the app configurations are placed in the **lib > config > config.dart**

When you open the Config.dart file, you will see these lines of code.

{% code title="Config.dart" %}
```dart
class Config {
  static const String SITE_URL = "https://dev.itsanubhav.com";
  // receiveTimeout
  static const int receiveTimeout = 5000;

  static const bool forceRTL = false;

  static const String CHANNEL_ID = "UCJbPGzawDH1njbqV-D5HqKw";

  static const String YT_API_KEY = "AIzaSyAyAlVxB4InSmw7MAz2_n7b8RzKRPHDhOg";

  // connectTimeout
  static const int connectionTimeout = 3000;

  //OneSignal Notification App ID
  static const String ONESIGNAL_APP_ID = "f2d5fe59-afcc-4044-b4aa-e4f47c580259";

  static String admobAppId = "ca-app-pub-2424373783985998~1521649242";
  static String admobBannerAdUnit = "ca-app-pub-3940256099942544/6300978111";
  static String admobInterstitialAdUnit =
      "ca-app-pub-3940256099942544/1033173712";
  static String admobNativeAdUnit = "ca-app-pub-3940256099942544/2247696110";

  static final sliderArrayList = [
    Slider(
        sliderImageUrl: 'assets/images/slider_1.png',
        sliderHeading: "Awesome Design",
        sliderSubHeading: "Clean design that focus on what matters the most"),
    Slider(
        sliderImageUrl: 'assets/images/slider_2.png',
        sliderHeading: "Page 2",
        sliderSubHeading: "Page 2 description"),
    Slider(
        sliderImageUrl: 'assets/images/slider_3.png',
        sliderHeading: "Page 3",
        sliderSubHeading: "Page 3 description"),
  ];
}
```
{% endcode %}

Change these to your own configuration.

### Translation

Go to **lib > i18n.dart** and change mentioned below to your own texts.&#x20;

**Note that the 'en\_US' is the language code**

```dart
class Messages extends Translations {
  @override
  Map<String, Map<String, String>> get keys => {
        'en_US': {
          'see_more': 'See More',
          'change_theme': 'Change Theme',
          'theme_mode': 'Theme Mode',
          'light': 'Light',
          'dark': 'Dark',
          'follow_system': 'Follow System',
          'change_language': 'Change Language',
          'privacy_policy': 'Privacy Policy',
          'about_us': 'About Us',
  ....
```

To change the list of supported languages, go to **lib > config > constants.dart** and edit the following lines

```dart
  static List<String> languageNames = ["English", "हिन्दी", "عربى"];

  static List<String> languageCodes = ["en", "hi", "ar"];
  static List<String> countryCodes = ["US", "IN", "SA"];

```

{% hint style="danger" %}
Keep the name, language codes, and country-code in the same order.
{% endhint %}
