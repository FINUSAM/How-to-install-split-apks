In this video, I will guide you on how to merge split APK files into a bundle APK file. You will learn the following: 

1. How to export split APK files to a host machine  
2. How to merge these files 
3. How to sign a newly merged APK (a bundle file) file 
4. How to install and test on Android Emulator

Link To Download APKEditor
https://github.com/REAndroid/APKEditor/rel...

Commands:
adb shell
pm packages list
pm path
apk pull
java -jar APKEditor-1.2.9.jar m -i "path to the split apk files folder"

keytool -genkey -v -keystore custom.keystore -alias mykeyaliasname -keyalg RSA -keysize 2048 -validity 10000
apksigner sign --ks-key-alias mykeyaliasname --ks custom.keystore "merge APK file name"
apksigner verify "merge APK file name"