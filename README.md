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
  ionic start [projectName] blank [banlkPage]  
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
