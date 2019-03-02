# Ionic
Chill &amp; Study

# Arch-Linux config
PATH:  
/etc/profile  
/etc/bash.bashrc  
  export PATH="$PATH:/$HOME/user/Android/Sdk/tools"  
  export PATH="$PATH:/$HOME/user/Android/Sdk/tools/bin"  

Node.js:  
  npm -g install ionic@4.8.0 cordova //Installing  
  ionic start [projectName] blank [blankPage]  
  ionic serve // Starting server  

Build:  
  sdkmanager --licenses // Accept licenses  
  ionic build // Checke errors  
  **ionic cordova build android // Build an Apk**  
  
Devices check:  
  cordova run android  --list // Show devices
  ionic cordova emulate android --device emulated_device  
  cordova build [emulatorName] // Build new emulator  
  **cordova run android // Open the ionic project and run**  
  **ionic cordova run android -lc // with Log**

-----------------------------------

# NPM for libraries  
Start:
  mkdir folder && cd folder  
  npm init // Start  
  npm install [package] --global // Global var like Ionic  
  npm install [librarie] --save // For the group  
  npm install [librarie] --save-dev // Just for the dev  
  npm install // Inside the folder with package.json  
  npm uninstall librarie --save // Remove librarie and save  

-----------------------------------

# SQLite fix Bugs  
Start:  
  ionic cordova plugin add cordova-sqlite-storage  
  npm install --save @ionic-native/sqlite  
  
**Fix the bug for SQLite 5.0:**  
  app.module.ts | import { SQLite } from '@ionic-native/sqlite/ngx'; // Need to use "package/ngx"  
Refs for this bug:  
https://stackoverflow.com/questions/54396072/type-sqliteoriginal-is-not-assignable-to-type-provider  
https://ionicframework.com/docs/native  
  
Or:**Dowgrade SQLite for 4.8**  
  ionic cordova plugin remove cordova-sqlite-storage  
  npm uninstall --save @ionic-native/sqlite  
  
  1 - ionic cordova plugin add cordova-sqlite-storage@2.5  
  2 - npm install @ionic-native/sqlite@4.8  

-----------------------------------
