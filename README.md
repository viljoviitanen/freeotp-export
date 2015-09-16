# freeotp-export

FreeOTP qrcode exporter app in javascript

Backround: FreeOTP is a Google Authenticator compatible open source Android app, made by Red Hat. Available at https://play.google.com/store/apps/details?id=org.fedorahosted.freeotp .

Google authenticator does not allow backuping the secrets with adb, to backup one needs a rooted phone. FreeOTP however allows adb backup. The backup file obviously can be restored to any android phone, but for easy transfer to other phones, you can create qr codes with this app. The app does all processing locally, no data is sent anywhere. 

__Be sure to understand the security implications of backing up the secrets from the authenticator app, and writing them on your computer storage.__

# Instructions

Make an adb backup of FreeOTP, (details on how to do this are currenly left as an excercise for the reader. While you are doing the backup, consider the above warning!). Open the adb backup file (.ab) with this app. Read the displayed qrcodes with the authenticator app on your other phone.

The author has tested the app with current Google Chrome and Mozilla Firefox on Ubuntu 14.04 in September 2015, generated qrcodes have been succesfully imported in FreeOTP and Google Authenticator on Android and Microsoft Authenticator on Windows Phone 8. Other browsers probably do not work.

This app can be opened directly at https://rawgit.com/viljoviitanen/freeotp-export/master/export.html 

An example tokens.xml file from FreeOTP is included with this repository.

#Todo

Use android backup files without fiddling with command line tools. There are javascript zlib (deflate) and tar implementations with free licenses, so it should be relatively easy.

#Acknowledgements

Based on https://github.com/philipsharp/FreeOTPDecoder (Apache license)

Uses https://github.com/davidshimjs/qrcodejs (MIT license)

Uses https://github.com/nodeca/pako (MIT license)

Uses https://github.com/Qvazar/js-untar (GPLv3 license)

Content is served by https://rawgit.com/

# License

Apache License, Version 2.0
