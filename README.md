Glass-Notifications
===================
A Google Glass application that will clone notifications from an Android 4.3+ device to Google Glass.  

* This app will uses my [IntentTunnel](https://github.com/TheMasterBaron/Glass-IntentTunnel/) project for communication from the phone to Glass.  IntentTunnel is a Intent router that handles bluetooth communications for multiple applications using a single bluetooth connection.

In Android 4.3, they introduced the option to capure notifications.  This is how Glass-Notifications will be able to forward your notificaitons to Glass
Goto Settings->Security->Notification Access and enable Glass-Notifications.

![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/phone-notification-access.png?raw=true)

===============================================================================================
Here is a screen shot of my notifications bar pulled down on my phone:
![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/phone-notifications.png?raw=true)

Here is a screen shot of Glass-Notifications capturing my notifications and allowing me to pick which ones I want.  By default, notificaitons that are dismissable are enabled and ones that are not are disabled.  You can enable/disable them using this tool.  Also, when capturing the notifications, the larger versions of the notificaiton are used to show more information on Glass.

![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/phone-captured-notifications.png?raw=true)

===============================================================================================
Here is the notification telling me I have an auto awesome picture waiting for me.  This notification made a sound on my phone, so it also made a sound on Glass to let me know there is something waiting for me.  If I look up within 5 seconds, the notificaiton will be there for me to see.

GLASS SCREENSHOT:

![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/glass-autoawesome.png?raw=true)

===============================================================================================
The auto awesome notificaiton is dismisable on my phone.  So, I have the option to dismiss it from Glass.

GLASS SCREENSHOT:

![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/glass-autoawesome-dismiss.png?raw=true)

===============================================================================================
I have installed an app called Notificaiton Weather from the play store.  This app puts a permenant weather forcast im my notifications.  This is not dismisable so it's just a livecard that gives me the weather. BONUS!

GLASS SCREENSHOT:

![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/glass-weather.png?raw=true)

===============================================================================================
This is just an example of a simpler notification.

GLASS SCREENSHOT:

![Screenshot](https://github.com/TheMasterBaron/Glass-Notifications/blob/master/screenshots/glass-small.png?raw=true)




Install Instructions
===================
WORKS ON ANDROID 4.3+ ONLY

1. Download and install [IntentTunnel](https://github.com/TheMasterBaron/Glass-IntentTunnel/).  Check the readme on how to install IntentTunnel on both your phone and Glass.

2. Download the Glass-Notifications APK [here](https://github.com/TheMasterBaron/Glass-Notifications/releases/download/v0.0.3/Glass-Notifications-debug-unaligned-0.0.3.apk).  The same APK is for the phone and Glass

3. Intall the APK on Glass using this command:
<code>adb install -r Glass-Notifications-debug-unaligned.apk</code>

4. After installing the APK on Glass, start the Glass-Notifications service on Glass usng Glass Launcher, Launchy, or using this command adb:
<code>adb shell am start -n com.masterbaron.notifications/com.masterbaron.notifications.LaunchActivity</code>

5. Intall the APK on you Phone and run Glass-Notifications.  The first time you launch it, it should give you a button to press to enable Notification Access for Glass-Notificaitons.  After enabling notificaiton access, you can then select which notifications you would like to send to Glass.

If IntentTunnel is running you should start seeing notifications on Glass.

Change Log:
===========
[0.0.3](https://github.com/TheMasterBaron/Glass-Notifications/releases/download/v0.0.3/Glass-Notifications-debug-unaligned-0.0.3.apk): New GUI and option to remove action buttons (on by default)

0.0.2: Don't bypass service on broadcast

0.0.1: Initial Release
