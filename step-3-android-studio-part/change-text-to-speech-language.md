# Change Text-to-speech language

{% hint style="info" %}
Make sure the voice pack of the language is installed in the phone before you change the TTS language.
{% endhint %}

By default the TTS's language is determined by the phone's language. If the language of the phone is English then the TTS language will also be the same.&#x20;

You can change this by going into the **PostFragment.java**&#x20;

```java
if (i == TextToSpeech.SUCCESS) {
    int result = tts.setLanguage(Locale.getDefault());

    if (result == TextToSpeech.LANG_MISSING_DATA
            || result == TextToSpeech.LANG_NOT_SUPPORTED) {
        showSnackbar(getResources().getString(R.string.text_to_speak_language_not_supported));
    }
} else {
    Log.e("TTS", "Initilization Failed!");
}
```

Change the ** Locale.getDefault()** with new Locale("fr","CA"). fr is the language and CA is the country. Check the list of available locale [https://www.oracle.com/technetwork/java/javase/java8locales-2095355.html](https://www.oracle.com/technetwork/java/javase/java8locales-2095355.html)

```
if (i == TextToSpeech.SUCCESS) {
    int result = tts.setLanguage(new Locale("fr","CA"));

    if (result == TextToSpeech.LANG_MISSING_DATA
            || result == TextToSpeech.LANG_NOT_SUPPORTED) {
        showSnackbar(getResources().getString(R.string.text_to_speak_language_not_supported));
    }
} else {
    Log.e("TTS", "Initilization Failed!");
}
```

 
