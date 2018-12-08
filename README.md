# sign_release_apk

Builds for APK for release, aligns, signs with cert, verifies, removes build dirs, and zips for deployment.

### Installation

1. Clone this repo or download the zip from GitHub

2. Setup your shell environment variables (edit `~/.bash_profile or ~/.zshrc`)
   - `export SIGN_RELEASE_KEYSTORE=/path/to/my/javakeystore.jks`
     - Note: this is the keystore you generated from Android Studio
   - `export SIGN_RELEASE_BUILD_TOOLS=~/Library/Android/sdk/build-tools/28.0.3`
     - Replace 28.0.3 with a version of the build tools you have installed

   Altogether your ~/.bash_profile or ~/.zshrc should look something like this

   ```bash
   export SIGN_RELEASE_KEYSTORE=~/Documents/keystore
   export SIGN_RELEASE_BUILD_TOOLS=~/Library/Android/sdk/build-tools/28.0.3
   ```

3. Install gradle into your PATH

   - `brew install gradle`

4. Copy **sign_release** file to the `/usr/local/bin` folder

5. Now you're set up and you can run `sign_release` in terminal when in an Android Studio project either in Terminal itself or from the "Terminal" tab within Android Studio.