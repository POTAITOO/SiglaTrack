# Android Development Setup

This project requires Android SDK to run on Android devices/emulators.

## Prerequisites

1. **Install Android Studio**: Download from https://developer.android.com/studio
   - Install with default settings
   - Make sure to install Android SDK, Android SDK Platform, and Android Virtual Device

2. **Set up Environment Variables**:

   ### For Windows (Git Bash/VS Code Terminal):
   
   Add these lines to your `~/.bash_profile` (for Git Bash) and `~/.bashrc` (for VS Code terminal):
   
   ```bash
   # Android SDK configuration
   export ANDROID_HOME="/c/Users/YOUR_USERNAME/AppData/Local/Android/Sdk"
   export PATH="$PATH:/c/Users/YOUR_USERNAME/AppData/Local/Android/Sdk/platform-tools:/c/Users/YOUR_USERNAME/AppData/Local/Android/Sdk/tools:/c/Users/YOUR_USERNAME/AppData/Local/Android/Sdk/tools/bin"
   ```
   
   **Replace `YOUR_USERNAME` with your actual Windows username**

3. **Reload your terminal** or run:
   ```bash
   source ~/.bash_profile
   source ~/.bashrc
   ```

4. **Verify installation**:
   ```bash
   adb --version
   ```

## Running the Android App

After setup, you can run:
```bash
npx expo run:android
```

## Troubleshooting

- If you get "adb command not found", make sure the environment variables are set correctly
- If Android SDK path is not found, verify Android Studio installed the SDK in the default location
- Close and reopen your terminal after adding environment variables

## Alternative Setup Methods

### Option 1: System Environment Variables (Windows)
1. Open System Properties → Advanced → Environment Variables
2. Add `ANDROID_HOME` pointing to your Android SDK directory
3. Add Android SDK tools to your PATH

### Option 2: Use Android Studio's built-in terminal
Android Studio's terminal comes with Android SDK tools pre-configured.