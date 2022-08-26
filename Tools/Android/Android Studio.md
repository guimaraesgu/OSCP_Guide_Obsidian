# Android Studio Tools
#### Use


#### Install
Download commandlinetools to /opt directory
```
wget https://dl.google.com/android/repository/commandlinetools-linux-8092744_latest.zip  
```

Unzip it and open android studio
````
./android-studio/bin/studio.sh
````

Go through android-studio configuration

Next, install adb via apt.
```
apt install adb
```

Finally we need to create a device 
```
/opt/cmdline-tools/bin/avdmanager create --name \[device_name] --package “system-images;android-28;default;x86”
```

#### Examples
evil-winrm -S -c cert.pem -k key.pem -r timelapse.htb -i 10.10.11.152
