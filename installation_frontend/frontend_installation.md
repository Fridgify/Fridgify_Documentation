## How to install Fridgify

So you decided to get yourself the newest Fridge management software. There are two possible ways, the quick and dirty App installation or the building from scratch. We will go through both ways for you.

### App Installation
1. Visit the [release page of our GitHub](https://github.com/Fridgify/Fridgify_Frontend/releases) with your phone
2. Download the newest release
3. Install it as usual or use "Build the app" step 1 and 4


### Build the app
Building from scratch requires a couple more steps.
1. Prepare your environment
    
    1. If you like to use your backend, follow the backend installation guide
    2. Set-up Flutter and Android Studio following one of these guides:
        - [Windows](https://flutter.dev/docs/get-started/install/windows)
        - [Linux](https://flutter.dev/docs/get-started/install/linux)
        - [macOS](https://flutter.dev/docs/get-started/install/macos)
    3. Clone the latest frontend repository
        - `git clone https://github.com/Fridgify/Fridgify_Frontend.git`
2. Edit the project
    
    1. Open the fridgify folder in Android Studio
    2. Set the Flutter SDK by going to File > Settings and changing in 'Languages & Frameworks'>Flutter the SDK path to your Flutter SDK location
    3. Go to the pubspec.yaml file and run pub get and pub upgrade (The IDE should give you the option if not open a terminal and move into the directory and run `flutter pub get`)
    4. If you want to connect your backend to the application go to assets/cfg/app_settings.json and change the host URL

3. Build the project

    1. Run `flutter test` in your project directory to confirm everything is running
    2. Sign your application as shown [here](https://flutter.dev/docs/deployment/android#signing-the-app)
    3. Run `flutter build apk` in your project directory to build the app.
    4. If you would like to install it on your device:
        1. Connect your device to your computer
        2. run `flutter devices` and connect the device id of your phone
        3. run `flutter install -d <device-id>` in your project directory
