-> Code Improvement Document 


Project Package structure

Main Package 
```
                                  - UI
                                    - Base
                                    - screen   
                                        - Activity
                                        - Fragment
                                  - Adapter 
                                  - CustomView
                                        - AppTextView
                                        - AppImageView
                                        - AppEditText
                                        - App Otherview
                                  - Util
                                    - HelperClass
                                    - NetworkUtil
                                    - DataTimeUtil
                                    - StringUtil
                                  - Constant
                                  - Network
                                  - Dagger
                                  - Database
                                  - Model Class 
```


#### 1) MVVM Code Implementation

Advantage

- View : All UI related Operation 
= Data model : All network call and database related code
- Model : Data structure
- View Model : Data Provider

#### 2) Retrofit 2

- For Network call

#### 3) Data Binding 

- For Component Operation
- Support both orientation portrait and landscape 

#### 4) Always Use Library up-to-date

#### 5) Require to use constraint layout in layout file (Low priority)  

#### 6) All String should be inside string.xml

#### 7) My suggestion is convert all application UI to one component (Style Base)

#### 8) Dagger for dependence injection

#### 9) Remove unused code from class

#### 10) Always use javaDoc for every class, and component of class. Example like variables,Methods... etc

#### 11) Must follow camelcase in variable and method name

#### 12) Remove commented code while create pull request

#### 13) All constant inside constant package

#### 14) All keys and sensitive data in project gradle files

#### 15) Require to create one method to show alert 

#### 16) Intent Create plugin to change screen
- https://github.com/yizems/ActivityIntentCreater

#### 17) Always type will use number like 
```
1=user
2=admin
3=team
etc in login screen
```
#### 18) Always use short keys name in API for fast data transfer

#### 19) Command API structure for all apis

#### 20) Any time force update user using response code 

#### 21) Always define string inside resource string.xml

#### 22) Always define color inside resource color.xml


#### 23) #BaseActivity,#BaseFragement,#BaseDialog,#BaseDialogFragment

- BaseActivity extend by AppCompatActivity
- Data-Binding work do inside baseactivity
- show hide progress dialog define in base activity

#### 24) #Simplify Android M system permissions (https://github.com/googlesamples/easypermissions)
- Easy ways handle runtime permission. Example created by google

#### 25) #User's location (https://github.com/mumayank/AirLocation)
- Get user  precise current location via a callback
 
#### 26) #Notifications (https://github.com/googlesamples/android-Notifications)
- In new firebase push notification. There are two notification types
``` 
Messages with both notification and data payload, both background and foreground. 
In this case, the notification is delivered to the device’s system tray,
and the data payload is delivered in the extras of the intent of your launcher Activity.

If you using {data:"something"}(data-message) with {notification:"something"}(display-message) while your app is in background the data payload will delivered to extras of the intent but not to the onMessageReceived() method.I assume you implement your code for showing notification, so when your app is in foreground onMessageReceived() is trigger and it display the desire notification you want but when it is not onMessageReceived() no get trigger instead android system will handle it with your notification payload. You just have remove {notification:"something"}(display-message/notification tray) from your server side code to always ensure onMessageReceived().
For anyone keep mention onMessageReceived() will always trigger no matter wether it is not foreground or background please visit this (https://firebase.google.com/support/faq/#fcm-android-background)
```

#### 27) #Automatic SMS Verification (https://developers.google.com/identity/sms-retriever/overview)
- Auto SMS detection old flow now deprecated. Now must implement sms-retriever API

#### 28) #Font (https://github.com/googlesamples/android-DownloadableFonts)
- Dynamic ways set fonts to all screens

#### 29) #Create Application component view one by one and include where require (Require discuss more on this)

#### 30) #shared preference (https://github.com/Pixplicity/EasyPrefs)
```
A small library containing a wrapper/helper for the Shared Preferences of android
```

#### 31) #Room Persistence Library (https://developer.android.com/topic/libraries/architecture/room)
```
The Room persistence library provides an abstraction layer over SQLite to allow for more robust database access while harnessing the full power of SQLite.
```

#### 32) #Video player (https://github.com/google/ExoPlayer)
- Currently we are use youtube video player 

#### 33) #font-awesome lib for icon https://github.com/eqot/font-awesome-android

#### 34) #Font resources (https://developer.android.com/guide/topics/resources/font-resource)


  
