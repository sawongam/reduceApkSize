# reduceApkSize
The 5 things to reduce your APK size:

- Replace `proguard-android.txt` with `proguard-android-optimize.txt`
- Make `minifyEnabled` `true`
- Add `shrinkResources` `true`
- Add `resConfigs`
- Reduce Images size

```
buildTypes {
    release {
        minifyEnabled true
        shrinkResources true
        resConfigs "en"
        proguardFiles getDefaultProguardFile('proguard-android-optimize.txt'), 'proguard-rules.pro'
    }
}
```
