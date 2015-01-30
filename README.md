# Building-LatinIME-with-Android-Studio

Still doesn't build so this is a work in progress

**1** Clone the [LatinIME](https://android.googlesource.com/platform/packages/inputmethods/LatinIME) repository

**2** Import LatinIME/java folder in Android Studio

**3** If on a Linux machine, remove all unsupported emoji characters from /app/src/main/res/values/strings-emoji-descriptions.xml using Replace (Ctrl + R) and matching the regex string '(?s)<!--.*?-->' and replacing that with ' '

**4** Add v4 support library using Maven

**5** Add libjni_latinime.so library to your project. To enable gesture typing, you'll want to get the libjni_latinimegoogle.so found in the Google Keyboard apk and also [here](http://www.theandroidsoul.com/download-new-apps-apks-android-5-0-lollipop-preview-images/)

**6** Add all missing classes from [here](https://github.com/VanirAOSP/packages_input_LatinIME/find/L5)

**7** Get missing InputMethodCommon package [here](https://android.googlesource.com/platform/frameworks/opt/inputmethodcommon/+/master/java/com/android/inputmethodcommon)
